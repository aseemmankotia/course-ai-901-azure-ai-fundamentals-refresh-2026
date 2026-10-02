# Computer Vision & Image Generation Cheat Sheet

## Image Analysis Capabilities

| Capability | Input | Output | Use Case | Exam Keyword |
|------------|-------|--------|----------|-------------|
| **Image Classification** | Image | ONE category label | Categorize entire image into predefined classes | "Assign category", "Classify as" |
| **Object Detection** | Image | Multiple objects + bounding boxes + confidence | Locate and identify multiple items in image | "Count objects", "Locate items", "Bounding box" |
| **OCR** | Image/Document | Extracted text (printed, handwritten, tables) | Extract text from documents, forms, images | "Read text", "Extract from form" |
| **Facial Detection** | Image | Face locations + attributes (age, emotion) | Find faces, estimate attributes—NO identity | "Detect faces", "Estimate age" |
| **Facial Recognition** | 2 images | Match score (1:1 verification) | Verify person matches their photo | "Verify identity", "Compare photos" |
| **Facial Identification** | 1 image + database | Best match from N people (1:N search) | Find person in database | "Search database", "Identify person" |
| **Text-to-Image Generation** | Text prompt | Generated image | Create visuals from descriptions | "Generate image", "Create from prompt" |
| **Computer Vision API** | Image | Tags, description, brands, objects | Analyze existing image content | "Analyze image", "Generate tags" |

## OCR Capabilities & Limitations

| Content Type | Accuracy | Notes | Exam Trap |
|--------------|----------|-------|----------|
| **Printed text** | 95%+ | High reliability | Assume works unless stated otherwise |
| **Handwritten text** | 70-90% | Lower accuracy, needs specialized models | Requires review workflow—never 100% |
| **Simple tables** | 85-95% | Rows/columns with clear borders | Structure extraction supported |
| **Complex tables** | 60-80% | Nested, merged cells, irregular layout | Expect errors—manual review needed |
| **Forms** | 80-90% | Checkboxes, fields, key-value pairs | Built-in form understanding |

## Facial Analysis: Regulatory Tiers

| Type | Definition | Regulation Level | Consent Required | Exam Focus |
|------|------------|-----------------|------------------|------------|
| **Detection** | Find faces + attributes | Low—general computer vision | No (no identity) | Not regulated like recognition |
| **Recognition (1:1)** | Compare 2 specific photos | Medium—privacy laws apply | Yes—explicit consent | GDPR, CCPA compliance required |
| **Identification (1:N)** | Search 1 face in database | High—heavily restricted | Yes + legal authority | Often banned/limited by jurisdiction |

**Exam Rule:** 1:1 = verification (recognition), 1:N = search (identification). Identification has stricter regulations.

## Computer Vision API: Key Features

**Returns:**
- **Tags:** Keywords describing image content ("outdoor", "person", "sky")
- **Description:** Full sentence describing the scene
- **Objects:** Items detected with bounding boxes
- **Brands:** Commercial logos/brands identified
- **Categories:** Broad classification ("outdoor_mountain", "food_")
- **Adult content:** Flags for inappropriate content

**Does NOT:**
- Generate new images (use text-to-image models)
- Identify specific people (use facial recognition)
- Extract text (use OCR)

## Vision Model Limitations

| Limitation | Impact | Mitigation | Exam Scenario |
|------------|--------|------------|---------------|
| **Training data bias** | Misinterprets underrepresented cultures/contexts | Test with diverse datasets | Cultural content misclassified |
| **Contextual errors** | Lacks human understanding of scene context | Manual review for critical decisions | "Costume party" vs "wedding" |
| **Regional variations** | Trained primarily on Western/US data | Validate with target region data | International product misidentified |
| **Confidence scores** | Not 100% certain—probabilistic | Set appropriate thresholds | Low confidence requires review |

## Decision Matrix

**Need to categorize whole image into ONE class?** → Image Classification

**Need to find and count multiple objects with locations?** → Object Detection

**Need to extract text from document/image?** → OCR

**Need to verify person matches their photo (2 images)?** → Facial Recognition (1:1) + consent

**Need to search for person in database (1 image vs N)?** → Facial Identification (1:N) + heavy regulations

**Need to create new image from text?** → Text-to-Image Generation (DALL-E, Stable Diffusion)

**Need to analyze existing image content?** → Computer Vision API

## Exam Tips

✅ **Heavily Tested:**
- Classification vs Detection: when to use each
- OCR printed vs handwritten accuracy
- 1:1 (recognition) vs 1:N (identification) + regulations

⚠️ **Common Mistakes:**
- Using detection when classification is sufficient (overcomplexity)
- Expecting 100% OCR accuracy on handwriting
- Confusing facial detection (attributes) with recognition (identity)
- Thinking all facial analysis is equally regulated

🔑 **Keywords:**
- "Multiple objects" + "locate" = Object Detection
- "Categorize entire image" = Image Classification
- "Extract text" = OCR
- "Verify identity" = Facial Recognition
- "Search database" = Facial Identification (heavy regulation)
- "Generate image" = Text-to-Image models
