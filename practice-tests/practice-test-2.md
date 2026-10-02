# Practice Test 2: AI-901: Azure AI Fundamentals Exam Prep with Foundry

- **Questions:** 45
- **Time limit:** 90 minutes
- **Passing score:** 70%%

> Answers are in `answer-key-2.md`. Track results in `score-tracker.md`.

---

**Q1.** A healthcare provider is deploying an AI system to analyze patient X-ray images for potential abnormalities. The system occasionally flags healthy tissue as abnormal, requiring radiologists to review false positives. Which responsible AI principle is MOST directly challenged when the system disproportionately generates false positives for patients with darker skin tones due to training data imbalance?

A) Transparency, because the model's decision-making process is not explainable to medical staff
B) Fairness, because the system produces unequal accuracy across different demographic groups
C) Reliability and safety, because any false positive represents a system malfunction
D) Privacy and security, because patient demographic data is being used in the analysis

---

**Q2.** A financial services company needs to build an AI solution that analyzes quarterly earnings call transcripts to extract key financial metrics, sentiment trends, and regulatory compliance risks mentioned by executives. The solution must process both the spoken audio and presentation slides simultaneously. Which combination of AI workloads BEST addresses this scenario?

A) Generative AI to summarize the entire call, computer vision to read slide text, and document intelligence for compliance detection
B) Natural language processing for transcript analysis and computer vision for optical character recognition on slides
C) Speech recognition combined with a multimodal generative AI agent that processes both audio and visual inputs
D) Speech recognition to transcribe audio, document intelligence to extract data from slides, and natural language processing to analyze sentiment and entities

---

**Q3.** An AI development team is evaluating whether to use a large language model (LLM) or a small language model (SLM) for a customer service chatbot that will run on mobile devices with limited connectivity. The chatbot needs to handle common product questions with 80% accuracy but must respond within 2 seconds and work offline. Which factor MOST strongly favors selecting an SLM over an LLM for this scenario?

A) SLMs require fewer tokens per prompt, reducing the cost per API call to the cloud service
B) SLMs have smaller parameter counts enabling local deployment on mobile devices without cloud connectivity
C) SLMs are trained on more recent data and will provide more current product information
D) SLMs use simpler transformer architectures that are easier to fine-tune for customer service

---

**Q4.** A legal firm is implementing a generative AI system to draft contract summaries from 50-page lease agreements. During testing, the system occasionally includes clauses that don't exist in the source document. The firm implements a solution where the AI must cite specific page numbers for every statement in the summary and retrieves relevant contract sections before generating each summary paragraph. Which term BEST describes this mitigation approach?

A) Prompt engineering with few-shot learning examples
B) Fine-tuning the model on domain-specific legal documents
C) Implementing transparency through explainable AI techniques
D) Grounding the model with retrieval-augmented generation

---

**Q5.** A manufacturing company wants to deploy an AI agent that monitors production line cameras, detects equipment anomalies, retrieves maintenance manuals from a database, and automatically generates work orders with repair instructions. The solution must coordinate multiple steps: analyzing visual input, making decisions based on historical data, and producing structured output. Which statement BEST describes why an AI agent architecture is appropriate for this scenario compared to a single-purpose AI model?

A) Agents use larger language models than single-purpose systems, providing better accuracy for complex manufacturing scenarios
B) Agents can execute multi-step workflows by orchestrating different AI models and tools, making autonomous decisions about which actions to take based on intermediate results
C) Agents store conversation history longer than standard models, enabling them to remember equipment issues across multiple production shifts
D) Agents are specifically designed for computer vision tasks and are more accurate than traditional object detection models

---

**Q6.** A university is developing an AI-powered admissions assistant that answers prospective student questions about programs, requirements, and campus life. During compliance review, legal counsel requires that every AI response include a mechanism for students to understand what information influenced the answer and a way to challenge potentially incorrect information. Which responsible AI principle is the legal requirement MOST directly enforcing?

A) Accountability, because the university must be able to defend decisions made by the AI system
B) Inclusiveness, because all students must have equal ability to access and question information
C) Reliability and safety, because incorrect admissions information could harm student outcomes
D) Transparency, because users must be able to understand how the system reached its outputs

---

**Q7.** A healthcare startup is building an AI system to analyze patient X-ray images and provide diagnostic suggestions to radiologists. The system occasionally identifies abnormalities that aren't present, and the team wants to ensure radiologists understand how the AI reached its conclusions. Which Responsible AI principle is MOST critical to address both concerns?

A) Fairness, by ensuring the model performs equally well across all patient demographics and medical conditions
B) Inclusiveness, by training the model on X-ray data from diverse patient populations and medical facilities
C) Privacy and security, by implementing encryption for patient data and ensuring HIPAA compliance throughout the diagnostic process
D) Transparency, by providing explainability features that show which image regions influenced the AI's decision and documenting known limitations including false positive rates

---

**Q8.** A financial services company needs an AI solution to extract structured data from thousands of mortgage application PDFs that vary in format—some are scanned images, others are digital forms, and layouts differ by year and region. The extracted data must populate a database for compliance review. Which AI workload BEST fits this requirement?

A) Computer vision with custom object detection to identify form fields and their values across different document layouts
B) Natural language processing with named entity recognition to identify financial terms and applicant information in the text
C) Generative AI with prompt engineering to read documents and output structured JSON data for each mortgage application
D) Document intelligence with form recognition to extract key-value pairs, tables, and structured data from varying document formats

---

**Q9.** An AI development team is fine-tuning a small language model (SLM) for a customer service chatbot that will run on-premises due to data residency requirements. During testing, they notice the model performs well on common queries but generates plausible-sounding but incorrect responses when asked about recent product updates released after the model's training cutoff date. What is the PRIMARY limitation being demonstrated, and what is the recommended mitigation?

A) Hallucination due to knowledge cutoff—implement retrieval-augmented generation (RAG) to ground responses in current product documentation
B) Token limit exceeded—implement conversation truncation and summarization to stay within the model's context window for longer conversations
C) Insufficient embedding quality—retrain the model with higher-dimensional embeddings to better capture semantic relationships in product queries
D) Transformer architecture constraint—switch to a larger language model (LLM) with more parameters to improve factual accuracy

---

**Q10.** A global e-learning platform is implementing speech-to-text capabilities to auto-generate captions for educational videos in multiple languages. During internal testing, the system performs well on standard accents but shows significantly lower accuracy for speakers with regional accents and speech patterns. Which combination of Responsible AI principle and technical approach BEST addresses this issue?

A) Reliability and safety—implement confidence thresholds to reject low-accuracy transcriptions and route them to human transcriptionists instead of showing incorrect captions
B) Accountability—establish clear ownership for caption quality and implement a feedback mechanism where users can report transcription errors for continuous improvement
C) Inclusiveness—expand training data to include diverse speech patterns, accents, and dialects, and test model performance across demographic groups to ensure equitable accuracy
D) Fairness—apply demographic parity constraints during model training to ensure equal false positive rates across different speaker accent groups

---

**Q11.** A manufacturing company wants to implement predictive maintenance by analyzing equipment sensor data, maintenance logs, and operator notes to predict failures. The solution needs to identify patterns in time-series sensor readings, extract insights from unstructured maintenance text, and generate maintenance recommendations. Which combination of AI workloads is required?

A) Machine learning for time-series anomaly detection in sensor data, natural language processing for extracting entities and sentiment from maintenance notes, and generative AI for recommendation generation
B) Computer vision for sensor data pattern analysis, natural language processing for maintenance log analysis, and generative AI for creating maintenance recommendations
C) Document intelligence for processing maintenance logs, speech recognition for operator voice notes, and generative AI agents to orchestrate the predictive maintenance workflow
D) Natural language processing for all text analysis, computer vision for equipment image inspection, and a rule-based system for generating maintenance schedules based on extracted patterns

---

**Q12.** An AI engineer is configuring a generative AI solution using Azure OpenAI Service for a legal research application. The application needs to summarize case law documents (averaging 50,000 words each) and answer specific questions about legal precedents. During initial testing with a GPT-4 model, the engineer notices that longer documents result in incomplete summaries and the model seems to 'forget' information from early sections when answering questions. What is the MOST likely cause and appropriate solution?

A) The transformer architecture's attention mechanism is degrading—switch to a model with sparse attention patterns that can handle longer sequences more efficiently without losing context from distant tokens
B) Embedding quality is insufficient for long documents—increase the embedding dimensions and use hierarchical embeddings to better capture the document's semantic structure across all sections
C) The model's token limit is being exceeded—implement a chunking strategy to process the document in segments with overlap, then use a map-reduce pattern to combine summaries and implement retrieval-augmented generation for question answering
D) The model lacks sufficient parameters for complex legal reasoning—deploy a larger LLM with more parameters to improve memory capacity and comprehension of lengthy legal documents

---

**Q13.** A healthcare startup is building an AI system to analyze patient X-ray images and provide preliminary assessments to radiologists. The system occasionally flags healthy patients as having potential issues, requiring additional manual review. According to responsible AI principles, which approach BEST addresses the primary concern while maintaining system utility?

A) Implement transparency measures by providing confidence scores and highlighting which image regions influenced the AI's decision, allowing radiologists to make informed judgments
B) Reduce the sensitivity threshold to minimize false positives, even if this means some actual conditions might be missed
C) Remove human radiologist review since the AI system can process images faster and more consistently
D) Focus solely on privacy by encrypting all patient data and removing identifying information from X-rays

---

**Q14.** A company plans to deploy a generative AI solution using Azure OpenAI Service. The solution will generate product descriptions based on technical specifications. During testing, the model occasionally generates descriptions that include features not present in the input specifications. Which combination of techniques BEST mitigates this issue?

A) Use a smaller language model with fewer parameters to reduce computational complexity and processing time
B) Increase the temperature parameter to 1.5 to generate more creative and diverse product descriptions
C) Fine-tune the model on a dataset of competitor product descriptions to improve output quality
D) Implement grounding by providing the model with retrieved product specification documents and configure system messages that instruct the model to only use provided information

---

**Q15.** An international e-commerce platform needs to implement an AI workload that can process customer service emails in multiple languages, extract key information such as order numbers and complaint categories, and route them to appropriate departments. Which AI workload combination BEST fulfills these requirements?

A) Computer vision for reading email text combined with generative AI for creating routing decisions
B) Speech processing for audio transcription combined with sentiment analysis for prioritization
C) Natural language processing for language understanding and information extraction combined with document intelligence for structured data extraction
D) Conversational AI agents for automated email responses combined with computer vision for attachment analysis

---

**Q16.** A financial services company is evaluating whether to use a large language model (LLM) or a small language model (SLM) for an internal tool that helps employees draft compliant responses to common regulatory inquiries. The tool will run on employee workstations and must process requests within 2 seconds while handling domain-specific financial terminology. Which factor MOST strongly favors choosing an SLM over an LLM for this scenario?

A) SLMs are always more accurate than LLMs when fine-tuned on domain-specific financial data
B) SLMs have larger context windows that can accommodate longer regulatory documents
C) SLMs provide better protection against prompt injection attacks in financial applications
D) SLMs require significantly less computational resources and can run efficiently on local workstations while meeting the 2-second latency requirement

---

**Q17.** A retail company wants to implement an AI solution that allows customers to take photos of items in-store and receive instant information about similar products, pricing, and availability. The solution must work offline in areas with poor connectivity. Which AI workload is MOST appropriate for the core image recognition functionality?

A) Computer vision to identify and classify objects in the photographs
B) Document intelligence to extract product information from the captured images
C) Generative AI to create descriptions of the items in the images
D) Natural language processing to interpret customer queries about the products

---

**Q18.** A government agency is deploying an AI system to help process disability benefit applications. During testing, the system shows a pattern of recommending approval for applications from certain demographic groups at higher rates than others, even when application details are similar. Which responsible AI principle is MOST directly violated, and what should be the priority action?

A) Inclusiveness is violated; priority action is to ensure the system interface is accessible to people with disabilities using screen readers and keyboard navigation
B) Accountability is violated; priority action is to establish a governance board to review all AI decisions before they are finalized
C) Fairness is violated; priority action is to audit the training data and model for demographic bias, then retrain with balanced data or adjust decision thresholds across groups
D) Privacy and security is violated; priority action is to implement stronger encryption for applicant demographic information

---

**Q19.** A healthcare organization is deploying an Azure AI solution that analyzes patient symptoms described in natural language and suggests possible diagnoses for physicians to review. During testing, the system occasionally suggests diagnoses that are not supported by the symptoms described, and in one case suggested a diagnosis more common in a different demographic group than the patient's actual demographic. Which two Responsible AI principles are MOST directly violated by these observed behaviors?

A) Reliability and safety, because the system produces unsupported suggestions; and inclusiveness, because it may not perform equally across demographic groups
B) Transparency, because patients cannot see how diagnoses are generated; and accountability, because no physician reviews the suggestions
C) Fairness, because suggestions vary between patients; and privacy and security, because symptom data is being processed
D) Reliability and safety, because the system requires physician review; and transparency, because the AI model's architecture is not disclosed

---

**Q20.** A developer is building a customer support agent using Azure AI Foundry and needs to ensure the agent stays focused on troubleshooting product issues and never discusses competitor products. The agent should politely redirect users who ask about competitors. Which approach BEST implements this requirement?

A) Configure content filters in the deployment settings to block competitor brand names from appearing in responses
B) Include explicit instructions in the system prompt defining the agent's role boundaries and providing a sample redirect response for competitor questions
C) Deploy the model with a lower temperature setting (0.1) to reduce creative responses about competitors
D) Use prompt shields in Azure AI Content Safety to detect and block jailbreak attempts related to competitor discussion

---

**Q21.** An application uses Azure AI Language service to analyze customer feedback in English, Spanish, and French. The application extracts key phrases from each review. A developer notices that key phrase extraction returns different numbers of phrases for semantically similar reviews in different languages. What explains this behavior?

A) The service converts all text to English before extraction, and translation quality affects the number of phrases detected
B) Key phrase extraction uses language-specific models that identify culturally relevant phrases, so phrase counts naturally vary across languages even for similar content
C) Different languages have different default confidence thresholds, causing some phrases to be filtered out in certain languages
D) The service is incorrectly configured - key phrase extraction should return identical phrase counts for semantically equivalent text across languages

---

**Q22.** A company is building a document processing pipeline using Azure AI Document Intelligence (formerly Form Recognizer). They need to extract tables, handwritten text, and specific labeled fields from mixed-format invoices. The invoices come from 15 different vendors with varying layouts. Which solution approach is MOST cost-effective while maintaining accuracy?

A) Use the prebuilt invoice model for all vendors, then apply custom post-processing rules to handle layout variations
B) Train a custom neural model using 500+ labeled invoice samples from all 15 vendors combined into a single model
C) Deploy 15 separate custom template models, one trained specifically for each vendor's invoice format
D) Use the Read API for OCR, then extract fields using regex patterns and table coordinates for each vendor format

---

**Q23.** A mobile app allows users to take photos of food items and receive nutritional estimates. The app must identify specific food items in the image (e.g., 'apple', 'chicken breast', 'rice'). Which Azure AI Vision capability should the developer implement?

A) Deploy a custom image classification model in Azure AI Vision, trained on a dataset of individual food images with single-item labels
B) Train a custom object detection model in Azure AI Vision with bounding boxes labeled for each food category
C) Use the dense captioning feature to generate detailed descriptions of all food items visible in the image
D) Use the prebuilt product recognition feature to identify food items from the general product catalog

---

**Q24.** A developer is building a real-time customer service application where users speak in various languages. The application must detect the language automatically, transcribe the speech to text, then translate to English for agent review. Using Azure AI Speech and Translator services, which implementation provides the LOWEST latency?

A) Enable auto-detect language with Speech-to-Text, then use the speech translation feature to output translated text directly in English
B) Use Speech-to-Text with automatic language detection, then send the detected language and transcribed text to Azure Translator for translation to English
C) Use Speech-to-Text with a multi-language model configured for all supported languages, then apply Language Detection service before translation
D) Record the audio, use Language Detection on a text sample to identify language, then configure Speech-to-Text with the detected language before translating

---

**Q25.** A healthcare application uses Azure AI Vision for facial detection in patient photos to assist with identity verification during telehealth appointments. The development team must ensure HIPAA compliance. Which statement about implementing facial detection for this scenario is correct?

A) Facial detection can be used with Azure AI Vision, but the application must not store or persist the face rectangle coordinates returned by the service
B) Facial detection returns only bounding box coordinates and detected attributes (glasses, blur, etc.) without creating facial signatures, so it can be used if the images are encrypted in transit and at rest
C) HIPAA requires Limited Access approval for any facial recognition scenario - facial detection cannot be used without Microsoft reviewing and approving the use case
D) Facial detection must be disabled for healthcare applications - only general object detection can be used to verify patient presence in the video frame

---

**Q26.** A developer is building a chat application using Azure OpenAI Service through the Foundry portal. The application must maintain conversation history and respond differently based on whether the user is a technical expert or a beginner. Which prompt engineering approach BEST achieves this requirement?

A) Include the user's expertise level in each user message and rely on the model to infer the appropriate response style
B) Create a system message that defines the assistant's behavior based on user expertise level, then pass conversation history with each API call
C) Use different deployed model instances for each user type and route requests based on a pre-screening question
D) Store the expertise level in the deployment configuration and create separate deployments for technical and beginner users

---

**Q27.** An insurance company needs to extract policyholder names, policy numbers, claim amounts, and dates from thousands of scanned claim forms that vary in layout and format. The solution must handle both typed and handwritten text. Which Azure AI service combination provides the MOST efficient solution?

A) Azure AI Vision for OCR, then Azure OpenAI Service to parse the extracted text into structured fields
B) Azure AI Language entity recognition on text extracted by Azure AI Vision OCR
C) Azure AI Document Intelligence with a custom extraction model trained on sample claim forms
D) Azure Content Understanding with pre-built document models for insurance claims

---

**Q28.** A retail company is developing a product recommendation agent using Azure OpenAI. The agent must access real-time inventory data from a SQL database before making recommendations. During testing, the agent sometimes recommends out-of-stock items. What is the BEST way to ensure the agent only recommends available products?

A) Implement function calling to query the inventory database in real-time when generating recommendations
B) Include current inventory data in the system message and update it every 5 minutes
C) Fine-tune the model with recent inventory snapshots to teach it current stock levels
D) Use retrieval-augmented generation (RAG) with a vector database containing daily inventory snapshots

---

**Q29.** A company needs to analyze customer support call recordings to identify negative sentiment, extract the main topic of each call, and detect mentions of competitor names. The solution must process audio files in English, Spanish, and French. Which implementation approach BEST meets these requirements?

A) Use Azure AI Speech batch transcription with sentiment analysis enabled, then use Azure OpenAI to identify topics and competitor mentions from the transcription
B) Deploy three separate Azure AI Speech models (one per language) for transcription, then use Azure AI Vision to analyze the transcript text for sentiment and entities
C) Use Azure AI Language speech analytics to process audio directly for sentiment and topic extraction without separate transcription
D) Use Azure AI Speech to transcribe calls to text, then Azure AI Language for sentiment analysis, key phrase extraction, and named entity recognition with custom entity categories for competitors

---

**Q30.** A manufacturing company is building a quality control system that must detect 12 specific types of product defects from assembly line camera images. The system needs 95%+ accuracy and must be deployed within 2 weeks. The company has 300 labeled images per defect type. Which approach BEST meets these requirements?

A) Train a custom Azure AI Vision image classification model using the 3,600 labeled images
B) Use Azure AI Vision's pre-built product recognition model and map detected products to defect categories
C) Deploy GPT-4 Turbo with Vision through Azure OpenAI and provide defect examples in the prompt
D) Build a custom object detection model using Azure Machine Learning with TensorFlow

---

**Q31.** A legal firm needs to process contracts to identify and redact personal information (names, addresses, phone numbers, Social Security numbers) before sharing documents with third parties. The solution must preserve the original document layout and formatting. Which Azure AI capability provides the MOST appropriate solution?

A) Azure AI Language PII detection with custom entity types, then programmatically replace detected entities in the original document
B) Azure AI Vision OCR to extract text, Azure AI Language for PII detection, then reconstruct the document with redactions
C) Azure OpenAI GPT-4 to identify PII in document text and return a redacted version maintaining original formatting
D) Azure AI Document Intelligence with PII redaction enabled to detect and visually redact sensitive information

---

**Q32.** A developer is building a chat application using Azure OpenAI Service through Microsoft Foundry. The application must maintain conversation history and provide contextually relevant responses across multiple turns. The developer writes the following system prompt: 'You are a helpful assistant.' Which implementation approach will BEST enable multi-turn conversations with proper context retention?

A) Store the entire conversation history in Azure Cosmos DB and retrieve all messages before each API call, passing them as a single concatenated user message
B) Set the temperature parameter to 0 and rely on the model's built-in memory to automatically recall previous conversation turns without passing message history
C) Use the messages array parameter in the API request, including previous user and assistant messages with their respective roles, and maintain a maximum token budget by removing oldest messages when needed
D) Create a new deployment for each conversation turn and use the deployment name to encode conversation state

---

**Q33.** A company processes customer support tickets in English, Spanish, and French. They need to detect sentiment and extract key phrases from each ticket regardless of language. The solution must minimize code complexity and API calls. Which Azure AI service configuration achieves this requirement MOST efficiently?

A) Call Azure AI Language sentiment analysis and key phrase extraction directly on the original text; these APIs automatically detect language and process content in 100+ languages without translation
B) Use Azure AI Translator to convert all text to English first, then call Azure AI Language sentiment analysis and key phrase extraction on the translated text
C) Deploy three separate Azure AI Language resources, one configured for each language, and route requests based on detected language
D) Use Azure OpenAI GPT-4 with a custom prompt asking it to return sentiment and key phrases in JSON format for all three languages

---

**Q34.** A developer is implementing speech-to-text functionality for a mobile application using Azure AI Speech service. The app must transcribe audio in real-time during live calls with minimal latency. Audio is captured at 16 kHz sample rate in WAV format. Which API method and configuration will BEST meet these requirements?

A) Use the batch transcription REST API to upload audio files to Azure Storage, then poll for transcription results every 5 seconds
B) Use the speech-to-text REST API with the audio file encoded as base64 in the request body, sending complete audio every 10 seconds
C) Use the Speech SDK with continuous recognition mode, establishing a WebSocket connection that streams audio chunks and receives transcription results asynchronously as speech is recognized
D) Use the Speech SDK with single-shot recognition mode, calling RecognizeOnceAsync() every 3 seconds with buffered audio segments

---

**Q35.** A retail company wants to extract product information (item name, price, quantity) from scanned invoices and receipts in various formats (PDF, JPG, PNG). Documents contain both printed and handwritten text. The solution must handle tables and multi-column layouts. Which Azure AI service provides the MOST appropriate pre-built capability for this scenario?

A) Azure AI Document Intelligence with the prebuilt-invoice model to extract structured fields including line items, totals, and vendor information automatically
B) Azure AI Vision OCR API to extract all text, then use regular expressions to parse item names, prices, and quantities from the extracted text
C) Azure OpenAI GPT-4 Vision to analyze document images and return extracted data in JSON format based on a custom prompt
D) Azure AI Custom Vision to train an object detection model that identifies and locates text regions, then extract text coordinates

---

**Q36.** A developer is building an agent using Microsoft Foundry that must access current weather data and company-specific product inventory to answer customer questions. The agent should decide when to use each data source. Which implementation approach aligns with Microsoft Foundry agent patterns?

A) Fine-tune a GPT model with weather and inventory data, then deploy the fine-tuned model to answer questions directly from learned data
B) Embed all weather and inventory data in the system prompt, refreshing the prompt every hour with updated data
C) Define functions/tools for get_weather(location) and check_inventory(product_id) in the agent configuration, allowing the model to call these functions based on user queries and receive results for response generation
D) Use Retrieval Augmented Generation (RAG) with a vector database containing both weather observations and inventory records, retrieving similar documents for each query

---

**Q37.** A developer deploys an Azure OpenAI GPT-4 model through Microsoft Foundry and tests image generation capabilities. The deployment fails when sending requests with image URLs in the messages array. The deployment configuration shows 'Model: gpt-4' and 'Version: 0613'. What is the MOST likely cause of this failure?

A) The deployment region does not support vision capabilities for GPT-4 models
B) The deployed model version (0613) is text-only; vision capabilities require GPT-4 with vision support (gpt-4-vision-preview or gpt-4-turbo versions that include vision)
C) Image URLs must be base64-encoded inline in the message content rather than passed as URL references
D) The API request is missing the required 'vision_enabled: true' parameter in the headers

---

**Q38.** A developer is building a chat application using Azure AI Foundry SDK. The application must maintain conversation history across multiple user turns and apply a system message that restricts responses to financial advice only. Which code pattern BEST implements this requirement?

A) Store conversation history in Azure Blob Storage and retrieve it before each API call, concatenating all messages into a single user prompt
B) Create a new client for each user message, passing the system message and full conversation history as a list of message objects with role and content properties
C) Use the streaming API with a stateful session object that automatically persists conversation context between calls
D) Pass only the latest user message to the API and rely on the model's built-in conversation memory to maintain context

---

**Q39.** An organization needs to extract key financial metrics (revenue, profit margin, fiscal quarter) from 10,000 quarterly earnings PDF reports with varying layouts. The solution must handle both structured tables and unstructured narrative text. Which Azure AI service combination provides the MOST appropriate solution?

A) Azure AI Vision for OCR followed by custom regex patterns to extract numeric values
B) Azure AI Language key phrase extraction API to identify financial terms
C) Azure Form Recognizer prebuilt invoice model to extract financial data
D) Azure Content Understanding with a custom extraction model trained on sample earnings reports

---

**Q40.** A retail company is deploying an object detection model in Azure AI Foundry to identify products on store shelves. During testing, the model achieves 92% precision but only 68% recall. The business requirement prioritizes detecting ALL products even if some false positives occur. What configuration change will BEST address this requirement?

A) Lower the confidence threshold from 0.5 to 0.3 to detect more potential objects
B) Increase the confidence threshold from 0.5 to 0.8 to reduce false detections
C) Retrain the model with data augmentation techniques to improve overall accuracy
D) Switch from object detection to image classification to simplify the prediction task

---

**Q41.** A customer service application uses Azure AI Language to analyze support ticket text. The application must detect negative sentiment AND extract specific complaint entities (product name, issue type, requested action) from the same text in a single API call. Which Azure AI Language feature combination achieves this with minimal API calls?

A) Call sentiment analysis API, then call named entity recognition API, then call key phrase extraction API separately
B) Use the text analytics for health API which combines sentiment and entity extraction
C) Submit a single request to the analyze text API with both sentiment analysis and entity recognition tasks enabled
D) Use a custom text classification model trained to output both sentiment labels and entity spans

---

**Q42.** A manufacturing company is building an agent in Azure AI Foundry that provides equipment maintenance guidance. The agent must access a vector database of maintenance manuals and retrieve relevant sections before generating responses. Which Azure AI Foundry agent component enables this retrieval pattern?

A) Include the entire vector database content in the system message as context
B) Configure a plugin that connects to the vector database and executes semantic search queries
C) Use function calling to trigger manual indexing of the database before each response
D) Deploy a fine-tuned model that has been trained on all maintenance manual content

---

**Q43.** A global e-learning platform needs to convert course audio lectures in English to text transcripts, then translate those transcripts into Spanish, French, and Mandarin. The solution must preserve technical terminology accurately and complete processing within 2 hours for a 90-minute lecture. Which implementation approach is MOST cost-effective while meeting requirements?

A) Use Azure AI Speech real-time transcription streaming API, then separately call Azure AI Language translation for each sentence
B) Deploy a multilingual speech recognition model that directly outputs transcripts in all four languages simultaneously
C) Use Azure AI Video Indexer to extract transcripts and translations in a single automated pipeline
D) Use Azure AI Speech batch transcription API for speech-to-text, then Azure AI Translator for each target language with custom glossaries for technical terms

---

**Q44.** A developer is building a customer support agent using Azure AI Foundry. The agent must maintain conversation context across multiple turns, remember customer preferences mentioned earlier in the chat, and route complex queries to human agents. The solution should minimize custom code while providing full control over the agent's behavior and knowledge sources. Which Azure AI Foundry capability should the developer use?

A) Deploy a GPT-4 model endpoint and implement conversation history management in the application code using the Foundry SDK
B) Use Azure AI Content Understanding to extract customer intent and route to pre-built response templates
C) Create an AI agent in Azure AI Foundry with custom instructions, conversation memory, and function calling for escalation logic
D) Configure Azure AI Speech service with custom voice profiles and integrate with Azure Bot Service for multi-turn dialogs

---

**Q45.** A healthcare application needs to extract patient information from thousands of handwritten medical forms that contain both printed text and checkboxes. The forms have inconsistent layouts, varying handwriting styles, and multiple languages. The extracted data must be structured into predefined fields (patient name, date of birth, diagnoses, medications) for database import. Which Azure AI Foundry solution provides this capability with the LEAST custom model training?

A) Azure Content Understanding with a custom extraction model trained on sample medical forms to identify and extract the specific fields
B) Azure AI Language custom named entity recognition (NER) model trained to identify medical entities in the extracted text
C) Azure AI Vision OCR to extract all text, then use GPT-4 deployed in Foundry with prompt engineering to structure the extracted text into JSON fields
D) Azure Form Recognizer prebuilt health insurance card model to extract patient demographic information from the forms

---

