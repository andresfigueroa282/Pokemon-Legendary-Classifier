# 🧠 Legendary Pokémon Classifier

This project uses supervised machine learning to predict whether a Pokémon is **Legendary** or not based on its stats and characteristics. It was built using a publicly available Pokémon dataset.

---

## 📌 Project Goal

The objective is to train a binary classification model that can determine if a given Pokémon is *Legendary* (`True`) or *Not Legendary* (`False`). This is ideal for demonstrating:

- Data cleaning & preprocessing
- Feature selection
- Classification modeling
- Evaluation using key performance metrics

---

## 🗃️ Dataset

The dataset contains information about various Pokémon, including:

- Base stats
- Physical traits
- Other attributes
- Target variable: `is_legendary` (boolean)

Some features such as `name`, `abilities`, and `type weaknesses` were removed to prevent data leakage or overfitting.

---

## 🧪 Models Used

- Decision Tree Classifier, Random Forest, XGBoost

---

## 🧼 Key Steps

1. **Data Cleaning**: Removed or imputed missing and invalid values (e.g., parsing `capture_rate`).
2. **Feature Selection**: Dropped irrelevant columns and any that could leak target information (like `base_egg_steps`).
3. **Train-Test Split**: Used `train_test_split` with stratification to preserve class distribution.
4. **Model Training**: Used a Decision Tree Classifier with max depth tuning.
5. **Evaluation**: Evaluated using Accuracy, Precision, Recall, F1 Score, and a Confusion Matrix.

---

## 📈 Results

- **Accuracy**: ~98.7%
- **Precision (Legendary)**: 88%
- **Recall (Legendary)**: 100%
- **F1 Score (Legendary)**: 93%

The model performs very well at identifying Legendary Pokémon with high recall and strong overall accuracy.

---

## 📁 Files Included

- `Pokemon Portfolio Project.ipynb`: Jupyter notebook with code and outputs
- `pokemon.csv`: Cleaned dataset (or reference to Kaggle)
- `README.md`: Project documentation

---

## 🏷️ Tags

`#MachineLearning` `#Classification` `#Pokemon` `#DataScience` `#BeginnerML` `#Sklearn`
