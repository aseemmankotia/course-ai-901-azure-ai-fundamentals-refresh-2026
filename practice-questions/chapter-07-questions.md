## Chapter 7: Computer Vision and Image Generation in Foundry — Practice Questions

**Q1.** A retail company needs to automatically categorize product images uploaded by sellers into predefined departments: Electronics, Clothing, Home & Garden, or Toys. The system should assign exactly one category per image. Which AI capability BEST meets this requirement?

A) Image classification to assign each image to one of the predefined categories
B) Object detection to identify all products in each image and assign multiple categories
C) OCR to extract product labels and categorize based on text content
D) Facial detection to identify people using the products and infer categories

<details>
<summary>Answer</summary>

**Correct: A**

Image classification categorizes an entire image into one of several predefined classes. This matches the requirement: one image → one category from a fixed set of options (Electronics, Clothing, etc.).

**Why the others are wrong:**
- Object detection locates and identifies multiple objects with bounding boxes—overkill when you only need one category for the whole image, not locations of individual items
- OCR extracts text from images but requires readable text labels—most product photos don't have clear text, and the requirement is visual categorization not text extraction
- Facial detection identifies faces in images—irrelevant to categorizing product types; products may not even show people

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A security application monitors parking lot footage and needs to count how many vehicles are present, identify their types (car, truck, motorcycle), and mark their locations with coordinates. Which capability should be implemented?

A) Image classification to categorize the parking lot as 'empty', 'partial', or 'full'
B) Object detection to locate and identify each vehicle with bounding boxes
C) OCR to read license plate numbers and vehicle identification
D) Computer Vision tagging to generate descriptive tags like 'outdoor', 'vehicles', 'parking'

<details>
<summary>Answer</summary>

**Correct: B**

Object detection locates multiple objects within an image, provides bounding box coordinates, identifies object types, and returns confidence scores—exactly what's needed to count vehicles, identify their types, and mark locations.

**Why the others are wrong:**
- Image classification assigns one label to the entire image—can't count individual vehicles or provide their locations, only categorize the overall scene
- OCR extracts text from images—useful for license plates but doesn't locate or count vehicles; requires separate vehicle detection first
- Computer Vision tagging generates descriptive keywords for the image but doesn't provide object counts, types, or precise locations—too general for this requirement

</details>

---

**Q3.** A document processing system needs to extract text from scanned invoices that contain printed headers, handwritten notes in margins, and structured tables with line items. What are the key OCR capabilities and limitations for this scenario?

A) OCR can extract printed text and tables with high accuracy; handwritten text has lower accuracy and may require specialized models; table structure extraction is supported but complex layouts may have errors
B) OCR only works on printed text; handwritten content cannot be extracted and must be manually entered; tables are treated as plain text without structure
C) OCR extracts all text with equal accuracy regardless of format; handwriting and print are processed identically; tables are always perfectly structured
D) OCR requires images to be converted to PDF first; it cannot process handwriting or tables; only single-column printed text is supported

<details>
<summary>Answer</summary>

**Correct: A**

This accurately describes OCR capabilities: printed text has high accuracy, handwritten text has lower accuracy and may need specialized models, table extraction is supported but complex layouts can cause errors—all real limitations teams must plan for.

**Why the others are wrong:**
- Modern OCR can process handwritten text (though with lower accuracy than print)—it's not impossible, just less reliable; table structure extraction is a standard feature
- Handwriting and print have different accuracy rates due to variability in handwriting—treating them as equal ignores real performance differences; perfect table extraction is unrealistic with complex layouts
- OCR works on various image formats directly, not just PDF; modern OCR handles handwriting and tables—these aren't unsupported features; multi-column layouts are supported

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** An event management app needs to verify that a person checking in matches their registration photo (comparing two specific photos). Which capability is required and what regulatory constraints apply?

A) Facial identification (1:N search) to find the person in a database; minimal regulation since it's for event security
B) Facial recognition (1:1 verification) to compare two specific images; subject to privacy regulations and requires explicit consent
C) Facial detection to confirm a face is present in both photos; no special regulations apply
D) Object detection to locate and match facial features; exempt from facial recognition regulations

<details>
<summary>Answer</summary>

**Correct: B**

Comparing two specific photos is 1:1 verification = facial recognition. This is regulated technology requiring explicit consent, proper data handling, and compliance with privacy laws (GDPR, CCPA, etc.). The scenario matches this exactly.

**Why the others are wrong:**
- Facial identification is 1:N (searching one face against a database)—this scenario is 1:1 (comparing two known photos); identification has even stricter regulations, not minimal ones
- Facial detection only identifies that faces exist and their locations—it doesn't compare or verify identity; regulations apply when comparing faces for identification purposes
- Object detection locates objects generically—using it to match facial features for identity verification still constitutes facial recognition and falls under the same regulations

</details>

---

**Q5.** A law enforcement agency wants to search for a suspect by comparing a single photo against a database of 50,000 known individuals. What type of facial analysis is this, and what are the key considerations?

A) Facial recognition (1:1) with standard privacy consent requirements
B) Facial identification (1:N search) which is heavily regulated, often restricted, and requires legal authority and strict data governance
C) Facial detection which identifies faces but requires additional recognition capability
D) Object detection applied to faces with minimal regulatory constraints

<details>
<summary>Answer</summary>

**Correct: B**

Searching one face against a database of many is 1:N = facial identification. This is heavily regulated, often restricted or banned in certain jurisdictions, requires legal authority for law enforcement use, and demands strict data governance. Many jurisdictions limit or prohibit this use.

**Why the others are wrong:**
- Facial recognition is 1:1 verification (comparing two specific images)—this scenario is 1:N (searching against a database); regulations are stricter for 1:N identification
- Facial detection only identifies presence and location of faces—it doesn't compare or search for identity matches; this scenario requires identification capability
- Object detection doesn't compare faces for identity—using it for identity matching is still facial identification and subject to the same heavy regulations

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** A marketing team needs to generate product visualization images from text descriptions like 'modern minimalist chair in a bright living room with plants' for A/B testing ad campaigns. Which AI capability is appropriate?

A) Computer Vision API to analyze existing chair images and generate descriptions
B) Image classification to categorize furniture styles and room types
C) Text-to-image generation models (DALL-E, Stable Diffusion) to create visuals from text prompts
D) OCR to extract text from furniture catalogs and create matching images

<details>
<summary>Answer</summary>

**Correct: C**

Text-to-image generation models like DALL-E and Stable Diffusion create new images from text prompts—exactly what's needed to generate product visualizations from descriptions for A/B testing without photographing actual products.

**Why the others are wrong:**
- Computer Vision API analyzes existing images and generates descriptions (image → text)—this scenario needs the opposite (text → image); it doesn't create new images
- Image classification categorizes existing images into predefined classes—it doesn't generate new images from text descriptions; wrong direction entirely
- OCR extracts text from images—it doesn't create images from text; completely opposite of what's needed for generating product visualizations

</details>

---

**Q7.** A content moderation system uses Computer Vision API in Foundry to analyze user-uploaded images for tags, descriptions, and brand detection. The system incorrectly tags an image of a traditional Chinese wedding as a 'costume party' and misses culturally significant symbols. What limitation does this demonstrate?

A) Computer Vision API cannot analyze images with people—facial detection must be used separately
B) Vision model accuracy depends on training data; cultural and contextual misinterpretation risks exist when models lack diverse training examples
C) Computer Vision API only works on commercial brands and cannot identify cultural or traditional content
D) The API requires manual tagging of cultural content before it can recognize similar images

<details>
<summary>Answer</summary>

**Correct: B**

Vision models are trained on datasets that may not represent all cultures equally—this leads to misinterpretation of culturally specific content. Accuracy depends on training data diversity. Teams must test with diverse datasets and consider cultural context limitations.

**Why the others are wrong:**
- Computer Vision API can analyze images with people and generate tags/descriptions—facial detection is optional for identity-related features but not required for basic image analysis
- Computer Vision API isn't limited to commercial brands—it analyzes all image content; the issue is training data bias, not a technical restriction on content types
- The API doesn't require manual pre-tagging—it generates tags automatically; the problem is its training data may lack diverse cultural examples, not that it needs manual input

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** A healthcare application needs to process patient intake forms that include checkboxes, handwritten patient notes, and printed prescription details. The system must extract both the structure (which checkboxes are marked) and the text content. Which combination of capabilities is required?

A) Image classification to categorize form types, then OCR to extract all text content including checkbox status and handwritten notes
B) Facial detection to identify patient photos, then object detection to locate checkboxes and text regions
C) Computer Vision API tagging to identify form elements, then manual data entry for accuracy
D) OCR with form and table extraction capabilities to capture structured data (checkboxes, fields) and text content (printed and handwritten)

<details>
<summary>Answer</summary>

**Correct: D**

OCR with form/table extraction capabilities can handle structured elements (checkboxes, form fields) AND text content (printed and handwritten). Modern OCR specifically supports form processing with structure recognition—this is the purpose-built solution.

**Why the others are wrong:**
- Image classification categorizes entire images—it can't extract text or checkbox status; OCR alone can handle both structure and text without needing classification first
- Facial detection and object detection aren't designed for document processing—OCR is the specialized tool for text and form extraction; using vision models for this is inefficient and inaccurate
- Computer Vision tagging generates descriptive keywords—it doesn't extract structured form data or text content; manual entry defeats the purpose of automated processing

</details>

---

