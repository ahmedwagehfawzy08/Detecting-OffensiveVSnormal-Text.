# Detecting Offensive Arabic Text 🛡️📜

This project focuses on detecting offensive or harmful Arabic language content using machine learning and NLP techniques. It leverages preprocessing tailored for Arabic text and a Multinomial Naive Bayes classifier for classification.

## 🔍 Project Goals
- Classify Arabic text into offensive / non-offensive categories.
- Use lightweight, efficient models that are easy to deploy.
- Explore the impact of preprocessing Arabic content on classification performance.

---

## 🧰 Tools & Libraries
- `Python`
- `scikit-learn`
- `pandas`, `numpy`
- `CountVectorizer`, `TF-IDF`
- `Arabert` (for Arabic text preprocessing)
- `Tashaphyne` (for Arabic stemming)

---

## 📁 Dataset
The dataset used is:
- **`ar_dataset.csv`** – Arabic sentences labeled as offensive or not.

The CSV file should contain:
```csv
text,label
"أنت غبي",1
"مرحبا بك",0
...
