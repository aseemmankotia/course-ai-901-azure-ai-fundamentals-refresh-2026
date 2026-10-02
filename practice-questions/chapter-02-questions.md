## Chapter 2: Responsible AI Principles and Scenario Application — Practice Questions

**Q1.** A healthcare company is developing an AI system to predict patient readmission risk. During testing, they discover the model recommends fewer follow-up appointments for patients from certain ethnic neighborhoods, even when clinical indicators are similar. Which Responsible AI principle is MOST violated?

A) Fairness - because the model treats different demographic groups inequitably based on protected characteristics
B) Transparency - because the model's decision-making process isn't explained to patients
C) Privacy and security - because the model uses sensitive health data without proper consent
D) Accountability - because no human review process exists for the recommendations

<details>
<summary>Answer</summary>

**Correct: A**

Fairness is violated when AI systems treat people or groups inequitably. The model shows disparate treatment based on demographic characteristics (ethnic neighborhoods) despite similar clinical indicators, which is the definition of bias and unfair treatment.

**Why the others are wrong:**
- Transparency issues would involve not explaining how decisions are made, but the primary violation here is the biased treatment itself, not the explanation
- Privacy violations would involve unauthorized data collection or inadequate protection of personal data, which isn't the issue described
- Accountability concerns human oversight, but the core problem is the biased algorithm producing inequitable outcomes, not the review process

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A retail company wants to deploy a chatbot that collects customer payment information. To comply with Responsible AI privacy and security principles, which combination of controls is MOST appropriate?

A) Store all conversation logs in plaintext for quality assurance and use role-based access control for the database
B) Use a public cloud storage service with default settings and require customers to consent to data collection
C) Encrypt payment data at rest and in transit, implement access controls, and avoid storing full payment card numbers
D) Allow all developers to access production data for debugging and implement audit logging

<details>
<summary>Answer</summary>

**Correct: C**

Privacy and security principles require protecting personal data through encryption (at rest and in transit), implementing proper access controls, and minimizing sensitive data storage. Not storing full payment card numbers follows data minimization principles.

**Why the others are wrong:**
- Storing sensitive payment information in plaintext violates encryption requirements even with access controls
- Default settings typically don't provide adequate security for sensitive data, and consent alone doesn't satisfy technical protection requirements
- Allowing broad developer access to production payment data violates principle of least privilege and creates unnecessary security risk

</details>

---

**Q3.** An AI-powered resume screening system consistently ranks candidates with employment gaps lower, which disproportionately affects women who took parental leave. The company claims the model is 'objective' because it only uses employment history data. Which statement BEST describes this situation?

A) The system violates fairness principles because the training data and feature selection perpetuate historical bias
B) The system is fair because it applies the same criteria to all candidates equally
C) The system demonstrates good transparency because the ranking criteria are clearly defined
D) The system meets reliability standards because it consistently produces the same results

<details>
<summary>Answer</summary>

**Correct: A**

Fairness requires equitable treatment of all groups. Even when applying consistent rules, if the training data reflects historical biases or the features chosen (employment gaps) disproportionately impact protected groups, the system violates fairness principles. Equal treatment doesn't guarantee equitable outcomes.

**Why the others are wrong:**
- Applying the same biased criteria equally still produces unfair outcomes - fairness requires equity, not just equality of process
- Transparency is about explaining decisions, but knowing how an unfair system works doesn't make it fair
- Reliability means consistent performance, but consistently biased results aren't acceptable - consistency doesn't equal fairness

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** A financial services company is deploying an AI loan approval system. To satisfy the Accountability principle, what should they implement?

A) Train the model on diverse historical data and monitor for bias metrics
B) Provide clear explanations of how the model makes decisions to loan applicants
C) Encrypt all customer financial data and implement multi-factor authentication
D) Establish human review processes for decisions and assign responsibility for outcomes to specific roles

<details>
<summary>Answer</summary>

**Correct: D**

Accountability means humans remain responsible for AI decisions. This requires human oversight processes (human review) and clear assignment of responsibility to specific people or roles who can be held accountable for system outcomes and errors.

**Why the others are wrong:**
- Training on diverse data and monitoring bias addresses Fairness, not Accountability
- Providing explanations addresses Transparency, not Accountability (who is responsible)
- Encryption and authentication address Privacy and Security, not Accountability

</details>

---

**Q5.** An AI system for diagnosing skin conditions performs with 95% accuracy on light skin tones but only 70% accuracy on darker skin tones. The training dataset contained 90% images of light skin. Which action BEST addresses the Fairness violation?

A) Collect additional images of darker skin tones and retrain the model to achieve balanced performance across all skin tones
B) Document the accuracy difference in the user manual so doctors are aware of the limitation
C) Add a confidence score to predictions so users know when the system is uncertain
D) Implement access controls to ensure only certified dermatologists use the system

<details>
<summary>Answer</summary>

**Correct: A**

Fairness violations due to biased training data are fixed by collecting representative data and retraining. The root cause is the imbalanced dataset (90% light skin), so fixing fairness requires balanced training data to achieve equitable performance across all groups.

**Why the others are wrong:**
- Documenting the bias addresses Transparency but doesn't fix the Fairness problem - the system still performs inequitably
- Confidence scores improve Transparency and might help with Reliability but don't address the underlying fairness issue of disparate performance
- Access controls address security and potentially accountability but don't fix the biased model performance

</details>

---

**Q6.** A city is deploying an AI surveillance system for public safety. To meet the Transparency principle, what is MOST important?

A) Encrypt all video footage and restrict access to authorized law enforcement only
B) Ensure the system performs equally well in all neighborhoods regardless of demographics
C) Publicly disclose what data is collected, how the AI analyzes it, and how decisions are made
D) Establish a process for citizens to appeal decisions made by the AI system

<details>
<summary>Answer</summary>

**Correct: C**

Transparency means users and affected parties should understand how AI systems work and make decisions. This requires disclosing what data is collected, how it's processed, and how the AI makes decisions so people understand the system's operation.

**Why the others are wrong:**
- Encryption and access controls address Privacy and Security, not Transparency
- Equal performance across demographics addresses Fairness, not Transparency
- Appeal processes address Accountability, not Transparency (though transparency helps accountability)

</details>

---

**Q7.** An AI-powered voice assistant is being designed for elderly users. Many potential users have hearing impairments or mobility limitations. Which Responsible AI principle is MOST directly addressed by providing text-based alternatives and large button interfaces?

A) Reliability and safety - ensuring the system performs consistently for all users
B) Fairness - treating all age groups equitably in feature availability
C) Inclusiveness - designing the system to empower and engage people of all abilities
D) Transparency - making the interface easier to understand

<details>
<summary>Answer</summary>

**Correct: C**

Inclusiveness specifically means designing AI systems to empower and engage all people regardless of physical abilities, cognitive capabilities, or other characteristics. Providing text alternatives for hearing impairments and large buttons for mobility limitations directly addresses inclusiveness.

**Why the others are wrong:**
- Reliability is about consistent performance and error handling, not about accommodating different abilities
- Fairness is about equitable treatment of groups and avoiding bias, not about accessibility features for different abilities
- Transparency is about understanding how the system works, not about accessibility features (though clear interfaces can aid both)

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** A company's AI customer service bot occasionally provides incorrect information about product returns, causing customer frustration and financial losses. Which Responsible AI principle should be prioritized to address this issue?

A) Fairness - ensure all customers receive the same quality of service
B) Inclusiveness - make the bot accessible to customers with different technical skills
C) Privacy and security - protect customer data during interactions
D) Reliability and safety - improve the system to perform consistently and handle errors gracefully

<details>
<summary>Answer</summary>

**Correct: D**

Reliability and safety means AI systems should perform consistently, accurately, and safely, including handling errors gracefully. Providing incorrect information indicates reliability problems that need to be fixed through better training, validation, or fallback mechanisms.

**Why the others are wrong:**
- Fairness addresses equitable treatment of different groups, but the issue here is accuracy and consistency for all users, not disparate treatment
- Inclusiveness addresses accessibility for people with different abilities, not accuracy of information provided
- Privacy and security address data protection, but the issue is incorrect information, not data breaches

</details>

---

