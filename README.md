# 🧠 Legendary Pokémon Classifier

This project uses supervised machine learning to predict whether a Pokémon is **Legendary** or not based on its stats and attributes. It leverages a publicly available dataset of 802 Pokémon spanning seven generations.

---

## 📌 Project Goal

The goal is to train a **binary classification model** that predicts if a given Pokémon is *Legendary* (`True`) or *Not Legendary* (`False`), while demonstrating key machine learning steps:

- Data cleaning and preprocessing
- Feature selection
- Handling class imbalance (SMOTE)
- Model training and tuning (Logistic Regression, Random Forest, XGBoost)
- Evaluation using advanced metrics

---

## 🗃️ Dataset

The dataset includes a variety of Pokémon characteristics, such as:

- **Base stats**: `hp`, `attack`, `defense`, `sp_attack`, `sp_defense`, `speed`, etc.
- **Game mechanics**: `capture_rate`, `experience_growth`, `base_happiness`, etc.
- **Target variable**: `is_legendary` (binary)

**Removed Features**:
- Categorical or descriptive features such as `type1`, `type2`, `name`, and `japanese_name` - Non-informative or potentially misleading features like
- `base_total` and `capture_rate`, which are directly or indirectly correlated with legendary status and could cause data leakage

---

## ⚙️ Key Steps

1. **Data Cleaning**: Parsed columns, handled missing values, and removed irrelevant or leaked features.
2. **Feature Selection**: Focused on numerical attributes mostly related to a Pokémon's stats.
3. **Train-Test Split**: Used stratified 80/20 split to maintain class proportions.
4. **Class Balancing**: Applied **SMOTE** to oversample the minority class (legendary Pokémon) in the training set.
5. **Scaling**: Standardized numerical features before training.
6. **Modeling**:
   - **Logistic Regression**: Used as a baseline
   - **Random Forest**: Tuned via `GridSearchCV` and thresholding
   - **XGBoost**: Tuned and evaluated with probability thresholding
7. **Evaluation Metrics**:
   - Accuracy
   - **Precision / Recall / F1-score** (with a focus on Legendary class)
   - **ROC AUC** (used model confidence via `predict_proba`)
     
---

## 🤖 Best Performing Model

**✅ Random Forest Classifier** with threshold tuning:

- **Precision (Legendary)**: 0.87  
- **Recall (Legendary)**: 0.93  
- **F1 Score (Legendary)**: 0.90  
- **Accuracy**: 0.98  
- **ROC AUC**: 0.9988

*XGBoost also performed well, but had slightly lower F1 due to reduced recall at the optimal threshold.*

---

## 📁 Files Included

- `Pokemon_Legendary_Classifier.ipynb`: Full code notebook with preprocessing, modeling, and evaluation
- `pokemon.csv`: 🔗 [View Dataset on Kaggle]([https://github.com/andresfigueroa282/Pokemon-Legendary-Classifier](https://www.kaggle.com/datasets/rounakbanik/pokemon)) 
- `README.md`: Project overview and documentation

---

## 🏷️ Tags

`#MachineLearning` `#Classification` `#Pokemon` `#BinaryClassifier` `#RandomForest` `#XGBoost` `#DataScience` `#Sklearn`

---

*Project by Andres Figueroa*
