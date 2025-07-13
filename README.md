# Detecting Offensive Arabic Text 🛡️

A machine learning project for detecting offensive or harmful content in Arabic text using classical NLP techniques. The model is trained on labeled Arabic data and includes preprocessing steps specific to Arabic language, making it suitable for real-world applications like social media moderation, chat filtering, or sentiment analysis.

---

## 🚀 Overview

This project aims to classify Arabic sentences into **offensive** or **non-offensive** categories using lightweight and explainable machine learning models. The approach avoids complex deep learning architectures, instead relying on:
- Arabic-specific text cleaning and normalization
- Feature extraction via `CountVectorizer` and `TF-IDF`
- Classification using `Multinomial Naive Bayes`

The goal is to deliver a fast, interpretable solution that works well with limited computational resources.

---

## 🧰 Tools & Libraries

- `Python`
- `pandas` – for data manipulation
- `numpy` – for numerical operations
- `scikit-learn` – for modeling (Naive Bayes, Vectorizers, metrics)
- `arabert` – Arabic-specific text preprocessing
- `tashaphyne` – Arabic light stemming (optional)

---

## 📁 Dataset

The dataset used is named `ar_dataset.csv` and contains Arabic phrases labeled as offensive or not.

**Sample format:**
```csv
text,label
"أنت غبي",1
"مرحبا بك",0
"أكرهك أيها الحقير",1
"كيف حالك اليوم؟",0
```
- `1`: Offensive
- `0`: Non-offensive

You can expand the dataset from other Arabic corpora or annotate new sentences manually for better performance.

---

## ⚙️ How to Run

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/Detecting-Offensive-Text-Arabic.git
cd Detecting-Offensive-Text-Arabic
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

Or manually:
```bash
pip install numpy pandas scikit-learn arabert tashaphyne
```

### 3. Launch the Notebook
```bash
jupyter notebook Detecting_OffinseveText.ipynb
```

---

## 🔄 Workflow Breakdown

### 1. Text Preprocessing
- Remove punctuation and diacritics
- Normalize Arabic letters (e.g., Alef forms, Teh Marbuta, etc.)
- Tokenize using `ArabertPreprocessor`
- Optionally apply stemming using `Tashaphyne`

### 2. Feature Engineering
- Convert text to numeric form using `CountVectorizer`
- Apply `TF-IDF` transformation to scale features

### 3. Model Training
- Use `Multinomial Naive Bayes` classifier
- Train on the processed feature set

### 4. Model Evaluation
- Accuracy
- Confusion Matrix
- Precision, Recall
- F1 Score

---

## ✅ Sample Output

**Input:**
```
"أنت إنسان فاشل ومقرف"
```

**Prediction:** Offensive (1)

**Input:**
```
"أتمنى لك يوماً جميلاً"
```

**Prediction:** Non-offensive (0)

---

## 📊 Results

| Metric     | Value   |
|------------|---------|
| Accuracy   | ~92%    |
| F1 Score   | ~0.91   |
| Model Size | Lightweight (<1MB) |

Results are based on a relatively small dataset. Improving the dataset size and quality will boost performance.


---


## ✍️ Author

Developed by AW.  
Contact me for collaboration, suggestions, or feedback.
```
