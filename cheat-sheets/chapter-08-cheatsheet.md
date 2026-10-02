# Azure AI Document Intelligence Cheat Sheet

## Service Purpose
**Azure AI Document Intelligence** (formerly Form Recognizer): Extracts structured, labeled data from documents—understands layout, fields, and relationships.

## Pre-Built Models vs Custom Models

| Use Pre-Built When | Use Custom When |
|---|---|
| Document type matches available models | Organization-specific layouts |
| Standard formats (invoices, receipts, IDs) | Unique fields not in pre-built models |
| No training data needed | Have 5+ labeled examples |
| Examples: vendor invoices, expense receipts, driver's licenses, business cards | Examples: proprietary forms, custom intake documents, specific contract templates |

## Pre-Built Models: What They Extract

### Receipt Model
- **Fields**: Merchant name/address/phone, date, time, total, subtotal, tax, tip, line items
- **Use case**: Expense reimbursement, AP automation
- **Exam note**: Handles handwritten receipts, multiple languages

### Invoice Model
- **Fields**: Vendor/customer info, invoice ID, dates (invoice/due), total, subtotal, tax, PO number, line items (description, quantity, price)
- **Use case**: Accounts payable processing
- **Exam note**: Extracts full line item tables with structure

### ID Document Model
- **Types**: Driver's licenses, passports, ID cards, residence permits
- **Fields**: Name (first/last), DOB, document number, address, expiration, sex, country/region, MRZ
- **Use case**: Identity verification, KYC compliance
- **Exam note**: Global coverage—handles IDs from multiple countries

### Business Card Model
- **Fields**: Names, job titles, companies, departments, addresses, emails, websites, phones (mobile/work/fax)
- **Use case**: Contact digitization, CRM import
- **Exam note**: Handles varied layouts—no training needed

### W-2 Model (US Tax Form)
- **Fields**: Employee info, employer info, wages, federal/state tax withheld, SSN, EIN
- **Use case**: Tax document processing, HR systems

### 1099 Models (US Tax Forms)
- **Types**: 1099-MISC, 1099-NEC, 1099-DIV, 1099-INT, others
- **Use case**: Tax processing for contractors, investment income

## Core Capabilities

### Layout Analysis
- Extracts **tables** (rows/columns preserved)
- Detects **selection marks** (checkboxes, radio buttons)
- Returns **text lines** with reading order
- Provides **bounding boxes** for spatial info
- **Exam note**: Use when table structure matters

### Key-Value Pair Extraction
- Identifies **field labels** and **associated values**
- Example: "Invoice Number: 12345" → key="Invoice Number", value="12345"
- **Exam note**: Core output for form extraction—structured, labeled data

### Confidence Scores
- **Range**: 0.0 (no confidence) to 1.0 (maximum confidence)
- Each extracted field has **individual score**
- **Best practice**: Set threshold (e.g., 0.85); route low-confidence to human review
- **Exam note**: Confidence scores enable human-in-the-loop workflows

## Custom Model Requirements
- **Minimum**: 5 labeled training documents
- **Recommended**: 15-20 for better accuracy
- **Format**: Label field locations in sample documents
- **Improvement**: Add more labeled samples over time to increase accuracy

## Key Distinctions (Heavily Tested)

### Document Intelligence vs OCR
| Azure AI Document Intelligence | Azure AI Vision OCR |
|---|---|
| Extracts **structured fields with labels** | Reads **raw text** only |
| Understands document layout (tables, forms) | Returns text + bounding boxes |
| Output: key-value pairs, tables, checkboxes | Output: unstructured text strings |
| Use for: forms, invoices, receipts, IDs | Use for: reading text from images/documents |

### Document Intelligence vs Language Service
| Azure AI Document Intelligence | Azure AI Language |
|---|---|
| Extracts **document structure/fields** | Analyzes **language content** |
| Purpose: structured data extraction | Purpose: sentiment, entities, key phrases |
| Example: invoice total, table cells | Example: positive/negative sentiment, person names |
| Use for: form processing, document digitization | Use for: text analysis, content understanding |

## Exam Scenarios

**Extract expense data from receipts** → Pre-built receipt model  
**Extract contact info from business cards** → Pre-built business card model  
**Verify identity from driver's license** → Pre-built ID document model  
**Process vendor invoices for AP** → Pre-built invoice model  
**Extract data from custom org forms** → Train custom model (need 5+ examples)  
**Read text from document (no structure needed)** → Azure AI Vision OCR  
**Analyze sentiment in document** → Azure AI Language service  
**Extract tables with structure intact** → Layout analysis  
**Low confidence score on extraction** → Implement human review workflow  

## Common Exam Traps

❌ **Wrong**: Using OCR when structured extraction is needed → OCR gives raw text, not labeled fields  
✅ **Right**: Use Document Intelligence for forms/documents with fields  

❌ **Wrong**: Training custom model when pre-built model exists → Waste time/resources  
✅ **Right**: Check pre-built models first; custom only for org-specific layouts  

❌ **Wrong**: Using Language service for document field extraction → Language analyzes text content, not document structure  
✅ **Right**: Language for sentiment/entities; Document Intelligence for fields/layout  

❌ **Wrong**: Rejecting all low-confidence extractions → May discard valid data  
✅ **Right**: Route low-confidence to human review; use feedback to improve model
