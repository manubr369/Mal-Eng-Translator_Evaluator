# Malayalam–English LLM Translation Evaluation & Linguistic Validation

Professional dataset, quality audit framework, and executive reporting dashboard for evaluating, post-editing, and annotating AI-generated Malayalam–English and English–Malayalam translations. Developed as a portfolio project for AI training, data annotation, and bilingual linguistic validator roles (Welo Data / Outlier / DataAnnotation).

---

## 📌 Project Overview & Scope
* **Total Audited Segments:** 50 parallel translation pairs.
* **Translation Directions:** 
  * English → Malayalam: 40 segments (80%)
  * Malayalam → English: 10 segments (20%)
* **Content Domains Covered:** 
  * Everyday Conversation (`15` segments)
  * Formal Notices & Admin (`10` segments)
  * Numbers, Dates & Medical (`9` segments)
  * Idiomatic Expressions (`8` segments)
  * Technical & UI Instructions (`8` segments)
* **Primary Deliverable:** An enterprise-grade Excel workbook (`Project Ai Training Mal-Eng Translation.xlsx`) featuring an executive summary dashboard (`Summary`) and a granularly annotated dataset (`Project(Translations)`).

---

## 🛠️ Evaluation Methodology & Rubric

Every AI translation was audited against a 4-tier severity verdict rubric and a 9-category error taxonomy:

### 1. Severity Verdicts
* **Correct (`21` segments / `42.0%`):** Accurate and natural. Requires zero post-editing.
* **Minor (`29` segments / `58.0%`):** Comprehensible and full meaning is intact, but reads awkwardly, uses unnatural syntax, or requires post-editing for native fluency.
* **Major (`0` segments / `0.0%`):** Meaning changes, or information is lost or added.
* **Critical (`0` segments / `0.0%`):** Could cause real harm or compliance failure (wrong time, date, number, dosage, or proper name).

### 2. Error Taxonomy (Logged across Minor defects)
* **Fluency: unnatural (`14` instances):** Word-for-word "translationese", redundant pronouns (e.g., *അത്*, *അവരുടെ*), and stiff clause chaining.
* **Terminology (`5` instances):** Non-idiomatic domain words (e.g., *രണ്ടുതവണ* vs. *രണ്ടുനേരം* in medical dosages; *സാധുവായിരിക്കൂ* in commercial promotions).
* **Register (`4` instances):** Overly formal, bookish, or literary Malayalam used for casual English idioms (e.g., *അവസാനിപ്പിക്കാം*, *വെളിപ്പെടുത്തി*).
* **Accuracy: mistranslation (`2` instances):** Literal idiom renderings where natural phrasing differs (e.g., *ബസ് നഷ്ടമായി*).
* **Fluency: grammar (`2` instances):** English passive voice calques (*ലോക്ക് ചെയ്യപ്പെടും*) and Indian English preposition interference (*begin from next Monday*).
* **Script/spelling (`1` instance):** Acronyms left in Latin script instead of Malayalam transliteration (*GST* vs. *ജി.എസ്.ടി.*).
* **Accuracy: addition / omission / number/name:** Fully precise on all numerical values, currencies (₹), dates, and times (`100%` accuracy).

---

## 📊 Key Findings & Insights
* **Zero-Defect Pass Rate:** `42.0%` of the AI-generated translations were production-ready with zero post-editing required.
* **Safety & Core Accuracy:** `0%` Major or Critical defects—confirming that the underlying LLM correctly preserved all numerical data, dates, times, currencies, and proper nouns without hallucination.
* **Primary Failure Modes:** **Fluency: unnatural** (`51.9%` of errors) and **Terminology/Register** (`33.3%` combined) accounted for over `85%` of all post-editing interventions. This demonstrates that LLMs struggle most with regional idiomatic register and natural colloquial syntax rather than raw vocabulary.

---

## 📁 Repository Structure
* `Project Ai Training Mal-Eng Translation.xlsx` — The complete Excel deliverable containing:
  * **Summary Sheet:** Executive KPI scorecard, verdict distribution by direction, error taxonomy breakdown, and domain-wise fine-tuning guidance.
  * **Project(Translations) Sheet:** 50 fully annotated rows featuring `#`, `Direction`, `Category`, `Source text`, `AI translation`, `Verdict`, `Error type`, `Corrected version`, and `Why (Reason for the error)`.

---
*Created by [Manu B R] | Bilingual Linguistic Validator & AI Trainer*
