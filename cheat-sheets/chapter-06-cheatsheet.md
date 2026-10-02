# Text and Speech AI with Foundry Tools — Cheat Sheet

## Sentiment Analysis
| Aspect | Details |
|--------|--------|
| **Output Categories** | Positive, Negative, Neutral, Mixed |
| **Confidence Score** | 0.0 to 1.0 (model confidence in classification) |
| **Mixed vs Neutral** | Mixed = both positive AND negative present; Neutral = neither strong positive nor negative |
| **Document vs Sentence** | Provides both document-level and per-sentence sentiment |
| **Exam Trap** | Score is confidence, NOT percentage of positive words |

## Key Phrase Extraction
| What It Does | Identifies main topics/themes in text |
|--------------|---------------------------------------|
| **Example Output** | 'customer support', 'product quality', 'shipping speed' |
| **Use Case** | Topic analysis, content categorization, trend identification |
| **Not For** | Extracting specific typed entities (use entity recognition instead) |
| **Exam Trap** | Don't confuse with entity recognition—key phrases are topics, not structured data |

## Entity Recognition
| Entity Types | Person, Location, Organization, Date, Quantity, Email, URL, Phone |
|--------------|-------------------------------------------------------------------|
| **Output** | Extracted entity + type + confidence score |
| **Use Case** | Extracting structured data from contracts, forms, documents |
| **Example** | "Microsoft" → Organization, "January 15, 2026" → Date, "$50,000" → Quantity |
| **Exam Trap** | Use for specific typed data extraction, not topic identification |

## Language Detection vs Translation
| Feature | Language Detection | Translation |
|---------|-------------------|-------------|
| **Purpose** | Identify language only | Convert text between languages |
| **When to Use** | Routing, filtering, preprocessing | Making content available in different language |
| **Languages** | Detects 100+ | Translates between 100+ |
| **Cost Efficiency** | Cheaper when no translation needed | Use only when conversion required |
| **Exam Scenario** | 'Route to language-specific pipeline' → detection only | 'Make all articles available in English' → detection THEN translation |

## Speech-to-Text
| Mode | Real-time Transcription | Batch Transcription |
|------|------------------------|---------------------|
| **Input** | Live audio stream | Pre-recorded audio files |
| **Output Timing** | Immediate during conversation | After processing completes |
| **Use Case** | Live call transcription, real-time captioning | Post-call analysis, recorded meeting transcription |
| **Language Detection** | Can auto-detect source language | Supports language parameter |
| **Exam Keyword** | 'Live', 'real-time', 'as conversation happens' | 'Recorded', 'batch', 'post-call' |

## Text-to-Speech
| Feature | Neural Voices |
|---------|---------------|
| **Quality** | Natural-sounding, human-like |
| **Customization** | Male/female, accents, languages |
| **Use Case** | Audio narration, accessibility, virtual assistants |
| **Languages** | Multiple languages supported |
| **Exam Keyword** | 'Generate audio', 'narration', 'natural-sounding voices' |

## Azure AI Foundry Tools
| Aspect | Details |
|--------|--------|
| **What They Are** | Pre-built AI components for common tasks |
| **Included Services** | Sentiment analysis, key phrase extraction, entity recognition, language detection, translation, speech services |
| **Advantage** | No training data needed, work out-of-box, faster development |
| **When to Use** | Standard use cases with common requirements |
| **When NOT to Use** | Highly specialized domains requiring custom models |
| **Exam Trap** | Foundry Tools aren't free—they follow standard Azure pricing |

## Decision Tree for Exam Questions
```
Text analysis needed?
├─ Identify sentiment? → Sentiment Analysis
├─ Extract main topics? → Key Phrase Extraction  
├─ Extract typed entities? → Entity Recognition
└─ Identify language? → Language Detection

Translation needed?
├─ Only identify language? → Language Detection only
└─ Convert languages? → Detection + Translation

Audio involved?
├─ Audio → Text? → Speech-to-Text
│   ├─ Live? → Real-time transcription
│   └─ Recorded? → Batch transcription
└─ Text → Audio? → Text-to-Speech (Neural Voices)

Build vs Buy?
├─ Standard use case? → Foundry Tools (pre-built)
└─ Specialized domain? → Custom model
```

## Common Exam Traps
1. **Sentiment score** = confidence in classification, NOT percentage of positive words
2. **Mixed sentiment** ≠ neutral; mixed = both positive AND negative present
3. **Key phrases** = topics; **entities** = typed structured data
4. **Language detection alone** when no translation needed—don't over-engineer
5. **Speech-to-text vs text-to-speech**—direction matters!
6. **Real-time vs batch transcription**—watch for keywords 'live', 'recorded'
7. **Foundry Tools not free**—but reduce development time vs custom models
