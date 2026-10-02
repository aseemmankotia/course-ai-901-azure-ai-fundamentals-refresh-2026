# Chapter 5 Lab: Building Chat Apps and Single-Agent Solutions

**Estimated time:** 22 minutes

## Exercise

Two-part lab: (1) Review Foundry SDK chat client code (provided in GitHub), identify client initialization, message structure, response handling—explain what each block does without writing code. (2) Foundry portal: create a single-agent solution with access to a mock 'product catalog search' tool, configure tool parameters, test agent with queries like 'find products under $50', observe agent invoking tool vs responding directly

## Key takeaway

Chat applications use the Foundry SDK to send prompts and receive responses (stateless unless you maintain conversation history), while agent solutions autonomously invoke configured tools based on the user's query—the exam tests your ability to distinguish when to build a chat app (simple Q&A) versus an agent (multi-step autonomous task completion).
