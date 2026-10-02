# Chapter 2: Responsible AI Principles - Quick Reference

## The Six Principles (40-45% of AI-901 Exam)

| Principle | Definition | Key Exam Indicators |
|-----------|------------|--------------------|
| **Fairness** | Treat all people/groups equitably, avoid bias | Disparate outcomes for demographics; biased training data; unequal performance across groups |
| **Reliability & Safety** | Perform consistently, handle errors gracefully | Incorrect outputs; system failures; unpredictable behavior; no fallback mechanisms |
| **Privacy & Security** | Protect personal data, encryption, access controls | Sensitive data handling; PII protection; encryption requirements; access control needs |
| **Inclusiveness** | Empower ALL people regardless of abilities | Accessibility features; disability accommodations; language support; diverse user needs |
| **Transparency** | Users understand how AI makes decisions | Explaining decisions; disclosure of data use; understanding system logic |
| **Accountability** | Humans remain responsible for AI decisions | Human oversight; assigned responsibility; review processes; appeal mechanisms |

## Exam Strategy: Principle Selection Matrix

**Question asks about...** → **Choose this principle:**
- Biased outcomes for different groups → **Fairness**
- Explaining how decisions are made → **Transparency**
- Who is responsible for errors → **Accountability**
- Protecting sensitive data → **Privacy & Security**
- System provides wrong answers → **Reliability & Safety**
- Accessibility for disabilities → **Inclusiveness**

## Common Fairness Violations (HEAVILY TESTED)

### Training Data Issues
- Imbalanced datasets (90% one group, 10% another)
- Historical bias in data reflects past discrimination
- Underrepresentation of certain demographics

**Fix:** Collect representative data, retrain model, test for disparate impact

### Feature Selection Issues
- Features that correlate with protected characteristics (zip code → race)
- Criteria that disproportionately impact certain groups (employment gaps → women)

**Fix:** Remove or adjust problematic features, test for proxy discrimination

### Output/Performance Issues
- Different accuracy rates for different groups
- Disparate error rates (false positives/negatives)

**Fix:** Evaluate fairness metrics per demographic, retrain with balanced data

## Privacy & Security Requirements (HEAVILY TESTED)

### Three Required Technical Controls
1. **Encryption:** At rest AND in transit for sensitive data
2. **Access Controls:** Role-based access, principle of least privilege
3. **Data Minimization:** Store only necessary data, avoid full PII

### Personal/Sensitive Data Categories
- Payment information (credit cards, bank accounts)
- Health records (HIPAA protected)
- Personally Identifiable Information (PII): SSN, passport, driver's license
- Biometric data (fingerprints, facial recognition)
- Location data, browsing history

**Exam Tip:** ALL THREE controls required - encryption alone isn't enough

## Scenario Application Guide

### Fairness Scenarios
- Resume screening ranks one gender lower
- Medical diagnosis accuracy differs by race
- Loan approvals vary by neighborhood
- Facial recognition fails on darker skin tones

### Transparency Scenarios
- Users don't understand why they were denied
- Black box model with no explanations
- Unclear data collection practices
- Hidden decision criteria

### Accountability Scenarios
- No human review of AI decisions
- Unclear who is responsible for errors
- No process to appeal AI decisions
- Fully automated decisions with no oversight

### Privacy/Security Scenarios
- Sensitive data not encrypted
- Broad access to personal information
- Storing unnecessary PII
- Data breaches or unauthorized access

### Reliability Scenarios
- System gives incorrect information
- Unpredictable performance
- No error handling or fallbacks
- Inconsistent results

### Inclusiveness Scenarios
- No accessibility features for disabilities
- Voice-only interface (excludes deaf users)
- Complex interface (excludes cognitive impairments)
- Single language support

## Key Distinctions (Commonly Confused)

**Fairness vs Transparency**
- Fairness = WHAT outcomes (equitable results)
- Transparency = HOW decisions made (understanding process)

**Accountability vs Reliability**
- Accountability = WHO responsible (human oversight)
- Reliability = DOES IT WORK (technical performance)

**Inclusiveness vs Fairness**
- Inclusiveness = ACCESS for all abilities (can everyone use it?)
- Fairness = EQUITY of outcomes (does it treat groups fairly?)

## Exam Traps

❌ **TRAP:** System applies same rules to everyone = Fair
✅ **TRUTH:** Fair requires equitable OUTCOMES, not just equal process

❌ **TRAP:** Documenting bias satisfies Fairness
✅ **TRUTH:** Transparency documents, Fairness fixes (retrain model)

❌ **TRAP:** Confidence scores fix biased performance
✅ **TRUTH:** Confidence helps Reliability/Transparency, not Fairness

❌ **TRAP:** Access controls alone satisfy Privacy
✅ **TRUTH:** Need encryption + access controls + data minimization

## Quick Decision Tree for Scenario Questions

1. Does scenario involve different outcomes for different groups? → **Fairness**
2. Does scenario ask who/what is responsible for decisions? → **Accountability**
3. Does scenario involve protecting sensitive data? → **Privacy & Security**
4. Does scenario ask about explaining/understanding decisions? → **Transparency**
5. Does scenario involve incorrect outputs or failures? → **Reliability & Safety**
6. Does scenario involve accessibility/abilities? → **Inclusiveness**
