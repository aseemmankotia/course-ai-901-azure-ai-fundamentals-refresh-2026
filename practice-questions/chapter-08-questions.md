## Chapter 8: Information Extraction with Azure Content Understanding — Practice Questions

**Q1.** A retail company receives thousands of paper receipts daily from field employees for expense reimbursement. They need to automatically extract merchant name, date, total amount, and tax from these receipts to populate their accounting system. Which Azure AI service BEST meets this requirement?

A) Azure AI Vision OCR to read all text from receipts, then use custom code to parse the extracted text
B) Azure AI Language service to analyze entities in the receipt text
C) Azure AI Document Intelligence with the pre-built receipt model to extract structured fields
D) Azure AI Custom Vision to classify receipts by merchant type

<details>
<summary>Answer</summary>

**Correct: C**

Azure AI Document Intelligence's pre-built receipt model is specifically designed to extract structured fields (merchant name, date, total, tax, line items) from receipts. It understands receipt structure and returns labeled key-value pairs, eliminating custom parsing logic.

**Why the others are wrong:**
- OCR only reads text without understanding document structure or field labels. You'd need complex custom parsing code to identify which text is the merchant vs total vs date, which is error-prone and maintenance-heavy.
- Azure AI Language analyzes language patterns (sentiment, key phrases, entities) but doesn't extract structured document fields with labels. It's for natural language understanding, not form/document structure extraction.
- Custom Vision is for image classification (e.g., classifying receipt vs invoice), not extracting structured data fields from documents. It would only tell you 'this is a receipt' but not extract the merchant name or total.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A healthcare provider needs to process patient intake forms that have a unique layout specific to their clinic. The forms contain custom fields like 'Emergency Contact Relationship' and 'Preferred Pharmacy Name' that are not in standard forms. What approach should they use?

A) Use Azure AI Document Intelligence pre-built general document model, which handles all form types
B) Use the pre-built ID card model since it extracts personal information
C) Train a custom Azure AI Document Intelligence model using labeled examples of their specific intake forms
D) Use Azure AI Vision OCR and manually map extracted text to database fields

<details>
<summary>Answer</summary>

**Correct: C**

Custom models in Azure AI Document Intelligence are designed for documents with organization-specific layouts and fields. You provide 5+ labeled examples of your forms, and the service trains a model to extract your custom fields accurately. This is the exact scenario for custom models.

**Why the others are wrong:**
- The general document model extracts generic elements (text, tables, key-value pairs) but doesn't understand custom field semantics like 'Emergency Contact Relationship'. It won't label fields with your specific terminology.
- The pre-built ID card model is trained on government-issued IDs (driver's licenses, passports) and extracts standard ID fields (name, DOB, address, document number). It won't recognize custom clinic intake form fields.
- OCR extracts text but provides no structure or field labeling. You'd need to write and maintain complex parsing logic to map text positions to database fields, which breaks when form layout changes slightly.

</details>

---

**Q3.** An accounts payable team uses Azure AI Document Intelligence to process vendor invoices. The system extracts vendor name, invoice number, date, and total amount. The extracted 'Total Amount' field shows a confidence score of 0.62. What does this indicate?

A) The total amount extracted is 62% of the actual invoice total
B) The model is 62% confident in its extraction; human review is recommended for accuracy-critical scenarios
C) The invoice processing will fail and the document must be resubmitted
D) The extraction took 62 milliseconds to complete

<details>
<summary>Answer</summary>

**Correct: B**

Confidence scores in Azure AI Document Intelligence range from 0.0 to 1.0 and indicate the model's certainty in the extraction. 0.62 (62%) is moderate confidence, suggesting the field may be ambiguous or partially obscured. Best practice: set a threshold (e.g., 0.85) and route low-confidence extractions to human review queues.

**Why the others are wrong:**
- Confidence scores measure extraction certainty, not the numeric value of the extracted data. The model extracts the full amount it detected; the score indicates how sure it is that extraction is correct.
- Low confidence doesn't cause processing failure. The service returns the extraction with its confidence score, and your application logic decides whether to accept it, flag it for review, or reject it based on your threshold.
- Confidence scores are not performance metrics. Processing time is measured separately in milliseconds and is unrelated to extraction accuracy confidence.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** A government agency needs to digitize driver's licenses to verify citizen identity during online applications. They need to extract name, date of birth, license number, address, and expiration date. Which solution should they implement?

A) Azure AI Document Intelligence pre-built ID document model to extract identity fields from driver's licenses and passports
B) Azure AI Vision OCR to read text from licenses, then use regex patterns to extract fields
C) Train a custom Azure AI Document Intelligence model on government ID examples
D) Use Azure AI Language service to extract named entities (person, location, date) from license text

<details>
<summary>Answer</summary>

**Correct: A**

The pre-built ID document model is specifically trained on government-issued IDs (driver's licenses, passports, ID cards) and extracts standard identity fields: name, DOB, document number, address, expiration date, country/region. It understands ID layouts globally and returns structured, labeled fields.

**Why the others are wrong:**
- OCR extracts raw text without understanding which text is the name vs license number vs address. Regex patterns are brittle (break with format variations across states/countries) and require extensive maintenance as ID formats change.
- Custom models are for organization-specific documents. Government IDs follow standard formats that the pre-built model already handles. Training a custom model wastes time and resources when a pre-built solution exists.
- Language service extracts generic entities (any person name, any location, any date) from text but doesn't understand document structure or label fields as 'license holder name' vs 'issuing authority'. It's for analyzing language content, not structured document extraction.

</details>

---

**Q5.** A logistics company processes shipping manifests that contain tables with columns: Item Code, Description, Quantity, Weight, Destination. They need to extract this table data while preserving the row-column structure. Which Azure AI Document Intelligence capability should they use?

A) Key-value pair extraction to identify field labels and values
B) Layout analysis to extract tables with row and column structure preserved
C) Pre-built invoice model since it handles line items
D) OCR to read table text, then reconstruct the table in code

<details>
<summary>Answer</summary>

**Correct: B**

Layout analysis in Azure AI Document Intelligence extracts tables as structured data with rows, columns, and cells identified. It returns table content in JSON with row/column indices, preserving spatial relationships. This is the core capability for extracting tabular data from documents.

**Why the others are wrong:**
- Key-value pairs extract labeled fields (e.g., 'Invoice Number: 12345') but don't handle multi-row tabular data. Tables have repeating column headers and rows, which is a different structure than single key-value fields.
- The invoice model extracts line items (description, quantity, price) from invoices specifically, but shipping manifests have different columns (Item Code, Weight, Destination). Also, the scenario asks for general table extraction capability, not invoice-specific fields.
- OCR provides text with bounding boxes but doesn't identify table structure (which texts belong to same row/column). Reconstructing tables from raw OCR output requires complex spatial analysis code that's error-prone with merged cells or varied layouts.

</details>

---

**Q6.** A sales team wants to digitize business cards collected at trade shows. They need to extract contact name, job title, company name, email, and phone number to import into their CRM. The business cards have varied layouts and designs. What is the MOST efficient approach?

A) Train a custom model on examples of business cards from past trade shows
B) Use Azure AI Vision OCR followed by Azure AI Language entity extraction
C) Use Azure OpenAI GPT-4 with vision capabilities to analyze business card images
D) Use Azure AI Document Intelligence pre-built business card model to extract contact fields

<details>
<summary>Answer</summary>

**Correct: D**

The pre-built business card model is specifically designed for business cards with varied layouts. It's trained on thousands of business card designs and extracts standard contact fields: names, job titles, companies, emails, phone numbers, addresses, websites. Most efficient solution—no training required.

**Why the others are wrong:**
- Custom models require labeling 5+ examples and training time. Since business cards are a common document type with standard fields, a pre-built model already exists. Custom models are for organization-specific documents, not industry-standard formats.
- OCR extracts text without labeling which text is the name vs company vs email. Language entity extraction finds generic entities (any person name, any organization) but doesn't map them to business card roles (whose name? which company?). This combination lacks structure.
- While GPT-4 Vision can analyze images, it's overkill for structured extraction that Document Intelligence handles natively. It's also more expensive per request and requires prompt engineering. Use specialized services for structured document extraction.

</details>

---

**Q7.** A university needs to process student transcripts from 50 different universities, each with unique formats. Some transcripts are PDFs, others are scanned images. They need to extract course names, grades, and credit hours. The university has 20 sample transcripts from each institution. What is the BEST approach?

A) Use the pre-built invoice model since transcripts have line items like invoices
B) Use Azure AI Vision OCR to extract all text, then use Azure OpenAI to parse the structure
C) Use the pre-built general document model to extract all key-value pairs from transcripts
D) Train 50 separate custom Azure AI Document Intelligence models, one for each university's transcript format

<details>
<summary>Answer</summary>

**Correct: D**

Each university has a unique transcript layout, which is exactly the scenario for custom models. With 20 samples per institution (well above the 5 minimum), you can train 50 custom models. At runtime, identify the source university and route to the correct model. This provides accurate extraction for each specific format.

**Why the others are wrong:**
- Invoice models extract vendor info, line items, and totals—fields specific to invoices. Transcripts have different semantics (courses, grades, GPAs, semesters) and layouts (multi-semester tables, cumulative statistics). Wrong pre-built model for the document type.
- OCR + LLM can work but is less accurate and more expensive than purpose-built document extraction. LLMs may hallucinate data or misinterpret complex table structures. Document Intelligence with trained models provides deterministic, traceable extraction with confidence scores.
- General document model extracts generic key-value pairs but doesn't understand transcript-specific semantics (which text is a course name vs grade vs credit hours). With 20 samples per format, custom models will significantly outperform the general model.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** A company is deciding between Azure AI Vision OCR and Azure AI Document Intelligence for processing forms. Which statement BEST describes when to use each service?

A) Use OCR for extracting structured fields with labels; use Document Intelligence for reading text from images
B) Use Document Intelligence for extracting structured, labeled fields from documents; use OCR for reading text without structure
C) Both services provide identical capabilities; the choice depends only on pricing
D) Use OCR for digital PDFs; use Document Intelligence for scanned images

<details>
<summary>Answer</summary>

**Correct: B**

This is a key exam distinction: OCR reads text and returns it with positions (bounding boxes) but no semantic understanding of document structure or field labels. Document Intelligence understands document layout and extracts structured data (e.g., 'Invoice Number: 12345' labeled as key-value pair). If you need labeled, structured fields—use Document Intelligence.

**Why the others are wrong:**
- This is exactly backwards. OCR is for text reading only. Document Intelligence (formerly Form Recognizer) is specifically designed for structured field extraction with labels and document understanding.
- The services have different purposes: OCR for text reading, Document Intelligence for structured extraction. Pricing is a secondary consideration after determining which service meets your technical requirements.
- Both services handle digital PDFs and scanned images. The distinction is output structure, not input format. OCR outputs raw text; Document Intelligence outputs labeled, structured fields with confidence scores and layout analysis.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

