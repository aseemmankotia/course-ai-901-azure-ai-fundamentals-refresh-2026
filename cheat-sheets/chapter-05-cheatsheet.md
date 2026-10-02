# Chapter 5: Building Chat Apps and Single-Agent Solutions

## Chat Applications vs Agents

| Feature | Chat Application | Agent |
|---------|-----------------|-------|
| **Core function** | Responds to prompts | Makes decisions, invokes tools autonomously |
| **Tool invocation** | No | Yes — decides when and which tools |
| **Use case** | Q&A, conversation, content generation | Database queries, API calls, multi-step workflows |
| **Decision-making** | No autonomous decisions | Model decides tool invocation based on query |
| **Exam keyword** | "respond to user", "answer questions" | "automatically", "autonomously", "invoke tools" |

## Foundry SDK Chat Flow

### Required Steps (in order)
```python
# Step 1: Initialize client
client = ChatClient(endpoint=ENDPOINT, credential=KEY)

# Step 2: Build message array
messages = [
    {"role": "system", "content": "You are a helpful assistant"},
    {"role": "user", "content": "Hello"}
]

# Step 3: Send request
response = client.complete(messages=messages)

# Step 4: Parse response
answer = response.choices[0].message.content
```

### Message Roles
- **system**: Instructions, context, behavior guidelines (typically one at start)
- **user**: User input, questions
- **assistant**: Model responses (included in conversation history)

## Conversation History

**How it works**: Include ALL prior messages in message array for each new request

```python
# Request 1
messages = [
    {"role": "system", "content": "..."},
    {"role": "user", "content": "What's order 123?"}
]
# Get response, append to messages

# Request 2 — includes history
messages.append({"role": "assistant", "content": "Order 123 is..."})
messages.append({"role": "user", "content": "What was that order number?"})
# Model sees full context, can reference "order 123"
```

**Exam trap**: Conversation history ≠ streaming. History = message array content. Streaming = token delivery method.

## Streaming Responses

**Purpose**: Receive tokens as generated (better UX — immediate feedback)

**Not for**: Context management, conversation history, tool invocation

```python
stream = client.complete(messages=messages, stream=True)
for chunk in stream:
    print(chunk.choices[0].delta.content, end="")
```

## Single-Agent Solutions

### Agent Tool Configuration (Portal)

**Required elements**:
1. **Function name**: Identifier for the tool
2. **Parameters**: Name, type, description (description is critical for model decision-making)
3. **Return type**: What the tool returns

**Example**:
```json
{
  "name": "search_products",
  "description": "Search product catalog by keyword",
  "parameters": {
    "query": {
      "type": "string",
      "description": "Search term for product name or category"
    },
    "max_results": {
      "type": "integer",
      "description": "Maximum number of results to return (1-50)"
    }
  },
  "returns": "array of product objects"
}
```

### Agent Decision-Making

**Who decides**: Underlying language model (NOT keyword matching, NOT hard-coded rules)

**Based on**: 
- User query content
- Tool definitions (names, descriptions, parameters)
- Tool parameter descriptions (model uses these to determine relevance)

**Exam concept**: Model autonomously decides which tools to invoke and in what order. This autonomous decision-making is what makes it an agent vs. chat app.

## Testing Agents in Foundry Portal

### Testing Interface Features
- Send test queries to agent
- **Tool invocation logs**: See which tools called, parameters passed, results returned
- Conversation flow visualization
- Error messages for failed tool invocations

**Exam note**: Portal testing interface is for development/debugging. Production monitoring uses Azure Monitor.

### What to Verify
1. Correct tool invoked for query type
2. Appropriate parameters passed to tool
3. Tool results incorporated into final response
4. Multi-turn conversations maintain context
5. Error handling when tool invocation fails

## Common Exam Scenarios

| Scenario | Solution |
|----------|----------|
| "Automatically check database without explicit instruction" | Agent with database tool |
| "Reference earlier parts of conversation" | Chat app with conversation history (message array) |
| "Display response as it's generated" | Streaming responses |
| "Decide when to call which API" | Agent with multiple tools (model decides) |
| "Answer questions about documents" | Chat app (if no automated actions needed) |
| "Update records and send notifications" | Agent with tools for both operations |

## Key Exam Traps

1. **Chat app vs Agent**: Keywords "automatically", "autonomously", "without explicit instructions" → Agent
2. **Streaming ≠ Context**: Streaming is UX (token delivery). Context is message array content.
3. **Tool decision-making**: Model decides (not keyword matching, not hard-coded)
4. **Parameter descriptions matter**: Model uses them to decide tool invocation — not just documentation
5. **Testing vs Production**: Portal testing interface for dev. Azure Monitor for production.
