## Chapter 5: Building Chat Apps and Single-Agent Solutions — Practice Questions

**Q1.** A company is building a customer service solution using Azure AI Foundry. They need the solution to automatically check inventory databases and update order status without requiring explicit instructions for each action. Which approach should they implement?

A) A chat application with prompt engineering to format database queries
B) A single-agent solution with tools configured for database access and order management
C) A chat application with streaming responses enabled for real-time updates
D) A multi-turn conversation chat application with conversation history maintained

<details>
<summary>Answer</summary>

**Correct: B**

Agents autonomously decide when to invoke tools based on user queries. The requirement for automatic database checks and order updates without explicit instructions requires an agent that can make decisions and invoke tools independently. A single-agent solution with configured tools for database access meets this need.

**Why the others are wrong:**
- Chat applications respond to prompts but don't autonomously invoke tools or make decisions about when to query databases
- Streaming responses improve user experience by showing tokens as generated but don't enable autonomous tool invocation or decision-making
- Conversation history maintains context across messages but doesn't provide autonomous tool invocation capabilities

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A developer is implementing a chat application using the Azure AI Foundry SDK. After initializing the client with endpoint and key, what is the correct next step to send a user message?

A) Call client.send() with the user's text string directly
B) Build a message array containing system and user message objects, then pass to client.complete()
C) Create a prompt template and call client.generate() with the template
D) Initialize a conversation session and append messages to the session object

<details>
<summary>Answer</summary>

**Correct: B**

The standard SDK flow is: initialize client → build message array with roles (system, user, assistant) → send request using client.complete() or similar method → parse response. Messages must be structured as an array of message objects with role and content properties.

**Why the others are wrong:**
- The SDK requires structured message objects with roles, not raw text strings passed directly to send()
- The SDK uses message arrays, not prompt templates with a generate() method
- The SDK uses message arrays passed to completion methods, not session objects with append operations

</details>

---

**Q3.** A customer support chat application needs to reference earlier parts of the conversation when answering follow-up questions. The user asks 'What was the order number?' after previously discussing an order. How should the application maintain this context?

A) Store conversation state in a database and query it before each response
B) Enable streaming responses to maintain connection state across messages
C) Include all prior messages (system, user, assistant) in the message array when sending each new request
D) Configure the agent with a memory tool that stores previous interactions

<details>
<summary>Answer</summary>

**Correct: C**

Conversation history is maintained by including all prior messages in the message array sent with each request. The model receives the full conversation context (system message, all user messages, all assistant responses) to understand references to earlier parts of the conversation.

**Why the others are wrong:**
- While database storage might be used for persistence, context is provided to the model by including messages in the request array, not by external querying
- Streaming affects how responses are delivered (token by token) but doesn't maintain conversation context across separate requests
- Memory tools are for agents with external data access; basic conversation context is maintained through the message array, not tool configuration

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** A company wants to improve user experience in their chat application by displaying responses as they're generated rather than waiting for the complete response. Which Azure AI Foundry SDK feature should they implement?

A) Async/await completion methods with callback handlers
B) Batch processing with response caching enabled
C) Multi-agent orchestration with parallel tool invocation
D) Streaming responses to receive tokens as they're generated

<details>
<summary>Answer</summary>

**Correct: D**

Streaming responses enable receiving tokens as they're generated, allowing the UI to display partial responses in real-time. This provides better UX by showing immediate progress rather than waiting for the complete response. The SDK provides streaming methods that yield tokens incrementally.

**Why the others are wrong:**
- Async/await improves performance but still waits for complete responses; it doesn't provide incremental token delivery
- Batch processing and caching are for efficiency and cost optimization, not for incremental response display during generation
- Multi-agent orchestration is for complex workflows with multiple agents; streaming is a response delivery mechanism for better UX

</details>

---

**Q5.** An organization is creating a travel booking agent in Azure AI Foundry portal. The agent needs to search flight databases, check hotel availability, and calculate total trip costs. What is required to enable the agent to perform these actions autonomously?

A) Write detailed system prompts instructing the agent when to perform each action
B) Configure tool definitions with function names, parameters, and return types for each capability
C) Enable the agent's built-in search and calculation plugins in the portal settings
D) Create separate agents for each function and configure agent-to-agent communication

<details>
<summary>Answer</summary>

**Correct: B**

Agents require tool definitions configured in Foundry portal. Each tool must have: function name, parameters (with types and descriptions), and return types. The agent then autonomously decides when to invoke which tool based on user queries. Tool configuration defines what capabilities the agent has access to.

**Why the others are wrong:**
- System prompts provide context but don't give agents the actual capability to invoke tools; tool definitions with function signatures are required
- Tools must be explicitly defined with function signatures; there are no built-in plugins that automatically enable search and calculations without configuration
- A single agent with multiple tools handles this scenario; multi-agent orchestration is for more complex workflows requiring specialized agents

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** A developer is testing a single-agent solution in the Azure AI Foundry portal. The agent has access to three tools: database_query, send_email, and calculate_price. When asked 'What's the total cost for order 12345?', which component determines whether to invoke database_query, calculate_price, or both?

A) The Foundry portal's built-in routing logic based on keyword matching
B) The developer must specify tool invocation order in the agent configuration
C) The underlying language model decides which tools to invoke based on the query and tool definitions
D) The first tool whose parameter types match the query input gets invoked automatically

<details>
<summary>Answer</summary>

**Correct: C**

Agent decision-making: the underlying language model analyzes the user query and available tool definitions (function names, descriptions, parameters) to decide which tools to invoke and in what order. The model reasons about which tools are needed to fulfill the request. This is the key difference between chat apps (no autonomous decisions) and agents (autonomous tool invocation).

**Why the others are wrong:**
- Tool invocation is decided by the language model's reasoning, not simple keyword matching in portal routing logic
- The agent (model) makes autonomous decisions about tool invocation; developers define available tools but don't hard-code invocation sequences
- Tool selection is based on semantic understanding of the query and tool purposes, not automatic parameter type matching

</details>

---

**Q7.** During agent testing in Azure AI Foundry portal, a developer needs to verify that their agent correctly invoked the search_products tool before providing a product recommendation. Where can they observe this tool invocation?

A) In the response JSON's metadata section containing tool_calls array
B) In the Azure Monitor Application Insights trace logs
C) In the Foundry portal agent testing interface tool invocation logs
D) In the agent's conversation history as a special system message

<details>
<summary>Answer</summary>

**Correct: C**

The Foundry portal agent testing interface provides tool invocation logs showing which tools were called, with what parameters, and what they returned. This testing interface is specifically designed for observing and debugging agent behavior during development.

**Why the others are wrong:**
- While tool calls may appear in response structures, the primary interface for observing tool invocation during testing is the portal's dedicated testing interface and logs
- Azure Monitor is for production monitoring; the portal's testing interface is the primary tool for development-time agent testing and debugging
- Tool invocations are logged separately in the testing interface; they don't appear as system messages in conversation history

</details>

---

**Q8.** A company is building a solution where users ask questions about company policies. The solution should only provide answers based on policy documents without taking any automated actions. The solution needs to reference previous questions in the conversation. Which implementation approach is most appropriate?

A) A single-agent solution with a document search tool configured
B) A multi-agent solution with one agent for search and one for response generation
C) A chat application with streaming responses and prompt engineering for policy context
D) A chat application that includes conversation history in each request

<details>
<summary>Answer</summary>

**Correct: D**

This is a chat application use case, not an agent. The solution responds to prompts and doesn't need to autonomously invoke tools or make decisions about actions. Chat application with conversation history (including prior messages in requests) handles context across questions. Prompt engineering with policy context enables accurate responses without autonomous tool invocation.

**Why the others are wrong:**
- Agents autonomously invoke tools; this scenario only requires answering questions without automated actions, making a chat application more appropriate
- Multi-agent solutions are for complex workflows requiring specialized agents; this simple Q&A scenario doesn't require agent orchestration
- While streaming improves UX, this scenario needs conversation history maintained (prior messages included), not specifically an agent with tools

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

