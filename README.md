# 🛡️ Arabic NLP & Web Security with DistilBERT
 
> Fine-tuned **DistilBERT** models applied to two domains: (1) **Extractive Question Answering** on Quranic Arabic passages, and (2) **Web Attack Detection** (XSS & SQL Injection) with ~94% classification accuracy.
 
---
 
## 📌 Project Overview
 
This repository contains a Jupyter notebook demonstrating the fine-tuning and evaluation of DistilBERT for security and Arabic NLP tasks. It was developed as part of the **AI Engineering graduation research** at Alamein International University.
 
DistilBERT was chosen for its balance of speed and accuracy — 40% fewer parameters than BERT while retaining ~97% of its performance — making it suitable for both real-time inference (security) and research-grade NLP (Arabic QA).
 
---
 
## ✨ Key Results
 
| Task | Model | Accuracy / Score |
|---|---|---|
| Web Attack Detection (XSS + SQLi) | DistilBERT fine-tuned | **~94%** |
| Arabic Extractive QA (Quran) | DistilBERT-multilingual | Competitive F1 vs AraBERT |
 
---
 
## 🧠 Tasks Covered
 
### 1. Web Attack Detection
Classifies HTTP request payloads as `BENIGN`, `XSS`, or `SQL_INJECTION` using a fine-tuned DistilBERT text classifier. Payloads are tokenized and passed through the transformer for multi-class prediction.
 
**Why transformers over regex/rules?**
Transformer models generalize to obfuscated, encoded, and novel attack variants that rule-based WAFs (Web Application Firewalls) miss.
 
### 2. Quranic Extractive Question Answering
An extractive QA pipeline for Arabic — given a passage from the Quran and a question, the model extracts the answer span directly from the text. Evaluated against AraBERT, MARBERT, GPT-2, and T5 baselines.
 
---
 
## 🛠️ Technologies Used
 
| Category | Tool |
|---|---|
| Model | `distilbert-base-uncased` / `distilbert-base-multilingual-cased` |
| Framework | PyTorch + Hugging Face Transformers |
| Environment | Jupyter Notebook / Google Colab |
| Data Processing | Pandas, NumPy |
| Evaluation | Scikit-learn (classification_report, F1, accuracy) |
 
---
 
## 📁 Repository Structure
 
```
distilbert-arabic-nlp-security/
├── Untitled23_(2).ipynb     # Main notebook: fine-tuning, evaluation, results
└── README.md
```
 
---
 
## 🚀 Getting Started
 
### Prerequisites
```bash
pip install transformers torch datasets scikit-learn pandas numpy
```
 
### Run the Notebook
 
1. Clone the repository:
   ```bash
   git clone https://github.com/AbdelrahmanHaleem/distilbert-arabic-nlp-security.git
   cd distilbert-arabic-nlp-security
   ```
 
2. Launch Jupyter:
   ```bash
   jupyter notebook
   ```
 
3. Open `Untitled23_(2).ipynb` and run all cells.
 
> **Tip:** For faster training, open the notebook in **Google Colab** and enable GPU runtime (`Runtime > Change runtime type > T4 GPU`).
 
---
 
## 📊 Evaluation Metrics
 
The notebook reports the following per classification task:
- Accuracy
- Precision, Recall, F1-score (per class)
- Confusion matrix visualization
 
---
 
## 🔮 Future Work
 
- Deploy the attack detection model as a FastAPI middleware endpoint
- Extend QA dataset with more Quranic suras and hadith collections
- Benchmark against larger models (AraBERT, CAMeL-BERT)
- Add explainability layer (SHAP/LIME) for security audit logging
 
---
 
## 👤 Author
 
**Abdelrahman Ahmed Haleem**
AI Engineering Graduate, Alamein International University (2025)
Arabic NLP Research Intern, SRTA-City (Summer 2024)
 
[LinkedIn](https://www.linkedin.com/in/haleem1) | [GitHub](https://github.com/AbdelrahmanHaleem)
