# Chapter 3: How Generative AI Models Work - Cheat Sheet

## Model Selection Matrix

| Requirement | Choose GPT-4 | Choose GPT-3.5 | Choose SLM |
|-------------|--------------|----------------|------------|
| Complex reasoning | ✓ | | |
| Multi-step problems | ✓ | | |
| Cost optimization | | ✓ | ✓✓ |
| Speed critical (<1s) | | ✓ | ✓✓ |
| High volume (1000s/day) | | ✓ | ✓✓ |
| Specialized domain | | | ✓ |
| Local deployment | | | ✓ |
| Simple/repetitive tasks | | ✓ | ✓ |

## Token Essentials

- **1 token** ≈ 4 characters ≈ 0.75 words (English)
- **Token limit** = prompt + completion combined
- Example: 8192 token limit, 1000 token prompt → max_tokens ≤ 7192
- **Billing**: Per token (input + output)
- **Exam gotcha**: Students forget limit is cumulative

## Temperature Settings

| Value | Behavior | Use Case |
|-------|----------|----------|
| 0.0 | Deterministic, consistent | Data extraction, SQL, factual Q&A |
| 0.3-0.5 | Mostly consistent | Documentation, technical writing |
| 0.7 | Balanced (default) | General content, chatbots |
| 0.9-1.0 | Creative, varied | Marketing, stories, brainstorming |

**Exam rule**: Factual accuracy needed = low temperature (0-0.3)

## Key Parameters

```python
# Azure OpenAI API configuration
{
  "messages": [
    {"role": "system", "content": "Set behavior/role here"},
    {"role": "user", "content": "Actual request here"}
  ],
  "temperature": 0.7,        # 0-2, controls randomness
  "max_tokens": 500,         # Max output length
  "top_p": 0.95,             # Alternative to temperature
  "frequency_penalty": 0,    # Reduce repetition (0-2)
  "presence_penalty": 0      # Encourage new topics (0-2)
}
```

## Hallucination vs Grounding

**Hallucination** = Generating false information (fake citations, statistics, facts)

**Solutions** (in order of effectiveness):
1. **RAG (Retrieval-Augmented Generation)** - Provide documents as context
2. Lower temperature - More deterministic
3. Clear instructions - "Only use provided information"
4. ❌ **Not solutions**: Bigger model alone, system message alone

**Exam scenario**: "Model cites non-existent case law" → Answer: Implement RAG

## LLM vs SLM Decision Tree

```
Does task require complex reasoning/nuance?
├─ YES → LLM (GPT-4 if very complex, GPT-3.5 otherwise)
└─ NO → Is speed/cost critical?
   ├─ YES → Is it a specialized domain?
   │  ├─ YES → SLM (fine-tuned)
   │  └─ NO → GPT-3.5-turbo
   └─ NO → GPT-3.5-turbo
```

## Embeddings Quick Reference

- **Purpose**: Convert text → numeric vectors for semantic similarity
- **Use cases**: 
  - Similarity search
  - Document retrieval for RAG
  - Clustering/classification
  - Semantic search
- **Not for**: Generation, translation, compression
- **Exam tip**: "Find similar documents" = embeddings + vector search

## Common Limitations (Exam-Heavy)

| Limitation | Impact | Solution |
|------------|--------|----------|
| Training cutoff | No current data | RAG with current docs |
| Hallucination | Fake facts | RAG, lower temperature, validation |
| Token limits | Can't process long docs | Chunking, summarization |
| No execution | Can't run code/queries | Function calling, tools |
| Determinism | Same input ≠ same output* | Temperature = 0 (*not guaranteed) |

## Message Roles

- **System**: Sets behavior/persona (persistent for conversation)
- **User**: Actual request/question/input
- **Assistant**: Model's response (in conversation history)

**Exam gotcha**: System message doesn't reduce tokens or prevent hallucination alone

## Typical Use Cases for Exam

1. **Content generation**: Blogs, emails, product descriptions
2. **Summarization**: Long docs → key points
3. **Translation**: Cross-language content
4. **Q&A**: FAQs, customer support
5. **Code completion**: IDE features
6. **Conversational agents**: Chatbots

**Pattern recognition for exam**: Match scenario details to use case
- "Generate 1000 product descriptions" → Content generation + cost concern → GPT-3.5 or SLM
- "Answer legal questions accurately" → Q&A + grounding concern → RAG required
- "Complete code as user types" → Code completion + latency concern → GPT-3.5 or SLM
