## Chapter 4: Deploying and Prompting Models in Microsoft Foundry — Practice Questions

**Q1.** A company needs to deploy a language model from Microsoft Foundry for a customer service chatbot that must respond in under 2 seconds with consistent, policy-compliant answers. The solution must minimize costs while meeting performance requirements. Which deployment approach BEST meets these requirements?

A) Deploy GPT-3.5-turbo with temperature set to 0.1 and include detailed system prompt defining policies
B) Deploy GPT-4 with temperature set to 0.9 and max tokens set to 4000
C) Deploy GPT-4 with temperature set to 0.1 and max tokens set to 500
D) Deploy a small language model (SLM) with temperature set to 0.9 and no system prompt

<details>
<summary>Answer</summary>

**Correct: A**

GPT-3.5-turbo provides faster response times and lower costs than GPT-4, meeting the 2-second requirement. Temperature 0.1 ensures consistent, deterministic responses (critical for policy compliance). System prompt defines the policy constraints that apply to all interactions. This balances cost, speed, and compliance.

**Why the others are wrong:**
- GPT-4 is more expensive and slower than needed, and temperature 0.9 produces creative/varied responses that conflict with 'consistent, policy-compliant' requirement
- While GPT-4 with low temperature provides consistency, it's unnecessarily expensive and slower than GPT-3.5-turbo for this use case
- Temperature 0.9 produces unpredictable responses, and without system prompt there's no mechanism to enforce policy compliance

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A developer is testing prompts in the Microsoft Foundry Chat playground and notices responses are too creative and inconsistent. The application requires factual, deterministic answers. Which parameter change will MOST effectively address this issue?

A) Increase max_tokens from 500 to 2000
B) Increase top_p from 0.5 to 0.95
C) Decrease temperature from 0.7 to 0.1
D) Add more examples to the user prompt

<details>
<summary>Answer</summary>

**Correct: C**

Temperature controls randomness. Lower temperature (0.1) makes responses more deterministic and focused, reducing creativity and increasing consistency—exactly what's needed for factual answers. Temperature is the primary parameter for controlling this behavior.

**Why the others are wrong:**
- max_tokens controls response length, not creativity or consistency—it won't solve the randomness problem
- Increasing top_p adds MORE diversity by considering more token possibilities, making responses less deterministic (opposite of what's needed)
- While examples help, they don't directly control randomness—the model can still produce creative variations with high temperature

</details>

---

**Q3.** A healthcare application requires that all AI responses include a disclaimer and never provide medical diagnoses. Where should these requirements be configured in Microsoft Foundry to apply to every user interaction?

A) In the model deployment settings under Safety configurations
B) In each individual user prompt sent to the model
C) In the Foundry Tools pre-built component configuration
D) In the system prompt that defines AI role and constraints

<details>
<summary>Answer</summary>

**Correct: D**

System prompts define AI behavior and constraints that apply to ALL user interactions. Setting role constraints (no diagnoses) and output requirements (always include disclaimer) in system prompt ensures consistent application across every request without requiring users to specify these rules.

**Why the others are wrong:**
- Safety configurations provide content filtering but don't define custom business rules like disclaimers or role limitations
- Requiring constraints in each user prompt is error-prone, inefficient, and gives users ability to bypass requirements
- Foundry Tools are for specific tasks like summarization—they don't provide persistent behavioral constraints across all interactions

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** An organization is deploying a GPT-4 model from the Foundry Models catalog. During deployment configuration, which setting directly controls the maximum number of requests the endpoint can process per minute?

A) Model version selection
B) Deployment name
C) Token quota (TPM - Tokens Per Minute)
D) Temperature parameter

<details>
<summary>Answer</summary>

**Correct: C**

Token quota (TPM - Tokens Per Minute) is the deployment setting that limits throughput capacity of the endpoint. This directly controls rate limiting and affects how many requests can be processed per minute based on token consumption per request.

**Why the others are wrong:**
- Model version affects capabilities and features but doesn't control request rate limits
- Deployment name is just an identifier for the endpoint—it has no functional impact on throughput
- Temperature is a prompt parameter that affects response randomness—it's not a deployment configuration and doesn't control request rates

</details>

---

**Q5.** A developer wrote this Foundry SDK code:

client = OpenAI(endpoint=url, credential=key)
response = client.chat.completions.create(
    model="gpt-35-turbo",
    messages=[{"role": "system", "content": "You are helpful"}, {"role": "user", "content": "Summarize this"}]
)
print(response.choices[0].message.content)

What does this code accomplish?

A) It trains a new GPT-3.5-turbo model using the provided messages as training data
B) It sends a chat request to an existing deployment with system and user messages, then prints the AI response
C) It deploys a model endpoint named 'gpt-35-turbo' to the specified URL
D) It configures the Foundry Models catalog to add a helpful assistant template

<details>
<summary>Answer</summary>

**Correct: B**

The code initializes a client connection to an existing endpoint, creates a chat completion request with a system prompt ('You are helpful') and user prompt ('Summarize this'), sends it to the deployed 'gpt-35-turbo' model, and prints the response text. This is standard inference/prompting code, not training or deployment.

**Why the others are wrong:**
- The SDK doesn't train models—it calls existing deployed models. Training happens in Foundry portal with different workflows
- The code calls an existing deployment (specified by endpoint URL), it doesn't create or deploy anything—deployment happens in Foundry portal
- This is client-side inference code, not catalog configuration—it uses an already-deployed model, doesn't modify the catalog

</details>

---

**Q6.** A company needs an AI solution to extract key dates, dollar amounts, and party names from legal contracts. Which Microsoft Foundry capability is MOST appropriate for this requirement?

A) Deploy GPT-4 and write custom system prompts for extraction
B) Use Chat playground with high temperature settings
C) Configure deployment quota settings for data extraction workload
D) Use Foundry Tools pre-built extraction component

<details>
<summary>Answer</summary>

**Correct: D**

Foundry Tools provide pre-built components for common tasks including extraction. The extraction component is purpose-built for pulling structured information (dates, amounts, names) from documents—faster to implement and optimized for this specific use case compared to custom prompting.

**Why the others are wrong:**
- While this works, it requires custom prompt engineering and testing—less efficient than using a pre-built, optimized extraction tool already designed for this task
- Chat playground is for testing prompts interactively, not for production extraction tasks. High temperature would hurt extraction accuracy (need deterministic, precise extraction)
- Quota settings control throughput limits, they don't provide extraction functionality—completely unrelated to the extraction task

</details>

---

**Q7.** A retail chatbot must respond to product questions but should NEVER discuss competitor products or pricing. During prompt engineering in the Chat playground, which approach MOST effectively implements this constraint?

A) Include the constraint 'Never discuss competitor products or pricing' in the system prompt with examples of what to refuse
B) Set temperature to 0.0 to prevent any mentions of competitors
C) Add competitor names to a blocked words list in the user prompt for each request
D) Deploy a smaller language model (SLM) which has less knowledge of competitors

<details>
<summary>Answer</summary>

**Correct: A**

System prompts define behavioral constraints that apply to all interactions. Explicitly stating the constraint with examples (few-shot prompting) trains the model to recognize and refuse competitor discussions. This is the proper use of system prompts for defining AI behavior and boundaries.

**Why the others are wrong:**
- Temperature controls randomness, not content restrictions—even at 0.0, the model can still discuss competitors if prompted directly
- This is inefficient, error-prone, and requires updating every user request—system prompts are designed to handle persistent constraints
- SLMs still know about competitors, just less detail. More importantly, this approach sacrifices overall quality to solve a constraint problem that should be handled by prompting

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** After deploying a GPT-3.5-turbo model in Microsoft Foundry, which resource provides the URL and authentication needed for SDK client initialization?

A) The Models catalog entry for GPT-3.5-turbo
B) The deployment endpoint configuration page
C) The Chat playground settings panel
D) The Foundry subscription resource keys

<details>
<summary>Answer</summary>

**Correct: B**

After deployment, the endpoint configuration page displays the specific endpoint URL and keys for that particular deployment. This is where you get the exact values needed for client.init(endpoint=url, credential=key) in SDK code. Each deployment has its own endpoint.

**Why the others are wrong:**
- The catalog shows available models to deploy but doesn't provide deployment-specific endpoints—endpoints are created only after you deploy a model
- Chat playground is for testing prompts, not for accessing deployment credentials—it uses endpoints but doesn't display the connection details needed for SDK code
- Subscription keys are account-level, but you need the deployment-specific endpoint URL that points to your particular GPT-3.5-turbo deployment instance

</details>

---

