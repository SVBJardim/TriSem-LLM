# TriSem-LLM: Multi-Criteria Semantic Screening of Scientific Articles

## Overview

TriSem-LLM is a semi-automated pipeline for screening scientific articles based on their relevance to a research question.

It combines multiple complementary signals:

- Keyword matching (lexical signal)
- Abstract-level semantic similarity
- Full-text semantic similarity (segment-based)
- LLM-based metadata correction (title refinement)

The approach follows a **no early exclusion strategy**, preserving recall while enabling a transparent and reproducible selection process.

---

## Objective

To support systematic literature reviews by identifying relevant articles through a **multi-criteria decision framework**, reducing manual effort while maintaining interpretability.

---

## 📂 Repository Structure

```
TriSem-LLM/
│
├── notebook.ipynb
├── README.md
├── requirements.txt
├── .gitignore
│
├── data/
│   ├── extracted_articles.csv
│   ├── relevant_articles.csv
│   └── duplicate_file_pairs.csv
```

---

## How to Run (Google Colab)

1. Open the notebook in Google Colab

2. Install dependencies:

```python
!pip install -r requirements.txt
```

3. Mount Google Drive (optional):

```python
from google.colab import drive
drive.mount('/content/drive')
```

4. Set API key:

```python
import os
os.environ["TOGETHER_API_KEY"] = "your_api_key_here"
```

5. Run all cells sequentially

---

## Data Availability

- Full-text PDFs are **not included** due to copyright restrictions
- Only extracted metadata and results are provided

---

## Outputs

- extracted_articles.csv → full metadata (~700 articles)
- relevant_articles.csv → filtered relevant subset
- duplicate_file_pairs.csv → detected duplicates

---

## Methodological Contributions

- Multi-signal relevance assessment
- No early exclusion strategy (recall preservation)
- Segment-based full-text similarity
- Transparent decision traceability

---

## Notes

- The pipeline is designed to be **reproducible and extensible**
- Works on CPU (GPU optional)
- Designed for systematic review workflows

---

## License

This project is licensed under the MIT License.
