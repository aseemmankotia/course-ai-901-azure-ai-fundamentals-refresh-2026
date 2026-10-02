# AI-901 Full Exam Simulation Quick Reference

## Exam Format
| Attribute | Value |
|-----------|-------|
| Questions | 40-60 (varies by version) |
| Active Time | 45 minutes |
| Total Time | 65 minutes (includes tutorial, survey) |
| Passing Score | 700/1000 (~70%, scaled scoring) |
| Question Types | Single-select, multiple-select, drag-and-drop, hot area |

## Time Management Formula
- **1 minute per question** average
- **Max 2 minutes** on any question first pass
- **Mark and move on** if uncertain
- **Reserve final 10 minutes** for marked question review

## Question Type Strategies

### Single-Select
- Read question stem for key constraints
- Eliminate answers violating constraints
- Watch for "BEST" vs "correct" wording (BEST = optimal, correct = works)

### Multiple-Select (Critical!)
- Select **EXACTLY** the number stated ("Select TWO" = select 2, not 1 or 3)
- Wrong count = entire question wrong
- Count your selections before submitting

### Scenario Questions
1. Identify key requirements and constraints
2. Eliminate answers that violate any constraint
3. Choose most direct/simplest solution unless "cost-optimized" or "minimal management" specified

## Service Selection Quick Matrix

### NLP Workloads
| Need | Service |
|------|--------|
| Pre-built NLP (sentiment, entities, intent) | Azure AI Language |
| PII detection and redaction | Azure AI Language PII |
| Generative text, conversational AI | Azure OpenAI Service |
| Speech to text with custom vocabulary | Azure AI Speech (custom model) |

### Vision Workloads
| Need | Service |
|------|--------|
| Text from images (simple OCR) | Azure AI Vision OCR |
| Structured document extraction (forms, receipts) | Azure AI Document Intelligence |
| Text + structure (tables, checkboxes) | Document Intelligence Layout |
| Object detection, image classification | Azure AI Vision |
| Face detection (no identification) | Azure AI Vision Face (detect only) |

### Foundry Components
| Component | Purpose |
|-----------|--------|
| System message | Define AI role, behavior, constraints |
| User message | Actual user query/request |
| Function/tool | Enable external API calls, tool use |
| Grounding data | Provide reference documents/knowledge |
| Agent | Orchestrates functions, multi-step reasoning |
| Chat app | Conversational interface to grounded knowledge |

## Responsible AI Principle Mapping

| Scenario Keyword | Principle | First Action |
|------------------|-----------|-------------|
| Differential outcomes by demographics | Fairness | Evaluate training data balance |
| Can't explain decision | Transparency | Implement model explainability |
| Harmful content generated | Reliability & Safety | Deploy content filters |
| Who's accountable? | Accountability | Define governance structure |
| Unauthorized data access | Privacy & Security | Implement access controls |
| Model biased against group | Fairness + Inclusiveness | Retrain with representative data |

## Common Exam Traps

1. **OCR vs Document Intelligence**: OCR = text only. Document Intelligence = text + structure
2. **Content Safety vs PII Detection**: Harmful content vs personal information—different services
3. **System vs User prompts**: System = behavior, User = query
4. **Agent vs Chat app**: Agent = function calling, Chat = knowledge only
5. **Facial detection vs identification**: Detection allowed, identification restricted
6. **Multiple-select count**: Must select exact number stated

## Review Checklist (Final 10 Minutes)
- [ ] All questions answered (unanswered = automatic wrong)
- [ ] All multiple-select questions have correct count
- [ ] Marked questions reviewed
- [ ] Hot area/drag-drop questions verified
- [ ] No second-guessing confident answers

## Key Numbers to Remember
- Passing score: **700/1000**
- Speech custom model: Needed for **custom vocabulary**
- Document Intelligence Layout: Extracts **text + structure**
- Multiple-select: Select **exactly** the stated number
- Time per question: **~1 minute** average
