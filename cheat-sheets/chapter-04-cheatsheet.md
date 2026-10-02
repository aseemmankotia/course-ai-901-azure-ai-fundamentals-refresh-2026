# Chapter 4: Deploying and Prompting Models in Microsoft Foundry — Quick Reference

## Deployment Configuration
| Setting | Purpose | Exam Notes |
|---------|---------|------------|
| **Model Selection** | Choose GPT-4, GPT-3.5-turbo, or SLM | GPT-3.5-turbo = faster + cheaper for most tasks |
| **Deployment Name** | Identifier for endpoint | Used in SDK model parameter |
| **Token Quota (TPM)** | Tokens Per Minute limit | Controls throughput capacity and rate limiting |
| **Endpoint URL** | API endpoint for requests | Required for SDK client initialization |

## Chat Playground Parameters
| Parameter | Range | Effect | When to Use |
|-----------|-------|--------|-------------|
| **temperature** | 0.0-1.0 | 0.1=focused/deterministic, 0.9=creative/random | Low (≤0.3) for facts/policies, high for creative tasks |
| **max_tokens** | 1-4096+ | Limits response length | Increase if responses cut off, decrease for brevity |
| **top_p** | 0.0-1.0 | Nucleus sampling (lower=fewer options) | Usually leave default; temperature preferred for control |

## Prompt Types
| Type | Purpose | Scope | Example Use |
|------|---------|-------|-------------|
| **System Prompt** | Define AI role, behavior, constraints | Applies to ALL user interactions | "You are a customer service agent. Never discuss competitors. Always include disclaimer." |
| **User Prompt** | Specific query or task | Single request | "What are the return policy details for order #12345?" |

## Prompt Engineering Principles
1. **Be Specific**: "Extract dates in YYYY-MM-DD format" > "find dates"
2. **Provide Examples** (few-shot): Show desired input/output format
3. **Set Constraints**: "Response must be under 50 words" / "Never mention pricing"
4. **Iterate**: Test in playground, refine based on results

## Model Comparison
| Model | Speed | Cost | Context Length | Best For |
|-------|-------|------|----------------|----------|
| **GPT-4** | Slower | Higher | Longer | Complex reasoning, long documents |
| **GPT-3.5-turbo** | Faster | Lower | Shorter | General tasks, cost optimization |
| **SLMs** | Fastest | Lowest | Shortest | Simple, specialized tasks |

## Foundry SDK Basics (Read & Understand)
```python
# 1. Initialize client with endpoint and key
client = OpenAI(endpoint=url, credential=key)

# 2. Create chat completion with messages
response = client.chat.completions.create(
    model="gpt-35-turbo",  # Deployment name
    messages=[
        {"role": "system", "content": "System prompt here"},
        {"role": "user", "content": "User prompt here"}
    ]
)

# 3. Access response content
output = response.choices[0].message.content
```

**Message Roles**:
- `system`: Defines AI behavior (persistent instructions)
- `user`: End user query
- `assistant`: AI's previous response (for multi-turn conversations)

## Foundry Tools
| Tool | Purpose | When to Use |
|------|---------|-------------|
| **Extraction** | Pull structured data from text | Extracting dates, names, amounts from documents |
| **Summarization** | Condense long content | Long reports, articles |
| **Q&A** | Answer questions from knowledge base | FAQ, document search |

**Exam Tip**: Use pre-built tools when task matches—faster than custom prompting.

## Common Exam Scenarios
| Requirement | Solution |
|-------------|----------|
| Consistent, policy-compliant responses | Low temperature (0.1) + detailed system prompt |
| Fast, cost-effective chatbot | GPT-3.5-turbo deployment |
| Complex reasoning task | GPT-4 deployment |
| Extract structured data from documents | Foundry Tools extraction component |
| Apply constraint to all interactions | Define constraint in system prompt |
| Control request rate limits | Configure TPM (Tokens Per Minute) quota |

## Key Exam Gotchas
- **Temperature 0.0 ≠ content filtering**: Low temp makes responses focused, doesn't block topics (use system prompt for constraints)
- **max_tokens controls OUTPUT length only**: Doesn't limit input or control randomness
- **System prompt applies to all requests**: Don't repeat constraints in each user prompt
- **TPM quota = throughput limit**: Higher TPM allows more requests/min but costs more
- **Deployment name in SDK ≠ model name in catalog**: Use deployment name you created, not "gpt-4" generically
