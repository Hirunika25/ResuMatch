# ResuMatch
### Explainable CV–Job Matching System

## 1.Project Overview

This project implements a **CV (resume) to job description matching system** using modern NLP techniques.  
It compares multiple approaches — *Doc2Vec, pure SBERT, and a hybrid SBERT + skills scoring model* — and adds explainability (XAI) to show **why** a match was made.

The goal is to automate candidate screening and provide understandable match results for recruiters and job seekers.

---

## 2.Approaches Included

| Model | Description |
|-------|-------------|
| **Doc2Vec** | Classical document embedding baseline |
| **SBERT (pure)** | Transformer‑based semantic embedding and cosine similarity |
| **Hybrid SBERT** | SBERT + skill extraction + weighted scoring |
| **XAI component** | Sentence/skill contribution explanations |

---

## 3.Datasets Used

### 3.1 Resume/CV Data

- **Resume Dataset (Snehaan Bhawal)** — ~2400 resumes in PDF/text form (Kaggle). :contentReference[oaicite:8]{index=8}  
- Multiple resume dataset variants on Kaggle for diversified CV data. :contentReference[oaicite:9]{index=9}  
- **Structured resume dataset (~54k)** containing parsed resume fields. :contentReference[oaicite:10]{index=10}

### 3.2 Job Description Data

- **Data Science Job Postings & Skills (2024)** — with skills and job details. :contentReference[oaicite:11]{index=11}  
- **LinkedIn Data Scientist job postings** — for domain‑specific evaluation. :contentReference[oaicite:12]{index=12}  
- **General job posting datasets** for broader job matching tests. :contentReference[oaicite:13]{index=13}

---


## 4.Features

1. Semantic similarity matching (SBERT)  
2. Hybrid scoring with skill overlap  
3. Explainability (top skills and phrase contributions)  
4. Evaluation and comparison of models  
5. Examples with similarity scores

---

## 5.Installation

```bash
git clone <your‑repo‑url>
cd cv‑job‑matching
pip install -r requirements.txt  
```


---
## 6.Folder Strucutre

```bash
cv-job-matching-nlp/
├── data/
│   ├── cvs/                 # resume files
│   ├── jobs/                # job posting files
│   └── skills.json          # skill dictionary
├── notebooks/               # analysis notebooks
├── src/                     # Python modules
├── results/                 # saved matches and metrics
├── README.md
├── requirements.txt
└── LICENSE
```
---

## 7.Model Training & Matching

1. Preprocess CVs and job descriptions
2. Train models (Doc2Vec / SBERT)
3. Infer embeddings and compute similarity
4. Combine SBERT with skill scoring
5. Visualize and explain matches


---
## 8.Future Work

1. LLM‑based matching (GPT embeddings)
2. Real‑time job feed integration
3. Improve skill extraction with NER