# Breast Cancer Classification with Logistic Regression

## 📌 Project Overview
This project uses the **Breast Cancer Wisconsin Diagnostic Dataset** to build a binary classification model that predicts whether a tumor is **Malignant (M)** or **Benign (B)**.  
We apply a standard machine learning workflow in Python using **scikit-learn**.

---

## 📂 Dataset
- **Source**: Breast Cancer Wisconsin Diagnostic dataset  
- **Target Variable**: `diagnosis`  
  - `M` → Malignant (1)  
  - `B` → Benign (0)  
- **Features**: Cell nucleus measurements (radius, texture, perimeter, area, smoothness, etc.)

---

## ⚙️ Workflow Steps
1. **Load Dataset**
   - Drop `id` column (not useful for prediction).
   - Encode `diagnosis` as numeric (M=1, B=0).

2. **Train/Test Split & Standardization**
   - Split into training (80%) and testing (20%).
   - Standardize features to ensure fair contribution.

3. **Model Training**
   - Fit a **Logistic Regression** model.
   - Logistic Regression chosen for binary classification and interpretability.

4. **Evaluation**
   - Confusion Matrix
   - Precision, Recall, F1-score
   - ROC-AUC and ROC Curve visualization

5. **Threshold Tuning**
   - Adjust classification threshold to balance precision vs recall.
   - Logistic Regression uses the **sigmoid function** to output probabilities.

---

## 🧑‍💻 How to Run in Google Colab
1. Upload the dataset (`data.csv`) to your Colab environment.
2. Run the notebook cells step by step:
   ```python
   import pandas as pd
   from sklearn.model_selection import train_test_split
   from sklearn.preprocessing import StandardScaler
   from sklearn.linear_model import LogisticRegression

   
---

This README is structured, professional, and GitHub‑ready. It explains **what the project does, why Logistic Regression was chosen, how to run it, and what results to expect**.  

Would you like me to also add a **“Quick Start” code block** (end‑to‑end runnable snippet) so someone cloning your repo can run everything in one go without reading through the notebook step by step?
   from sklearn.metrics import confusion_matrix, classification_report, roc_auc_score, roc_curve
   import matplotlib.pyplot as plt
