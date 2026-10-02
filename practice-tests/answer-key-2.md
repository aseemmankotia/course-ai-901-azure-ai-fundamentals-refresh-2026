# Answer Key — Practice Test 2

**Q1. Correct: B**

Fairness directly addresses the requirement that AI systems produce equitable outcomes across different groups. When a model shows systematically different error rates for specific demographics due to biased training data, this is a core fairness violation requiring dataset rebalancing and validation across subgroups.

---

**Q2. Correct: D**

This scenario requires three distinct specialized workloads: speech (converting audio to text), document intelligence (structured extraction from presentation slides including tables and forms), and NLP (sentiment analysis, entity extraction, and understanding regulatory language). Each workload is purpose-built for its task, and combining them provides the most accurate and reliable solution.

---

**Q3. Correct: B**

The critical requirement is offline functionality with limited connectivity. SLMs typically have millions to low billions of parameters (vs. hundreds of billions for LLMs), making them small enough to deploy directly on mobile devices. This enables local inference without cloud API calls, meeting the offline and 2-second latency requirements. Edge deployment is the key architectural advantage of SLMs for this scenario.

---

**Q4. Correct: D**

Grounding with RAG (Retrieval-Augmented Generation) specifically addresses hallucination by retrieving relevant source content before generation and constraining the model to reference only retrieved information. Requiring page citations enforces grounding by making the model base responses on actual document content rather than generating plausible-sounding but fabricated clauses. This is the standard approach for reducing hallucination in document-based generative AI applications.

---

**Q5. Correct: B**

AI agents are characterized by their ability to autonomously plan and execute multi-step workflows, use tools (like database queries and work order systems), and make decisions about next actions based on intermediate results. This scenario requires orchestrating computer vision (anomaly detection), information retrieval (manual lookup), decision-making (severity assessment), and structured generation (work orders)—exactly what agent architectures are designed to handle through tool use and sequential reasoning.

---

**Q6. Correct: D**

Transparency specifically requires that AI systems provide understandable information about how they operate and how decisions are made. Requiring users to understand what information influenced responses and providing challenge mechanisms directly implements transparency—it makes the system's reasoning visible and verifiable. This allows users to assess trustworthiness and detect potential errors.

---

**Q7. Correct: D**

Transparency addresses both the hallucination concern (documenting limitations and false positive rates) and the need for radiologists to understand AI reasoning (explainability of which image features drove the conclusion). For medical AI, transparency enables human oversight and informed decision-making.

---

**Q8. Correct: D**

Document intelligence (Azure AI Document Intelligence) is specifically designed for this scenario—extracting structured data from documents with varying formats, handling both scanned and digital documents, recognizing forms, tables, and key-value pairs. This is a core document intelligence/information extraction workload.

---

**Q9. Correct: A**

The scenario describes hallucination—the model generates confident but incorrect responses about information outside its training data. RAG (grounding) is the standard mitigation, connecting the model to current documentation so responses are based on retrieved facts rather than potentially outdated training data.

---

**Q10. Correct: C**

Inclusiveness directly addresses the core issue—ensuring the AI system works for all users regardless of accent or speech pattern. The technical approach (diverse training data and performance testing across groups) is the correct method to achieve inclusive speech recognition that serves the global user base equitably.

---

**Q11. Correct: A**

This scenario requires: (1) ML for time-series sensor analysis—anomaly detection is a classic ML workload for numeric sensor data patterns, (2) NLP for unstructured text in maintenance logs—extracting entities and understanding context, and (3) Generative AI to synthesize insights and create maintenance recommendations in natural language.

---

**Q12. Correct: C**

At the conceptual level tested by AI-901, a 50,000-word document vastly exceeds typical token limits (roughly 75,000 tokens vs. common context windows of 8K-128K tokens depending on model). The described behavior (incomplete summaries, forgetting early content) is classic token limit exceeded behavior. Chunking + map-reduce + RAG is the standard architectural pattern for processing documents beyond context limits.

---

**Q13. Correct: A**

This scenario primarily involves reliability and safety (false positives requiring extra review) and requires transparency. Providing confidence scores and explainability (showing which regions influenced decisions) allows radiologists to understand and validate AI recommendations, maintaining safety while preserving utility. This aligns with Microsoft's responsible AI principles of transparency and reliability working together.

---

**Q14. Correct: D**

The issue described is hallucination - the model generating information not in the input. Grounding (providing relevant retrieved documents) and system message constraints directly address hallucination by anchoring the model to factual source material. This is the recommended approach in Azure OpenAI for reducing hallucinations in enterprise scenarios.

---

**Q15. Correct: C**

This scenario requires understanding multilingual text (NLP), extracting specific entities like order numbers and categories (information extraction - part of NLP and document intelligence capabilities), and classifying content for routing (also NLP). Document intelligence services handle structured information extraction from documents including emails. This combination directly maps to the described requirements.

---

**Q16. Correct: D**

The key requirement is running on employee workstations with 2-second latency. SLMs are specifically designed to be lightweight and efficient, requiring less memory and compute power, making them suitable for local deployment. LLMs typically require cloud infrastructure or powerful GPUs. The scenario's constraints (local execution, fast response) strongly favor SLM's resource efficiency.

---

**Q17. Correct: A**

The core requirement is identifying and recognizing objects (products) in photographs to find similar items - this is explicitly an image classification and object detection task, which is the domain of computer vision workloads. Computer vision can be deployed as edge models for offline scenarios.

---

**Q18. Correct: C**

The scenario explicitly describes different outcomes for different demographic groups with similar inputs - this is the definition of unfair bias. Fairness principle requires AI systems to treat all people equitably. The correct remediation is identifying the source of bias (training data, features, or model architecture) and correcting it through retraining, rebalancing data, or adjusting decision boundaries.

---

**Q19. Correct: A**

The scenario describes two distinct problems: (1) generating unsupported suggestions (hallucinations/unreliable outputs) directly violates reliability and safety principles, and (2) performing differently across demographic groups directly violates inclusiveness principles. These are the two most directly violated principles based on the observed behaviors.

---

**Q20. Correct: B**

System prompts are the primary mechanism for defining agent behavior, role boundaries, and response patterns. Including explicit instructions about what topics to avoid and how to redirect users is the most effective and reliable method. System prompts can provide specific examples like 'If asked about competitors, respond: I'm here to help with [Product] questions. For other products, please contact their support teams.'

---

**Q21. Correct: B**

Azure AI Language uses native language-specific models for key phrase extraction. Different languages have different grammatical structures, idiomatic expressions, and cultural contexts. A concept expressed in 2 words in English might require 4 words in French or be captured in a compound word in German. The models are trained to identify what constitutes a 'key phrase' in each language's natural structure, so output length variation is expected and correct behavior.

---

**Q22. Correct: A**

The prebuilt invoice model is trained on thousands of invoice variations and can handle most vendor layouts out-of-the-box. It automatically extracts common fields (invoice ID, dates, amounts, line items, tables) and handles handwriting. This is the most cost-effective option - no training data required, no training costs, immediate deployment. For the small percentage of fields it might miss due to unusual layouts, targeted post-processing is cheaper than training custom models.

---

**Q23. Correct: B**

Object detection is the correct capability because users will photograph plates with MULTIPLE food items simultaneously. Object detection identifies each item, draws bounding boxes around them, and classifies each one separately (e.g., one image might contain apple, rice, AND chicken). This is exactly what nutritional estimation needs - identify each distinct food item present. Custom training is needed because food recognition is domain-specific.

---

**Q24. Correct: A**

Speech translation (part of Azure AI Speech) performs speech recognition and translation in a SINGLE operation with auto-detect. It outputs translated text directly without needing a separate transcription→translation pipeline. This is the lowest latency option because it eliminates the round-trip to a separate Translator service call and processes both operations in the speech pipeline.

---

**Q25. Correct: B**

Facial DETECTION (detecting that a face exists and its location) is different from facial RECOGNITION/identification. Detection only returns rectangle coordinates and attributes - it doesn't create biometric templates or identify individuals. This can be used in HIPAA environments if the overall application meets compliance requirements (encryption, access controls, BAA with Microsoft, etc.). The detection itself doesn't create restricted biometric data.

---

**Q26. Correct: B**

System messages are specifically designed to set the assistant's behavior, tone, and context that persists across the conversation. Combined with maintaining conversation history in the messages array, this provides consistent, context-aware responses tailored to user expertise without requiring separate deployments or repeated context in every user message.

---

**Q27. Correct: C**

Azure AI Document Intelligence (formerly Form Recognizer) is purpose-built for structured data extraction from documents with varying layouts. Custom extraction models can be trained on sample forms to identify and extract specific fields (names, policy numbers, amounts, dates) from both typed and handwritten text, handling layout variations automatically—this is the most accurate and cost-effective solution for this scenario.

---

**Q28. Correct: A**

Function calling (tools) allows the model to invoke external functions/APIs during generation, enabling real-time database queries for current inventory. This ensures recommendations are based on live data at the moment of request, preventing out-of-stock recommendations—the only solution that guarantees real-time accuracy.

---

**Q29. Correct: D**

This is the correct multi-step pipeline: (1) Azure AI Speech transcribes multilingual audio to text (supports 100+ languages including English, Spanish, French); (2) Azure AI Language provides pre-built sentiment analysis, key phrase extraction (topics), and custom NER can be trained to detect competitor names. This uses the right service for each task at optimal cost.

---

**Q30. Correct: A**

Azure AI Vision Custom Vision allows training image classification models with as few as 50 images per class. With 300 images per defect type (3,600 total), this provides sufficient training data for high accuracy. The service handles model training, deployment, and provides a prediction API—achievable within 2 weeks with no ML expertise required. This is the purpose-built solution for custom image classification.

---

**Q31. Correct: D**

Azure AI Document Intelligence includes built-in PII detection and redaction capabilities that analyze document layout, identify PII entities, and return redacted documents (PDFs/images with PII blacked out) while preserving original formatting and layout. This single-service solution is purpose-built for document redaction scenarios.

---

**Q32. Correct: C**

The messages array is the standard mechanism for maintaining conversation context in Azure OpenAI Service. Each message includes a role (system, user, or assistant) and content. The API is stateless, so you must pass the full conversation history in each request. Token budget management is critical because context windows have limits (e.g., 4K, 8K, 128K tokens depending on model). This is the documented pattern in Microsoft Foundry SDK.

---

**Q33. Correct: A**

Azure AI Language sentiment analysis and key phrase extraction are multilingual APIs that automatically detect language and process content natively in the source language. They support 100+ languages without requiring translation. This is a single API call per operation, minimizing complexity and cost. The exam tests understanding that many Azure AI services are inherently multilingual.

---

**Q34. Correct: C**

Continuous recognition mode in the Speech SDK is designed for real-time scenarios. It maintains a persistent WebSocket connection, streams audio in small chunks (typically 100ms), and fires events as speech is recognized with very low latency. This is the standard pattern for live transcription, call centers, and real-time captioning applications. The exam tests recognition modes.

---

**Q35. Correct: A**

Azure AI Document Intelligence (formerly Form Recognizer) includes prebuilt models specifically designed for invoices and receipts. The prebuilt-invoice model automatically extracts structured data including line item tables (description, quantity, price), totals, dates, vendor info, and handles various layouts. It understands document structure, not just text. This is purpose-built for the scenario with no custom training required.

---

**Q36. Correct: C**

Function calling (tools) is the standard agent pattern in Microsoft Foundry and Azure OpenAI. You define functions with descriptions and parameters. The model intelligently decides when to call which function based on user intent, makes the call, receives real-time data, and incorporates it into the response. This enables agents to access live data and perform actions. The exam tests agent architecture patterns.

---

**Q37. Correct: B**

GPT-4 model versions have different capabilities. The original GPT-4 (versions like 0613) are text-only. Vision capabilities were introduced in specific versions like gpt-4-vision-preview and later incorporated into gpt-4-turbo and GPT-4o. Model version selection during deployment determines available capabilities. You cannot add vision to text-only model versions through configuration - you must deploy a vision-capable version. The exam tests model capability differences.

---

**Q38. Correct: B**

Azure AI Foundry SDK requires explicit conversation history management. You pass an array of message objects (each with 'role': 'system'/'user'/'assistant' and 'content') to the chat completion API. The system message sets behavior constraints, and including all prior messages maintains context. This is the standard pattern for multi-turn conversations.

---

**Q39. Correct: D**

Azure Content Understanding (part of Azure AI Foundry tooling) is designed for extracting structured data from documents with varying layouts. You can train a custom extraction model on labeled sample documents to identify specific fields (revenue, profit margin, quarter) across both tables and narrative text, handling layout variation automatically.

---

**Q40. Correct: A**

Recall measures the proportion of actual products detected (68% means 32% are missed). Lowering the confidence threshold causes the model to flag more detections, increasing recall (fewer missed products) at the cost of precision (more false positives). The business explicitly accepts false positives to avoid missing products, making this the correct trade-off.

---

**Q41. Correct: C**

Azure AI Language's analyze text API supports combining multiple tasks (sentiment analysis, entity recognition, key phrase extraction, language detection, PII detection) in a single request. You specify which tasks to run in the request payload, and the API returns all results together, minimizing latency and API calls.

---

**Q42. Correct: B**

Azure AI Foundry agents support plugins (also called tools or functions) that extend the agent's capabilities. A plugin can connect to external data sources like vector databases, execute semantic search based on the user query, retrieve relevant chunks, and inject them as context for the language model to generate grounded responses—this is the Retrieval Augmented Generation (RAG) pattern.

---

**Q43. Correct: D**

Batch transcription is optimized for pre-recorded audio files, processes asynchronously, and is more cost-effective than real-time streaming for non-interactive scenarios. Azure AI Translator supports custom glossaries to preserve technical terms accurately. This combination handles the 90-minute file well within 2 hours and minimizes cost compared to streaming or video indexing.

---

**Q44. Correct: C**

Azure AI Foundry agents provide built-in conversation memory, system instructions for behavior control, and function calling capabilities for external integrations (like escalation to human agents). This is the purpose-built solution for multi-turn conversational AI that minimizes custom code while maintaining full control over agent behavior and knowledge sources.

---

**Q45. Correct: C**

Azure AI Vision OCR handles handwriting, printed text, and multiple languages without training. Combining it with GPT-4 prompt engineering (both available in Foundry) requires zero custom model training—you simply prompt the LLM to structure the OCR output into the required JSON schema. This is the documented approach for variable-layout document processing in 2026 Foundry workflows.

---

