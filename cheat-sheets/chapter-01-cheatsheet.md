# AI-901 Chapter 1: Common AI Workloads Quick Reference

## Computer Vision Workloads

| Workload | Input | Output | Use Case |
|----------|-------|--------|----------|
| **Image Classification** | Single image | Category label + confidence | Is this a cat or dog? Indoor or outdoor scene? |
| **Object Detection** | Single image | Bounding boxes + labels + confidence per object | Count items on shelf, detect multiple people |
| **Facial Recognition** | Image with face | Identity match from database | Security access, photo tagging |
| **OCR** | Image with text | Plain text strings | Read signs, extract printed text |

**Exam Gotcha**: Object detection finds multiple things, classification assigns one category to the whole image.

## Natural Language Processing (NLP) Workloads

| Workload | Input | Output | Use Case |
|----------|-------|--------|----------|
| **Sentiment Analysis** | Text | Score 0-1 (negative to positive) | Analyze reviews, social media |
| **Entity Recognition** | Text | List of entities with types | Extract names, dates, locations from documents |
| **Key Phrase Extraction** | Text | List of important phrases | Document summarization, auto-tagging |
| **Translation** | Text in language A | Text in language B | Translate documents, websites |
| **Text Classification** | Text | Category from predefined list | Email routing, content moderation |

**Common Entity Types**: Person, Location, DateTime, Organization, Quantity, Email, URL

## Speech Workloads

| Workload | Input | Output | Use Case |
|----------|-------|--------|----------|
| **Speech-to-Text** | Audio | Text transcription | Meeting notes, subtitles |
| **Text-to-Speech** | Text | Audio/voice | Voice assistants, accessibility |
| **Speech Translation** | Audio in language A | Text/audio in language B | Live conference translation |

**Exam Tip**: Speech translation is ONE workload (not STT → translate → TTS).

## Document Intelligence

**Capabilities**: OCR + layout understanding + form recognition + entity extraction

**When to Use**:
- Extracting data from invoices, receipts, forms
- Reading handwritten documents with structure
- Identifying tables, key-value pairs in documents

**vs OCR Alone**: OCR only gets text. Document intelligence understands document structure and extracts specific fields.

## Generative AI Workloads

| Type | Creates | Example |
|------|---------|----------|
| **Text Generation** | New text from prompts | Product descriptions, emails |
| **Image Generation** | New images from prompts | Marketing visuals, concept art |
| **Code Completion** | Code from natural language | Function generation, boilerplate |

**Key Point**: Generates NEW content. Not for analyzing existing content.

## AI Agents

**Defining Characteristics**:
1. Autonomous multi-step task completion
2. Decision-making without human intervention
3. Tool use (APIs, databases, compilers, etc.)
4. Goal-directed behavior

**Agent vs Chat App**:
- **Agent**: Does tasks autonomously (e.g., "debug this code and fix all errors")
- **Chat App**: Conversational interface (e.g., "answer customer questions")

**Exam Scenario Clues**:
- "Autonomous", "without intervention", "multi-step", "use tools" → Agent
- "Conversational", "Q&A", "chat interface", "dialogue" → Chat App

## Scenario Mapping Guide

| Business Need | Correct Workload | Wrong Answers to Avoid |
|---------------|------------------|------------------------|
| Count inventory items | Object detection | Classification, OCR |
| Analyze customer satisfaction | Sentiment analysis | Entity recognition, translation |
| Extract data from invoices | Document intelligence | OCR alone, NLP alone |
| Real-time conference subtitles | Speech translation | STT + translate + TTS |
| Identify authorized personnel | Facial recognition | Object detection, classification |
| Route emails to departments | Text classification | Sentiment analysis, generation |
| Generate product descriptions | Text generation (Generative AI) | AI agent, chat app |
| Automated testing + debugging | AI agent | Code completion alone, NLP |

## Exam Strategy

**Heavily Tested**:
1. Matching business scenarios to exact workload type
2. Document intelligence vs OCR vs NLP distinctions
3. Agent vs chat app vs generative AI capabilities

**Common Mistakes**:
- Choosing classification when detection is needed (counting = detection)
- Picking OCR when document intelligence is required (structured data extraction)
- Selecting chat app when agent autonomy is needed (multi-step tasks)
- Choosing NLP for image problems or CV for text problems

**Memory Trick**: 
- **Detection** = multiple objects
- **Classification** = one category
- **Document Intelligence** = OCR + structure + entities
- **Agent** = autonomous + tools
- **Chat** = conversation
