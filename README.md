# SafeTweet: AI for Cyberbullying Detection on Social Platforms  

## 📌 Overview  
Cyberbullying is a major issue on social media platforms, with harmful effects on mental health and well-being. This project, **SafeTweet**, explores Natural Language Processing (NLP) and Machine Learning (ML) techniques to detect cyberbullying in tweets.  

The project implements and compares multiple models:  
- **Naive Bayes (NB)**  
- **Logistic Regression (LR)** (baseline and tuned)  
- **K-Nearest Neighbors (KNN) with PCA**  
- **DistilBERT (transformer-based model)**  

We evaluate these models using precision, recall, F1-score, and accuracy, with **DistilBERT achieving the best results (87.7% accuracy)** before resource limitations.  

---

## 📂 Repository Structure  
- `cyberbullying.py` – Main implementation (data preprocessing, model training, evaluation)  
- `CSE_256_ANUSHA_RAVICHANDRAN.pdf` – Full project report  
- `README.md` – Project documentation  


---

## 📊 Dataset  
- **Source:** [Kaggle – Cyberbullying Classification](https://www.kaggle.com)  
- **Size:** 47,692 tweets  
- **Classes:** 6 (e.g., age, ethnicity, gender, religion, other, not-cyberbullying)  
- **Binary conversion:** Converted to `cyberbullying` vs `not cyberbullying`  

**Preprocessing steps:**  
- Text cleaning (URLs, mentions, special characters)  
- Tokenization & lemmatization  
- Removal of duplicates  
- Oversampling for class balance  

---

## ⚙️ Models Implemented  

### 🔹 Baselines  
- **Naive Bayes** – Simple probabilistic model (Accuracy: 78.7%)  
- **Logistic Regression** – Both default and tuned with GridSearchCV (Accuracy: ~85.2%)  

### 🔹 Advanced Models  
- **KNN with PCA** – Improved local relationships in data (Accuracy: 85.6%)  
- **DistilBERT** – Transformer-based sequence classification (Accuracy: 87.7%)  

---

## 📈 Results  

| Model                      | Accuracy | F1-Score | Precision | Recall |
|-----------------------------|----------|----------|-----------|--------|
| Naive Bayes                 | 0.7868   | ~0.78    | ~0.78     | ~0.78  |
| Logistic Regression         | 0.8489   | ~0.84    | ~0.83     | ~0.84  |
| Tuned Logistic Regression   | 0.8522   | ~0.85    | ~0.85     | ~0.85  |
| KNN + PCA                   | 0.8563   | ~0.86    | ~0.87     | ~0.85  |
| DistilBERT (partial runs)   | 0.8775   | ~0.87    | ~0.87     | ~0.87  |

---

## 🚀 How to Run  

### Clone the repository and Run the file
```bash
git clone https://github.com/<your-username>/SafeTweet-Cyberbullying-Detection.git
cd SafeTweet-Cyberbullying-Detection

python cyberbullying.py

