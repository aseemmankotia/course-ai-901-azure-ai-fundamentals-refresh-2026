# Practice Test 1: AI-901: Azure AI Fundamentals Exam Prep with Foundry

- **Questions:** 45
- **Time limit:** 90 minutes
- **Passing score:** 70%%

> Answers are in `answer-key-1.md`. Track results in `score-tracker.md`.

---

**Q1.** A healthcare provider wants to build a solution that analyzes patient X-ray images to detect potential abnormalities and flag cases for radiologist review. Which AI workload does this scenario BEST represent?

A) Natural language processing to extract medical terms from radiology reports
B) Computer vision to classify and detect patterns in medical images
C) Document intelligence to process structured patient intake forms
D) Generative AI to create synthetic X-ray images for training purposes

---

**Q2.** A company deploys an AI hiring assistant that screens resumes. During testing, the system consistently scores candidates from certain universities lower than others, even when qualifications are similar. Which Responsible AI principle is MOST directly violated?

A) Transparency, because candidates cannot see how scores are calculated
B) Accountability, because no human reviewer validates the AI decisions
C) Privacy and security, because resume data contains personal information
D) Fairness, because the system produces discriminatory outcomes based on educational background

---

**Q3.** An organization wants to build a chatbot that answers customer questions by retrieving information from their product documentation and support articles. The chatbot should provide accurate answers grounded in company knowledge. Which approach BEST addresses the risk of hallucination?

A) Increase the temperature parameter to 1.5 to generate more creative and diverse responses
B) Use retrieval-augmented generation (RAG) to ground responses in retrieved documentation before generating answers
C) Use a larger language model with more parameters to improve general knowledge
D) Fine-tune the model on thousands of general Q&A pairs from public datasets

---

**Q4.** A retail company wants to automatically extract product names, quantities, and prices from supplier invoices in various formats (PDF, scanned images, emails). Which AI workload is MOST appropriate for this scenario?

A) Document intelligence to extract structured information from business documents
B) Computer vision to detect objects and text regions in the invoice images
C) Speech recognition to convert invoice details into text format
D) Natural language processing to understand the meaning of invoice descriptions

---

**Q5.** A developer is building a text summarization feature using Azure OpenAI Service. The input document is 15,000 words. The model has a context window of 8,192 tokens. Assuming an average of 1.3 tokens per word, what is the BEST approach to handle this document?

A) Increase the max_tokens parameter to 20,000 to accommodate the full document
B) Use a higher temperature setting to compress the input more efficiently
C) Split the document into chunks that fit within the token limit and summarize each chunk separately, then combine summaries
D) Switch to a smaller language model (SLM) which requires fewer tokens

---

**Q6.** A financial services company is deploying an AI agent that provides investment advice to customers. The agent can execute trades, retrieve account balances, and access market data through API calls. Which Responsible AI principle requires that customers can easily understand what data the agent accesses and what actions it can perform on their behalf?

A) Inclusiveness, ensuring the agent is accessible to users with different abilities
B) Reliability and safety, ensuring the agent performs actions correctly without errors
C) Transparency, making the agent's capabilities and limitations clear to users
D) Fairness, ensuring the agent provides equitable advice to all customer segments

---

**Q7.** A healthcare provider wants to automatically extract patient information such as names, dates of birth, medication names, and dosages from handwritten doctor's notes and scanned prescription forms. Which AI workload is BEST suited for this requirement?

A) Computer vision with optical character recognition (OCR)
B) Natural language processing with named entity recognition
C) Generative AI with multimodal foundation models
D) Document intelligence with form processing and entity extraction

---

**Q8.** A company is developing an AI system to screen job applications. To ensure the principle of fairness is applied, which action should be prioritized during model development?

A) Encrypt all applicant data using Azure Key Vault during processing
B) Test the model across demographic groups to identify and mitigate selection bias
C) Provide detailed documentation explaining how the AI makes decisions
D) Implement multiple AI models and compare their outputs for consistency

---

**Q9.** When using a large language model (LLM) to generate product descriptions, the model produces a description claiming a laptop has 128GB of RAM when the actual specification is 16GB. Which limitation of generative AI does this demonstrate?

A) Token context window limitation preventing full specification review
B) Hallucination where the model generates plausible but incorrect information
C) Embedding dimension mismatch causing numerical errors
D) Insufficient prompt engineering leading to ambiguous outputs

---

**Q10.** A retail company wants to enable customers to search their product catalog using photos taken on smartphones. Customers should be able to photograph an item they like and find similar products in the company's inventory. Which AI workload addresses this requirement?

A) Speech recognition with intent classification
B) Computer vision with image similarity and object detection
C) Natural language processing with semantic search
D) Document intelligence with image classification

---

**Q11.** An organization is implementing an AI chatbot for customer service. To satisfy the inclusiveness principle of responsible AI, which approach should be taken?

A) Implement rate limiting to ensure all customers get equal response times
B) Store conversation logs in geo-redundant storage for disaster recovery
C) Design the chatbot to work across multiple languages and accessibility modes including screen readers
D) Use ensemble models to improve prediction accuracy across all queries

---

**Q12.** A developer is using Azure OpenAI Service and notices that a prompt containing 450 words is processed as approximately 600 tokens. What does this demonstrate about how large language models process text?

A) Tokens represent semantic meaning units and one word can map to multiple tokens depending on linguistic patterns
B) The model is allocating extra tokens for system instructions and response formatting overhead
C) Token count includes special characters, punctuation, and whitespace as separate tokens beyond the words
D) The embedding layer duplicates tokens to create higher-dimensional vector representations

---

**Q13.** A healthcare provider wants to automatically extract patient information such as names, dates of birth, medical record numbers, and diagnosed conditions from thousands of scanned paper medical records. Which AI workload is MOST appropriate for this scenario?

A) Document intelligence with form recognition and entity extraction
B) Computer vision with object detection
C) Natural language processing with sentiment analysis
D) Generative AI with a large language model

---

**Q14.** A company is deploying an AI system to screen job applications. To align with the Responsible AI principle of fairness, which action should the company take?

A) Train the model exclusively on data from the company's most successful employees to optimize for performance
B) Use a generative AI model to rewrite all applications in a standardized format before evaluation
C) Implement the model without human oversight to eliminate potential human bias from the process
D) Evaluate the model's performance across different demographic groups and mitigate any identified disparities in selection rates

---

**Q15.** An organization builds an AI chatbot that sometimes provides factually incorrect information presented as fact, despite being trained on accurate data. This is an example of which limitation of generative AI?

A) Hallucination
B) Token limit exhaustion
C) Context window overflow
D) Embedding dimensionality mismatch

---

**Q16.** A retail company wants to deploy an AI system that analyzes customer service call recordings to identify when customers express frustration or satisfaction. Which AI workload BEST fits this requirement?

A) Speech recognition combined with natural language processing for sentiment analysis
B) Computer vision with facial recognition
C) Document intelligence with layout analysis
D) Generative AI with prompt engineering for content creation

---

**Q17.** When working with a large language model (LLM), what are tokens?

A) Security credentials used to authenticate API requests to the model
B) Units of text (such as words or parts of words) that the model processes for input and output
C) Hyperparameters that control the creativity and randomness of model responses
D) Vector representations that capture semantic meaning of concepts

---

**Q18.** A financial institution is developing an AI model to approve loan applications. According to Responsible AI principles, which combination of principles is MOST critical to implement for this scenario?

A) Transparency and accountability - providing explanations for decisions and maintaining clear responsibility for outcomes
B) Inclusiveness and creativity - ensuring the interface works for all users and generates novel loan products
C) Performance optimization and cost efficiency - maximizing processing speed while minimizing compute costs
D) Data minimization and storage optimization - collecting minimal data and reducing database size

---

**Q19.** A healthcare company is developing an AI system to analyze patient X-ray images and flag potential abnormalities for radiologist review. The system occasionally misses subtle fractures in images of elderly patients due to bone density differences. Which Responsible AI principle is MOST directly violated in this scenario?

A) Fairness, because the system performs inconsistently across different demographic groups leading to potentially unequal healthcare outcomes
B) Transparency, because the system does not explain why certain images are flagged while others are not
C) Accountability, because there is no clear ownership of decisions made by the AI system
D) Privacy and security, because patient medical images are being processed by an automated system

---

**Q20.** A developer is building a customer service chatbot using Azure AI Foundry. The chatbot must maintain conversation context across multiple turns and provide consistent responses based on company policies stored in a knowledge base. Which Azure AI Foundry component should the developer implement?

A) A conversational language understanding model with custom intents
B) A prompt flow with multiple language models chained together
C) A custom vision model trained on company documentation
D) A single-agent solution with retrieval-augmented generation (RAG)

---

**Q21.** A company needs to analyze customer feedback emails to determine overall sentiment and extract key topics mentioned. The solution must identify whether feedback is positive, negative, or neutral, and extract specific product names and issues. Which Azure AI service combination provides this functionality?

A) Azure AI Language for sentiment analysis and key phrase extraction
B) Azure AI Speech for transcription and Azure OpenAI for summarization
C) Azure Computer Vision for text detection and Azure Form Recognizer for entity extraction
D) Azure Content Understanding for document analysis and Azure Translator for language detection

---

**Q22.** A developer deploys a GPT-4 model in Azure AI Foundry portal and writes the following system prompt: 'You are a helpful assistant.' User messages frequently receive generic responses that don't align with the company's technical support style. What is the BEST way to improve response quality?

A) Increase the temperature parameter to 1.5 for more creative responses
B) Switch to a different model deployment in a new Azure region
C) Enhance the system prompt with specific role definition, tone guidelines, and response structure examples
D) Add a user prompt before each message that repeats the instructions

---

**Q23.** An application needs to convert recorded customer support calls to text for analysis and quality assurance. The audio files are in WAV format, average 10 minutes in length, and contain multiple speakers. Which Azure AI service should be used?

A) Azure AI Language audio transcription API
B) Azure AI Speech speech-to-text service
C) Azure OpenAI Whisper model deployment
D) Azure Content Understanding audio extraction feature

---

**Q24.** A retail company wants to automatically categorize product images uploaded by sellers into predefined categories such as 'Electronics', 'Clothing', 'Home & Garden', and 'Sports'. The solution must work without training a custom model. Which Azure AI capability should be implemented?

A) Azure Custom Vision with a new classification project
B) Azure AI Vision object detection API
C) Azure Computer Vision image classification with a pre-trained model
D) Azure OpenAI GPT-4 Vision for image categorization

---

**Q25.** A legal firm needs to extract specific fields (contract date, party names, clauses) from thousands of scanned contract PDFs with varying layouts. The documents are unstructured and not in standard forms. Which Azure AI service is BEST suited for this task?

A) Azure Content Understanding to extract structured data from unstructured documents
B) Azure Computer Vision OCR to extract all text, then custom code to parse fields
C) Azure AI Language named entity recognition on extracted text
D) Azure Form Recognizer pre-built invoice model

---

**Q26.** A marketing team with no coding experience wants to test how a deployed model in Microsoft Foundry responds to different system prompts before their developers build the full application. Where can they do this WITHOUT writing any code?

A) They must ask a developer to write a small script with the Foundry SDK, since model testing always requires code
B) In the Azure portal's Cloud Shell, using CLI commands to send test prompts to the deployment
C) By exporting the model and running it locally in a Jupyter notebook
D) In the Foundry portal's chat playground, where they can set a system prompt, send test messages, and adjust parameters interactively

---

**Q27.** A company needs to analyze customer feedback emails to identify the main topics discussed and determine whether each email expresses positive, negative, or neutral sentiment. Which Azure AI service capability should they use?

A) Azure AI Language's sentiment analysis and key phrase extraction features
B) Azure AI Speech for transcription combined with custom entity recognition
C) Azure Computer Vision's image classification with custom training
D) Azure Content Understanding's document layout analysis

---

**Q28.** A developer is testing a prompt in Azure AI Foundry for a model deployment. The system prompt is 450 tokens, the user prompt is 200 tokens, and the generated response is 350 tokens. If the deployed model has a context window of 8,192 tokens and costs $0.03 per 1,000 input tokens and $0.06 per 1,000 output tokens, what is the approximate cost for this single request?

A) $0.0405 (650 input tokens + 350 output tokens at respective rates)
B) $0.0195 (650 input tokens at input rate only)
C) $0.0405 (1,000 total tokens at blended rate)
D) $0.06 (all tokens billed at output rate)

---

**Q29.** A retail company wants to automatically extract product names, prices, and expiration dates from scanned supplier invoices in various formats (PDF, images, handwritten notes). Which Azure AI capability is best suited for this task?

A) Azure Computer Vision's OCR with custom post-processing scripts
B) Azure Content Understanding with a custom extraction model
C) Azure AI Language's named entity recognition on pre-extracted text
D) Azure AI Vision's object detection trained on invoice samples

---

**Q30.** A developer is creating an image generation solution using Azure AI Foundry. The marketing team needs to generate product images with specific brand colors and styles. The system prompt includes detailed instructions about color schemes and composition. However, generated images often ignore these requirements. What should the developer do to improve consistency?

A) Increase the temperature parameter to 1.5 for more creative outputs
B) Switch from DALL-E to GPT-4 Vision for better understanding of visual concepts
C) Enable content filtering at the highest level to ensure brand compliance
D) Move the color and style requirements from the system prompt to the user prompt with specific descriptive keywords

---

**Q31.** A global company needs to provide real-time translation of customer support calls from English to Spanish, French, and German. The solution must convert the translated text back to speech for the customer. Which Azure AI services should be combined?

A) Azure AI Language (translation), Azure Content Understanding (document processing)
B) Azure AI Speech (speech-to-text), Azure AI Translator, Azure AI Speech (text-to-speech)
C) Azure AI Vision (OCR), Azure AI Language (translation), Azure AI Speech (synthesis)
D) Azure OpenAI GPT-4 for translation, Azure AI Speech for audio processing

---

**Q32.** A company wants its Foundry-based chat assistant to answer questions using ONLY the company's internal HR policy documents, and to say it does not know when the answer is not in those documents. Which approach BEST achieves this grounding requirement?

A) Increase the model's temperature so it generates more precise answers from its training data
B) Add the HR documents as a data source so responses are grounded in retrieved content, and instruct the model in the system prompt to answer only from the provided context
C) Fine-tune the base model on general HR terminology so it becomes an HR expert
D) Enable content filters on the deployment, which restrict the model to approved company topics

---

**Q33.** A healthcare application needs to extract patient names, medication names, and dosage information from unstructured clinical notes. The solution must identify medical entities specific to healthcare. Which Azure AI service should be used?

A) Azure OpenAI Service with a custom prompt asking to extract medical information
B) Azure AI Vision with OCR to read the text and identify entities
C) Azure Content Understanding with a custom document model
D) Azure AI Language with named entity recognition (NER) using the built-in healthcare entity model

---

**Q34.** A company is building an image classification solution to categorize product photos into 15 different product categories. They have 5,000 labeled images. Which Azure AI service provides the MOST appropriate approach?

A) Azure OpenAI DALL-E to generate additional product images for each category
B) Azure AI Vision Image Analysis to use pre-built product tagging
C) Azure Content Understanding to extract product information from the images
D) Azure AI Vision Custom Vision service to train a classification model with the labeled images

---

**Q35.** A call center application needs to convert customer voice recordings to text and then analyze the sentiment of each call. The average call is 8 minutes long. What is the correct sequence of Azure AI services to implement this solution?

A) Use Azure AI Vision to extract text from the audio waveform, then use Azure OpenAI to determine sentiment
B) Use Azure Content Understanding to process the audio file and extract both transcription and sentiment in one operation
C) Use Azure AI Speech speech-to-text to transcribe the audio, then use Azure AI Language sentiment analysis on the transcribed text
D) Use Azure AI Language to transcribe the audio directly and analyze sentiment simultaneously

---

**Q36.** A retail company receives invoices from multiple vendors in different formats (PDF, images, scanned documents). They need to automatically extract vendor name, invoice number, total amount, and line items. Which Azure AI capability is BEST suited for this task?

A) Azure AI Vision OCR to extract all text, then use custom code to parse the fields
B) Azure OpenAI with a vision-capable model to analyze each invoice image
C) Azure AI Document Intelligence with the pre-built invoice model
D) Azure AI Language key phrase extraction to identify important invoice information

---

**Q37.** A developer deployed a GPT-4 model in Azure AI Foundry and is testing it with the Foundry SDK. The model must refuse to provide medical diagnoses and instead direct users to consult healthcare professionals. After several test conversations, the model occasionally provides diagnostic information. What is the MOST effective solution?

A) Add the medical policy restriction in every user prompt before sending to the model
B) Reduce the temperature parameter to 0 to make responses more deterministic
C) Enable content filtering in the Foundry portal deployment settings to block medical content
D) Strengthen the system prompt with explicit instructions and examples of refusing medical diagnosis requests, using clear directive language

---

**Q38.** A developer is building a chatbot using Azure AI Foundry SDK and needs to ensure the model stays focused on providing technical support answers only. The chatbot should refuse to discuss unrelated topics like sports or entertainment. Which approach should the developer implement?

A) Add user prompt examples showing both technical and non-technical queries with expected responses
B) Increase the temperature parameter to 0.9 to make responses more diverse and creative
C) Configure a system prompt that defines the assistant's role, boundaries, and response guidelines
D) Deploy multiple model instances and route requests based on detected topic categories

---

**Q39.** A company processes customer feedback in Spanish, French, and German, and needs to extract sentiment scores and key phrases from each review. The solution must handle all three languages without requiring separate configurations per language. Which Azure AI service should be used?

A) Azure OpenAI Service with language-specific prompts for each review language
B) Azure Translator to convert all text to English first, then apply sentiment analysis
C) Azure AI Language with the sentiment analysis and key phrase extraction features
D) Azure AI Speech with the speech-to-text feature configured for multilingual input

---

**Q40.** A retail company wants to automatically categorize product images into predefined categories like 'Electronics', 'Clothing', 'Home & Garden', etc. They have 5,000 labeled training images. Which Azure AI capability should they use?

A) Azure AI Vision image generation to create category templates
B) Azure AI Vision Custom Vision for image classification training
C) Azure AI Vision OCR to extract product labels from images
D) Azure OpenAI DALL-E model to analyze image content

---

**Q41.** A healthcare organization is building an agent using Azure AI Foundry that helps patients schedule appointments. The agent needs to check real-time appointment availability from an external scheduling system before confirming bookings. What capability must be implemented in the agent solution?

A) Embed the scheduling system's database connection string in the system prompt
B) Train a custom model on historical appointment data to predict availability
C) Configure the agent with function calling to invoke the scheduling system API
D) Use retrieval-augmented generation (RAG) to index appointment slot documents

---

**Q42.** A legal firm needs to extract specific data fields (contract date, parties involved, termination clauses) from thousands of contract PDFs with varying layouts and formats. Which Azure AI solution should they implement?

A) Azure AI Vision OCR to extract all text and then use regex patterns to find fields
B) Azure OpenAI GPT-4 to read each PDF page and extract information via prompts
C) Azure AI Content Understanding with custom document extraction models
D) Azure AI Language named entity recognition on the converted PDF text

---

**Q43.** A developer is testing a generative AI model deployment in Azure AI Foundry portal. The model returns coherent responses for general questions but produces inconsistent and sometimes incorrect answers when asked about the company's internal product documentation. The documentation exists in a SharePoint library. What solution should be implemented to improve answer accuracy?

A) Implement a RAG pattern by indexing the SharePoint documentation and retrieving relevant content before generating responses
B) Increase the model's max_tokens parameter to allow longer, more detailed responses
C) Fine-tune the base model using the entire SharePoint library as training data
D) Reduce the temperature parameter to 0.1 to make responses more deterministic

---

**Q44.** A company is building a customer support chatbot using Azure OpenAI Service through Microsoft Foundry. The chatbot must maintain conversation context, remember customer preferences mentioned earlier in the chat, and provide consistent responses based on company policies. Which approach BEST implements this requirement?

A) Use a system prompt that includes company policies and configure the model's temperature to 0 to ensure consistency across all conversations
B) Store all previous conversations in Azure Blob Storage and retrieve them using Azure Cognitive Search before each response
C) Deploy multiple model instances with different system prompts and use Azure Front Door to route requests based on conversation topic
D) Implement a system prompt containing company policies and guidelines, then pass conversation history as user messages in each API call to maintain context

---

**Q45.** A developer needs to extract key information from medical intake forms that contain both handwritten patient notes and printed checkboxes. The forms vary in layout across different clinics. Which Azure AI service available through Microsoft Foundry should the developer use?

A) Azure AI Vision for OCR to extract text, then Azure OpenAI to parse the extracted content into structured data
B) Azure AI Language custom named entity recognition to identify medical entities directly from scanned images
C) Azure Form Recognizer prebuilt receipt model to extract form fields and handwritten notes
D) Azure Content Understanding (Document Intelligence) with a custom model trained on sample forms from each clinic

---

