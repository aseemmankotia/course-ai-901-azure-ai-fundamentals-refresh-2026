## Chapter 6: Text and Speech AI with Foundry Tools — Practice Questions

**Q1.** A retail company receives thousands of product reviews daily in multiple languages. They need to determine the overall sentiment of each review and extract key topics customers mention most frequently. Which combination of Azure AI Language features should they use?

A) Language detection and translation only
B) Entity recognition and translation
C) Sentiment analysis and key phrase extraction
D) Speech-to-text and sentiment analysis

<details>
<summary>Answer</summary>

**Correct: C**

Sentiment analysis provides the overall sentiment score (positive/negative/neutral/mixed) for each review, while key phrase extraction identifies the main topics customers are discussing (e.g., 'shipping speed', 'product quality', 'customer service'). This directly matches the business requirements.

**Why the others are wrong:**
- Language detection and translation don't provide sentiment scores or topic extraction—they only identify and convert languages
- Entity recognition extracts structured data like names and dates but doesn't provide sentiment scores or main topics/themes
- Speech-to-text is for audio transcription, not text analysis—reviews are already in text form

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A healthcare application receives patient feedback forms in English, Spanish, and French. The system needs to identify which language each form is written in before routing it to the appropriate language-specific processing pipeline. No translation is required. Which Azure AI service capability should be used?

A) Translation service with source language auto-detect
B) Entity recognition with language parameter
C) Sentiment analysis with multilingual mode
D) Language detection only

<details>
<summary>Answer</summary>

**Correct: D**

Language detection identifies the language of input text without performing translation. Since the requirement explicitly states no translation is needed—only identification for routing purposes—language detection alone is the most efficient and cost-effective solution.

**Why the others are wrong:**
- Translation service performs unnecessary translation operations when only language identification is required, adding cost and latency
- Entity recognition extracts entities from text but doesn't provide language identification as its primary function
- Sentiment analysis analyzes sentiment but doesn't provide language identification as a standalone output for routing decisions

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A customer service center needs to automatically transcribe phone calls in real-time so agents can see a live text version of the conversation while speaking with customers. Which Azure AI Speech capability meets this requirement?

A) Text-to-speech with neural voices
B) Speech-to-text with real-time transcription
C) Batch transcription service
D) Custom Neural Voice training

<details>
<summary>Answer</summary>

**Correct: B**

Speech-to-text with real-time transcription converts audio to text as the conversation happens, providing live transcription. This is specifically designed for scenarios where immediate text output is required during active audio streaming.

**Why the others are wrong:**
- Text-to-speech converts text to audio (opposite direction)—it generates speech from text rather than transcribing speech to text
- Batch transcription processes pre-recorded audio files after the fact, not in real-time during live calls
- Custom Neural Voice training creates custom synthetic voices for text-to-speech, not transcription

</details>

---

**Q4.** An e-learning platform wants to generate audio narration from lesson text content in multiple languages with natural-sounding voices. Students should be able to select different voice options. Which Azure AI capability should be implemented?

A) Speech-to-text with custom models
B) Language detection and translation
C) Key phrase extraction with audio output
D) Text-to-speech with neural voices

<details>
<summary>Answer</summary>

**Correct: D**

Text-to-speech converts written text into natural-sounding audio. Neural voices provide high-quality, human-like speech in multiple languages with various voice options (male, female, different accents), exactly matching the requirement for customizable audio narration.

**Why the others are wrong:**
- Speech-to-text transcribes audio to text (opposite direction)—it doesn't generate audio from text
- Language detection and translation handle text-to-text operations but don't generate audio output
- Key phrase extraction analyzes text content but doesn't produce audio—it's a text analysis feature, not speech synthesis

</details>

---

**Q5.** A social media monitoring tool analyzes user comments to categorize them as positive, negative, neutral, or mixed. Each comment receives a score between 0.0 and 1.0 indicating confidence level. A comment scored as 'positive' with 0.92 confidence means what?

A) 92% of the comment text is positive words, 8% is neutral or negative
B) The model is 92% confident the overall sentiment is positive
C) The comment has a positivity rating of 92 out of 100
D) 92% of users would rate this comment as positive

<details>
<summary>Answer</summary>

**Correct: B**

Sentiment analysis confidence scores (0.0 to 1.0) represent the model's confidence in its sentiment classification. A score of 0.92 means the model is 92% confident in its determination that the overall sentiment is positive. This is how Azure AI Language sentiment analysis works.

**Why the others are wrong:**
- Confidence scores don't measure percentage of positive words—they measure model certainty about the classification
- The 0.0-1.0 scale is confidence in classification, not a rating scale out of 100—sentiment is categorical (positive/negative/neutral/mixed) with confidence
- Confidence scores reflect model certainty, not user agreement—they're not based on polling or user ratings

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** A legal document processing system needs to extract specific structured information from contracts: company names, dates, monetary amounts, and locations. Which Azure AI Language feature is BEST suited for this requirement?

A) Entity recognition
B) Key phrase extraction
C) Sentiment analysis
D) Translation with named entity detection

<details>
<summary>Answer</summary>

**Correct: A**

Entity recognition specifically extracts structured entities like person names, organizations (company names), dates, quantities (monetary amounts), and locations. This is designed for extracting specific categorized information from text, exactly matching the requirement.

**Why the others are wrong:**
- Key phrase extraction identifies main topics/themes (e.g., 'payment terms', 'liability clause') but doesn't extract specific structured entities with their types
- Sentiment analysis determines emotional tone (positive/negative/neutral/mixed) but doesn't extract specific structured data points
- Translation converts text between languages—while it may preserve entities, its primary purpose isn't entity extraction

</details>

---

**Q7.** A global news aggregator receives articles in 100+ languages and needs to make all content available in English. The system must first determine what language each article is written in, then convert it to English. Which approach should be used?

A) Use language detection first, then translation only for non-English articles
B) Use translation service only with auto-detect source language enabled
C) Use entity recognition to identify language, then translation
D) Use key phrase extraction with multilingual output

<details>
<summary>Answer</summary>

**Correct: A**

Language detection identifies the source language, then translation is applied only when needed (non-English articles). This is more efficient than translating everything blindly, and explicitly separating detection from translation provides better control and cost optimization for articles already in English.

**Why the others are wrong:**
- Auto-detect with translation would unnecessarily translate English articles to English, wasting API calls and adding latency—the exam tests efficiency in this scenario
- Entity recognition extracts entities from text but isn't designed for language identification—it's the wrong tool for this task
- Key phrase extraction identifies topics/themes but doesn't perform language detection or translation

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** A company is building a customer support chatbot using Azure AI Foundry. They need to analyze incoming messages for sentiment, extract key topics, and identify customer names and account numbers. Rather than building custom models, they want to use pre-built capabilities. What is the advantage of using Foundry Tools for this scenario?

A) Foundry Tools are free while custom models require per-token charges
B) Foundry Tools support more languages than custom-trained models
C) Foundry Tools provide higher accuracy than any custom model
D) Foundry Tools provide pre-built components that reduce development time and don't require training data

<details>
<summary>Answer</summary>

**Correct: D**

Azure AI Foundry provides pre-built tools for common AI tasks (sentiment analysis, key phrase extraction, entity recognition) that work out-of-the-box without requiring training data, labeled datasets, or custom model development. This significantly reduces development time and complexity for standard use cases.

**Why the others are wrong:**
- Foundry Tools and Language services follow standard Azure pricing—they're not free, and the exam tests understanding of when to use pre-built vs custom solutions based on requirements, not cost
- Language support depends on the specific Azure AI service, not whether you use Foundry Tools or custom models—both can support many languages
- Accuracy depends on the use case—custom models can outperform pre-built tools for specialized domains with sufficient training data

</details>

---

