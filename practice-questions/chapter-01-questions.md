## Chapter 1: Common AI Workloads and Business Scenarios — Practice Questions

**Q1.** A retail company wants to automatically count the number of products on store shelves using camera images to manage inventory levels. Which AI workload BEST addresses this requirement?

A) Natural language processing with entity recognition
B) Object detection with computer vision
C) Optical character recognition (OCR)
D) Generative AI for image synthesis

<details>
<summary>Answer</summary>

**Correct: B**

Object detection identifies and counts multiple instances of objects (products) within images, providing coordinates and confidence scores for each detected item. This is the exact workload for inventory counting scenarios.

**Why the others are wrong:**
- NLP entity recognition works with text, not images. Cannot process camera feeds or count physical objects.
- OCR extracts text from images but doesn't count objects. Would only work if reading price tags or labels, not counting products.
- Generative AI creates new images rather than analyzing existing ones. Cannot count real-world objects from camera feeds.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A hospital needs to extract patient names, medication dosages, and appointment dates from thousands of handwritten doctor notes. Which combination of AI workloads is required?

A) OCR followed by sentiment analysis
B) Computer vision object detection only
C) Speech-to-text with key phrase extraction
D) Document intelligence with layout analysis and entity extraction

<details>
<summary>Answer</summary>

**Correct: D**

Document intelligence combines OCR with form recognition and entity extraction specifically designed for structured and semi-structured documents. It understands document layout, extracts handwritten text, and identifies entities like names, dates, and quantities—exactly what's needed for medical notes.

**Why the others are wrong:**
- OCR alone only converts text to digital format without understanding context or extracting specific entities. Sentiment analysis determines emotional tone, irrelevant for medical data extraction.
- Object detection locates objects in images but doesn't read or extract text from documents.
- Speech-to-text converts audio to text, but these are handwritten notes (visual input), not audio recordings.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A customer support system needs to automatically categorize incoming support emails as 'billing', 'technical', or 'general inquiry' and route them to appropriate teams. Which AI workload accomplishes this?

A) Text classification using NLP
B) Image classification
C) Speech translation
D) Generative AI text generation

<details>
<summary>Answer</summary>

**Correct: A**

Text classification (also called document classification) is an NLP workload that assigns predefined categories to text content. It's designed exactly for routing and categorizing text-based communications like emails.

**Why the others are wrong:**
- Image classification categorizes images, not text. Emails are text content requiring NLP.
- Speech translation converts spoken language audio between languages. Emails are written text, not audio.
- Generative AI creates new content. This scenario needs analysis of existing content, not generation of new text.

</details>

---

**Q4.** A global conference platform needs to provide real-time subtitles in multiple languages for live video presentations. Which AI workload is required?

A) Direct speech translation
B) Speech-to-text followed by translation and text-to-speech
C) OCR with language detection
D) Natural language generation

<details>
<summary>Answer</summary>

**Correct: A**

Speech translation directly converts spoken audio from one language to another language's text or audio in a single integrated workload, optimized for real-time scenarios. This is the most efficient approach for live conference subtitles.

**Why the others are wrong:**
- While this pipeline works, it's inefficient for real-time use. Speech translation is a dedicated workload that handles this in one step with lower latency.
- OCR reads text from images/video frames. Conference audio is spoken words, not on-screen text.
- NLG generates text from structured data, not from spoken audio in different languages.

</details>

---

**Q5.** An e-commerce company analyzes product reviews to determine if customers are satisfied or dissatisfied with purchases. Which specific NLP capability is being used?

A) Sentiment analysis
B) Entity recognition
C) Key phrase extraction
D) Language translation

<details>
<summary>Answer</summary>

**Correct: A**

Sentiment analysis determines the emotional tone (positive, negative, neutral) of text. This directly measures satisfaction vs dissatisfaction in customer reviews, typically returning a score from 0 (negative) to 1 (positive).

**Why the others are wrong:**
- Entity recognition identifies specific items (products, people, locations) in text but doesn't determine satisfaction level or emotional tone.
- Key phrase extraction identifies main topics or important phrases but doesn't classify emotional sentiment or satisfaction.
- Translation converts text between languages but doesn't analyze satisfaction or sentiment.

</details>

---

**Q6.** A software development team wants an AI system that writes code functions based on natural language descriptions, tests the code automatically, and fixes bugs without human intervention. Which type of AI capability is needed?

A) Generative AI for code completion only
B) Natural language processing with entity extraction
C) Computer vision with object detection
D) AI agent with tool use and autonomous decision-making

<details>
<summary>Answer</summary>

**Correct: D**

AI agents perform autonomous task completion, make decisions, and use tools (like compilers, debuggers, testing frameworks) to complete multi-step goals. Writing code, testing it, and fixing bugs requires autonomous decision-making and tool orchestration—agent capabilities, not just generation.

**Why the others are wrong:**
- Code completion generates code snippets but doesn't test code, identify bugs, or make autonomous decisions about fixes. It's a single-step generative task, not autonomous multi-step problem solving.
- NLP entity extraction identifies elements in text but doesn't generate code or perform automated testing/debugging.
- Computer vision analyzes images/video, completely unrelated to code generation and testing workflows.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** A security system uses cameras to identify authorized personnel by recognizing their faces and granting building access. What type of computer vision workload is this?

A) Image classification
B) Object detection
C) OCR
D) Facial recognition

<details>
<summary>Answer</summary>

**Correct: D**

Facial recognition specifically identifies individual people by analyzing facial features and matching them to a database of known faces. This is distinct from general object detection or classification—it's a specialized computer vision workload for identity verification.

**Why the others are wrong:**
- Image classification assigns categories to entire images (e.g., 'outdoor scene', 'office'), not individual identity verification.
- Object detection locates objects in images but doesn't identify specific individuals. It could detect 'a person' but not 'John Smith'.
- OCR reads text from images. Faces aren't text documents requiring character recognition.

</details>

---

**Q8.** A marketing team needs to generate unique product descriptions for 10,000 items based on technical specifications. A chatbot interface is NOT required—just automated text generation at scale. Which AI capability addresses this need?

A) AI agent with autonomous planning
B) Generative AI text generation
C) Conversational AI chat application
D) NLP key phrase extraction

<details>
<summary>Answer</summary>

**Correct: B**

Generative AI text generation creates new text content from prompts or structured data. For batch processing of product descriptions without conversation, direct text generation is the appropriate workload—no agent orchestration or chat interface needed.

**Why the others are wrong:**
- AI agents perform multi-step autonomous tasks with decision-making and tool use. Simple text generation doesn't require agent capabilities.
- Chat applications provide conversational interfaces with back-and-forth dialogue. This scenario needs batch text generation, not interactive conversation.
- Key phrase extraction analyzes existing text to find important phrases. This scenario requires creating new text, not analyzing existing content.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

