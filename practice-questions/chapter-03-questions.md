## Chapter 3: How Generative AI Models Work — Practice Questions

**Q1.** A company needs to process customer support tickets and generate responses. They receive 50,000 tickets per day and need responses within 2 seconds. The average ticket is 200 words. Cost optimization is critical. Which approach BEST meets these requirements?

A) Use a Small Language Model (SLM) fine-tuned on historical support data with local deployment
B) Use GPT-4 with temperature set to 0 for maximum consistency across all tickets
C) Use GPT-3.5-turbo with Azure OpenAI Service and cache common responses
D) Use an embedding model to find similar tickets and return exact previous responses

<details>
<summary>Answer</summary>

**Correct: A**

SLM provides low latency (local deployment eliminates API calls), low cost per inference, and can be specialized for the support domain. 50,000 tickets/day with 2-second SLA requires fast, cost-effective inference that SLMs excel at.

**Why the others are wrong:**
- GPT-4 is too slow (higher latency) and expensive for high-volume, repetitive tasks requiring 2-second responses. Cost would be prohibitive at 50K/day.
- GPT-3.5-turbo is better than GPT-4 for cost but still has API latency and token costs that accumulate. Caching helps but doesn't address core latency and volume cost issues.
- Embeddings find similar content but don't generate responses. This only solves retrieval, not generation. You'd still need an LLM to generate the actual response text.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A legal firm is building an AI assistant to answer questions about case law. The system frequently generates citations to cases that don't exist. What should be implemented to address this issue?

A) Increase the temperature parameter to 0.9 to make responses more creative and diverse
B) Use a larger model like GPT-4 instead of GPT-3.5 to improve accuracy
C) Implement retrieval-augmented generation (RAG) to ground responses in actual case law documents
D) Add a system message instructing the model to only cite real cases

<details>
<summary>Answer</summary>

**Correct: C**

This describes hallucination - generating false information. Grounding with retrieval (RAG) provides the model with actual case law documents as context, ensuring citations reference real cases from the knowledge base.

**Why the others are wrong:**
- Higher temperature increases randomness and creativity, making hallucination MORE likely, not less. Temperature should be lowered (closer to 0) for factual tasks.
- While larger models may have better reasoning, they still hallucinate without grounding. Size alone doesn't solve the lack of access to actual case law documents.
- System messages provide instructions but don't prevent hallucination. The model has no way to verify if a case exists without access to real case law data through retrieval.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A developer is calling Azure OpenAI API and receives an error: 'This model's maximum context length is 8192 tokens, however you requested 9500 tokens.' The prompt is 1000 tokens and max_tokens is set to 8500. What is the issue?

A) The max_tokens parameter should be reduced to 7192 or less
B) The model needs to be upgraded to one with a larger context window
C) The prompt needs to be compressed to under 500 tokens
D) The token limit includes both input and output, so max_tokens plus prompt must not exceed 8192

<details>
<summary>Answer</summary>

**Correct: D**

Token limits are for the total context window (input + output). With 1000 token prompt and 8500 max_tokens, the total requested is 9500, exceeding the 8192 limit. Solution: set max_tokens to 7192 or less (8192 - 1000).

**Why the others are wrong:**
- This is the solution, not the issue explanation. The question asks what IS the issue, not how to fix it.
- While upgrading to a larger model would work, it doesn't identify the actual issue - that the developer misunderstood how token limits work (they're cumulative).
- The prompt doesn't need compression. At 1000 tokens it leaves 7192 tokens for completion. The issue is max_tokens is set too high, not that the prompt is too long.

</details>

---

**Q4.** An e-commerce company wants to generate product descriptions. They need descriptions to be factually accurate about product specifications but creative in marketing language. Which configuration BEST achieves this?

A) Temperature 0.0, provide specifications in system message, use GPT-4 for best quality
B) Temperature 0.7, provide specifications in user message as context, use GPT-3.5-turbo for cost efficiency
C) Temperature 1.0, use embeddings to find similar products, use SLM for speed
D) Temperature 0.3, implement RAG with product database, use GPT-4 for complex reasoning

<details>
<summary>Answer</summary>

**Correct: B**

Temperature 0.7 balances creativity (for marketing language) with consistency (for specifications). Providing specs as context grounds the factual content. GPT-3.5-turbo is sufficient for this task and cost-effective for high-volume product descriptions.

**Why the others are wrong:**
- Temperature 0.0 produces deterministic output with no creativity - descriptions would be repetitive and bland. Also, GPT-4 is unnecessarily expensive for product descriptions that don't require complex reasoning.
- Temperature 1.0 is too high for maintaining factual accuracy about specifications. Embeddings alone don't generate text. SLMs may lack the general language quality needed for creative marketing copy.
- Temperature 0.3 is too conservative for creative marketing language. RAG is overkill when specifications can be passed directly in the prompt. GPT-4 is excessive for this task.

</details>

---

**Q5.** What is the primary reason that embeddings are used in AI applications?

A) To convert text into numeric vectors that capture semantic meaning for similarity comparison
B) To reduce the token count of input text and lower API costs
C) To compress large language models into smaller models for faster inference
D) To translate text between languages while preserving grammatical structure

<details>
<summary>Answer</summary>

**Correct: A**

Embeddings convert text to numeric vectors (arrays of numbers) that represent semantic meaning. Text with similar meaning has similar vectors, enabling similarity search, clustering, and retrieval - the foundation of RAG systems.

**Why the others are wrong:**
- Embeddings don't reduce token count - they're a different representation for different purposes (similarity/search). The embedded text still has the same token count when processed by an LLM.
- Embeddings are representations of text data, not models. Model compression techniques like quantization and distillation reduce model size, not embeddings.
- Translation is done by LLMs, not embeddings. While multilingual embeddings exist, their purpose is semantic representation, not translation.

</details>

---

**Q6.** A healthcare application needs to generate patient education materials. The content must be based on current medical guidelines updated monthly. The model was trained on data through 2023. What limitation must be addressed?

A) The model will hallucinate medical information and should not be used for healthcare
B) The model's token limit is too small for comprehensive medical education materials
C) The model lacks real-time data and requires grounding with current guideline documents
D) The model needs fine-tuning on medical data to understand healthcare terminology

<details>
<summary>Answer</summary>

**Correct: C**

LLMs are trained on static datasets and don't have access to information after their training cutoff date. Monthly guideline updates require retrieval-augmented generation (RAG) to provide current guidelines as context.

**Why the others are wrong:**
- While hallucination is a concern in healthcare, the specific issue described is outdated training data. The model can be used with proper grounding and human review. The question specifically highlights the currency issue, not hallucination generally.
- Token limits affect prompt length but aren't the core issue here. The problem is the model's knowledge cutoff date, not its ability to process long content.
- Medical terminology is common in training data. The issue isn't understanding medical language but having access to the latest guidelines which change monthly.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** A developer is choosing between GPT-4 and GPT-3.5-turbo for a code completion feature in an IDE. The feature needs to complete 10-20 line code snippets in under 1 second. Which factor is MOST important for this decision?

A) GPT-4's superior reasoning ability for complex algorithmic problems
B) GPT-4's larger context window for understanding more surrounding code
C) GPT-3.5-turbo's lower latency meeting the 1-second requirement
D) GPT-3.5-turbo's lower cost reducing per-completion expenses

<details>
<summary>Answer</summary>

**Correct: C**

The 1-second latency requirement is a hard constraint. GPT-3.5-turbo has significantly lower latency than GPT-4 and is sufficient for 10-20 line code completions. Performance requirements trump other factors when they're non-negotiable.

**Why the others are wrong:**
- While GPT-4 has better reasoning, 10-20 line completions don't typically require complex reasoning - they're pattern-based. More importantly, if GPT-4 can't meet the 1-second SLA, reasoning ability is irrelevant.
- Context window is useful but not the limiting factor for short code completions. The 1-second latency requirement is the primary constraint that must be met first.
- Cost is important but secondary to meeting the functional requirement. If the feature is too slow, users won't use it regardless of cost savings.

</details>

---

**Q8.** In a prompt to Azure OpenAI, a developer includes: system message defining role as a SQL expert, user message with a natural language question, and sets temperature to 0.2. What is the purpose of the system message in this configuration?

A) To set the behavioral context and domain expertise that shapes all subsequent responses
B) To provide example SQL queries the model should reference when generating responses
C) To reduce token usage by compressing instructions into a special message type
D) To enable function calling features that allow the model to execute SQL queries

<details>
<summary>Answer</summary>

**Correct: A**

System messages set persistent context and behavior for the entire conversation. They define the 'role' or 'persona' and apply to all user messages in that session. Here, it frames the model as a SQL expert for all responses.

**Why the others are wrong:**
- While system messages can include examples, their primary purpose is setting behavioral context, not providing reference material. Examples would more commonly go in user messages as few-shot prompts.
- System messages don't reduce token usage - they add tokens. All message types count toward token limits equally.
- Function calling is a separate feature enabled through specific API parameters, not through system messages. System messages provide context, not executable capabilities.

</details>

---

