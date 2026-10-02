# Chapter 4 Lab: Deploying and Prompting Models in Microsoft Foundry

**Estimated time:** 20 minutes

## Exercise

Foundry portal lab: deploy GPT-3.5-turbo model, open Chat playground, write a system prompt defining an AI customer support agent with specific constraints (polite tone, max 100 words, no financial advice), test 5 user prompts, observe behavior changes with temperature 0.0 vs 0.7, export conversation, review provided SDK code that sends the same prompts programmatically

## Key takeaway

Microsoft Foundry deployment involves selecting a model from the catalog, assigning a deployment name (used in SDK calls), and writing system prompts to define persistent AI behavior—the exam tests the distinction between model names and deployment names, and where to specify constraints (system prompt for all interactions, user prompt for specific queries).
