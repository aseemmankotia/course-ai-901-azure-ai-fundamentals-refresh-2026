# Answer Key — Practice Test 1

**Q1. Correct: B**

Computer vision workloads analyze and interpret visual content including images. Detecting abnormalities in X-rays requires image classification and object detection capabilities, which are core computer vision tasks. Azure AI Vision and Custom Vision services support medical imaging scenarios.

---

**Q2. Correct: D**

Fairness requires AI systems to treat all people equitably and not discriminate based on protected characteristics or proxies for them. University affiliation can be a proxy for socioeconomic status, race, or geography. Systematically scoring candidates differently based on their university violates fairness principles regardless of actual qualifications.

---

**Q3. Correct: B**

Retrieval-augmented generation (RAG) combines information retrieval with generation. It first retrieves relevant documents from the company's knowledge base, then uses that retrieved context to ground the LLM's response. This significantly reduces hallucination because answers are based on actual source material rather than the model's training data. Azure AI Search integrated with Azure OpenAI Service supports RAG patterns.

---

**Q4. Correct: A**

Document intelligence (formerly Form Recognizer) is specifically designed to extract structured information from documents including invoices. Azure AI Document Intelligence includes prebuilt models for invoices that extract key-value pairs, line items, tables, and specific fields like vendor, total, and dates. It handles multiple formats and layouts automatically.

---

**Q5. Correct: C**

15,000 words × 1.3 tokens/word = 19,500 tokens, which exceeds the 8,192 token context window. Chunking the document into smaller segments (each under ~6,000 tokens to leave room for the prompt and output), summarizing each chunk, then combining or further summarizing the results is the standard approach. This is a common pattern in document processing with LLMs.

---

**Q6. Correct: C**

Transparency requires that AI systems be understandable and that their capabilities, limitations, and decision-making processes be clear to users. For an AI agent with significant permissions (executing trades, accessing financial data), users must understand what the agent can and cannot do, what data it accesses, and how it operates. This enables informed consent and appropriate trust calibration.

---

**Q7. Correct: D**

Document intelligence is specifically designed for extracting structured information from documents including forms, invoices, and medical records. It combines OCR with understanding of document structure and entity extraction to identify specific fields like names, dates, and medication information from both printed and handwritten sources.

---

**Q8. Correct: B**

Fairness in responsible AI specifically requires testing models across different demographic groups (gender, age, ethnicity, etc.) to ensure the system doesn't discriminate or produce biased outcomes. This directly addresses fairness by identifying and measuring disparate impact across protected groups.

---

**Q9. Correct: B**

Hallucination is when generative AI models confidently generate information that sounds plausible but is factually incorrect. The model created a specification (128GB RAM) that doesn't exist in the source data, which is the textbook definition of LLM hallucination - a key limitation tested on AI-901.

---

**Q10. Correct: B**

Computer vision workloads handle image-based tasks including object detection (identifying what items are in the photo) and image similarity (finding visually similar products). This is a classic visual search scenario that requires analyzing image content and matching it against a product catalog.

---

**Q11. Correct: C**

Inclusiveness in responsible AI means designing AI systems that are accessible to all users regardless of language, disability, or technical capability. Supporting multiple languages and accessibility technologies like screen readers ensures the chatbot can serve diverse user populations.

---

**Q12. Correct: A**

Tokens in LLMs are sub-word units that don't map 1:1 to words. Common words might be one token, but uncommon words, technical terms, or words in non-English languages often split into multiple tokens. A 450-word prompt becoming 600 tokens (roughly 1.3 tokens per word) is typical tokenization behavior.

---

**Q13. Correct: A**

Document intelligence (Azure AI Document Intelligence) is specifically designed to extract structured information from documents including forms, invoices, and medical records. It combines OCR with entity extraction to identify and extract specific fields like names, dates, and custom entities from scanned documents.

---

**Q14. Correct: D**

Fairness in Responsible AI requires that AI systems treat all groups of people equitably and identify and mitigate bias. Evaluating model performance across demographic groups and addressing disparities directly implements fairness by ensuring the system doesn't discriminate against protected classes.

---

**Q15. Correct: A**

Hallucination is when generative AI models generate plausible-sounding but factually incorrect or nonsensical information. This is a well-known limitation of LLMs and SLMs where the model generates responses based on statistical patterns rather than verified facts.

---

**Q16. Correct: A**

Speech recognition converts the audio recordings to text, and natural language processing with sentiment analysis evaluates the emotional tone (frustration, satisfaction) in that text. This combination directly addresses analyzing call recordings for emotional content.

---

**Q17. Correct: B**

Tokens are the fundamental units that LLMs process. Text is broken down into tokens (which can be whole words, parts of words, or characters) before processing. Both input prompts and generated completions are measured and limited in tokens.

---

**Q18. Correct: A**

Loan decisions significantly impact people's lives and are subject to regulatory requirements. Transparency (explainability of why a loan was approved or denied) and accountability (clear governance and ability to appeal/review decisions) are the most critical Responsible AI principles for high-stakes financial decisions.

---

**Q19. Correct: A**

Fairness requires AI systems to treat all groups equitably and not produce biased outcomes. When the system performs worse for elderly patients due to their different bone density characteristics, it creates unfair treatment across age demographics, potentially leading to missed diagnoses in one group. This directly violates the fairness principle by producing discriminatory outcomes based on demographic factors.

---

**Q20. Correct: D**

A single-agent solution with RAG is specifically designed for this scenario. It maintains conversation context, grounds responses in the company knowledge base, and provides consistent answers by retrieving relevant information before generating responses. This is the core pattern for building knowledge-based chatbots in Azure AI Foundry.

---

**Q21. Correct: A**

Azure AI Language provides both sentiment analysis (positive/negative/neutral classification) and key phrase extraction (identifying product names and issues) in a single service. This directly addresses both requirements stated in the scenario.

---

**Q22. Correct: C**

Writing effective system prompts is a core AI-901 skill. The system prompt should include specific role definition, tone/style guidelines, and examples of desired response format. This is the standard approach to align model behavior with organizational requirements without changing the model or parameters unnecessarily.

---

**Q23. Correct: B**

Azure AI Speech speech-to-text is the dedicated service for converting audio to text. It handles various audio formats including WAV, supports speaker diarization for multiple speakers, and is optimized for speech recognition tasks.

---

**Q24. Correct: C**

Azure Computer Vision provides pre-trained image classification models that can categorize images into standard categories without requiring custom training. This matches the requirement to work 'without training a custom model'.

---

**Q25. Correct: A**

Azure Content Understanding is specifically designed for extracting structured information from unstructured documents, forms, and content with varying layouts. It handles the complexity of different document formats and intelligently extracts fields without requiring standard templates.

---

**Q26. Correct: D**

The Foundry portal's chat playground is designed exactly for this: pick a deployed model, type a system prompt, chat with it, and tune parameters like temperature - all without writing code.

---

**Q27. Correct: A**

Azure AI Language (part of Azure AI services accessible through Foundry) provides both sentiment analysis to determine positive/negative/neutral tone and key phrase extraction to identify main topics. These two features working together directly address both requirements for text analysis.

---

**Q28. Correct: A**

Input tokens (system prompt 450 + user prompt 200 = 650) are charged at $0.03/1k = $0.0195. Output tokens (350) are charged at $0.06/1k = $0.021. Total cost is $0.0195 + $0.021 = $0.0405. Input and output tokens are billed separately at different rates.

---

**Q29. Correct: B**

Azure Content Understanding (formerly Form Recognizer/Document Intelligence) is specifically designed for extracting structured data from documents, forms, and invoices. Custom extraction models can be trained to identify specific fields like product names, prices, and dates across various document formats and layouts.

---

**Q30. Correct: D**

For image generation models like DALL-E in Azure AI Foundry, detailed visual requirements and style guidance should be in the user prompt (the actual generation request) using specific, descriptive keywords. Image generation models respond better to detailed user prompts than system-level instructions. System prompts are less effective for controlling image generation parameters.

---

**Q31. Correct: B**

This workflow correctly chains the services: (1) Azure AI Speech's speech-to-text converts the incoming English audio to text, (2) Azure AI Translator translates the text to the target language, (3) Azure AI Speech's text-to-speech synthesizes the translated text into spoken audio for the customer. This is the standard pattern for real-time speech translation.

---

**Q32. Correct: B**

Grounding means retrieval: connecting the company documents as a data source makes the model answer from retrieved passages, and the system prompt instruction ('answer only from the provided context, otherwise say you don't know') constrains behavior - the standard retrieval-augmented pattern in Foundry.

---

**Q33. Correct: D**

Azure AI Language provides pre-built named entity recognition with a specialized healthcare model that identifies medical entities like medications, dosages, conditions, and treatments from unstructured text. This is purpose-built for this exact scenario.

---

**Q34. Correct: D**

Azure AI Custom Vision is specifically designed for training custom image classification and object detection models with user-provided labeled images. With 5,000 labeled images across 15 categories, this is the ideal use case for Custom Vision.

---

**Q35. Correct: C**

This is the correct two-step process: Azure AI Speech service provides speech-to-text transcription for audio files, and Azure AI Language service provides sentiment analysis for text. These are separate but complementary services designed to work together in this exact scenario.

---

**Q36. Correct: C**

Azure AI Document Intelligence (formerly Form Recognizer) includes pre-built models specifically for invoices that extract structured fields like vendor name, invoice number, amounts, dates, and line items. This handles multiple formats and provides structured JSON output without custom parsing code.

---

**Q37. Correct: D**

System prompts are the primary mechanism for controlling model behavior and enforcing policies. Strengthening the system prompt with explicit instructions, examples of proper refusals, and clear directive language (e.g., 'You must never provide medical diagnoses') is the most effective way to ensure consistent policy adherence across all conversations.

---

**Q38. Correct: C**

System prompts define the assistant's persona, constraints, and behavior rules. Setting clear boundaries in the system prompt (e.g., 'You are a technical support assistant. Only answer questions about product features and troubleshooting. Politely decline questions about other topics.') is the direct and effective way to control model behavior across all conversations.

---

**Q39. Correct: C**

Azure AI Language provides built-in sentiment analysis and key phrase extraction that automatically detects and processes over 100 languages including Spanish, French, and German. A single API call can handle multilingual text without language-specific configuration, returning sentiment scores (positive/negative/neutral/mixed) and extracted key phrases for each document.

---

**Q40. Correct: B**

Custom Vision is specifically designed for training custom image classification models. With 5,000 labeled images, the company can train a classification model that assigns images to their predefined categories. The service handles model training, evaluation, and deployment through the Azure AI Foundry portal or API.

---

**Q41. Correct: C**

Function calling allows agents to invoke external APIs and tools during conversation. The agent can determine when to call a 'check_availability' function with date/time parameters, receive real-time data from the scheduling API, and use that information to respond to the user. This is the standard pattern for connecting agents to live external systems.

---

**Q42. Correct: C**

Azure AI Content Understanding (formerly part of Document Intelligence) is purpose-built for structured data extraction from documents with varying layouts. You can train custom models to identify and extract specific fields from contracts, invoices, forms, and other documents, handling different formats and templates. It combines layout understanding with field extraction capabilities.

---

**Q43. Correct: A**

Retrieval-Augmented Generation (RAG) solves this exact scenario: grounding model responses in specific company documentation. The pattern involves indexing the SharePoint content (using Azure AI Search or similar), retrieving relevant documents based on the user query, and including that retrieved content in the prompt context. This gives the model current, accurate information to base its answers on rather than relying on general training data.

---

**Q44. Correct: D**

The correct implementation uses a system prompt to establish behavior and policies (persistent instructions), while passing conversation history as part of the messages array in each API call. This is the standard pattern for chat applications using Azure OpenAI - the system message defines the assistant's behavior, and the conversation history (alternating user/assistant messages) provides context. Temperature=0 helps consistency but doesn't maintain context across turns.

---

**Q45. Correct: D**

Azure Content Understanding (formerly Document Intelligence/Form Recognizer) is specifically designed for extracting structured information from documents and forms with varying layouts. Custom models can be trained on clinic-specific forms to recognize fields, checkboxes, and handwritten content accurately. This service handles both OCR and intelligent field extraction in one solution, making it the purpose-built tool for this scenario.

---

