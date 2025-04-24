# Decision Tree Classifier on Bank Dataset with Hyperparameter Tuning

This repository contains a machine learning pipeline for training and evaluating a Decision Tree Classifier using the **bank marketing dataset**. It includes **preprocessing**, **model training**, and **hyperparameter tuning** using `GridSearchCV`.

## 📁 Dataset

The dataset used in this project is `bank.csv`, which contains marketing campaign data from a Portuguese banking institution. It includes client and campaign-related information with the goal of predicting if a client will subscribe to a term deposit.

## 💡 Problem Statement

To build a classification model that predicts whether a client will subscribe to a term deposit (`y` column in the dataset) based on various features such as age, job, marital status, education, and more.

## 🧰 Technologies Used

- Python
- Pandas & NumPy
- Scikit-learn
- Matplotlib / Seaborn (optional for visualization)
- Jupyter Notebook / VS Code

## ⚙️ Project Workflow

### 1. Data Preprocessing
- Load the dataset using `pandas`
- Handle categorical variables using `OneHotEncoding` or `LabelEncoding`
- Deal with missing values if any
- Split the dataset into features and target

### 2. Train/Test Split
- Use `train_test_split` to divide the dataset (typically 80/20)

### 3. Model Training
- Train a basic `DecisionTreeClassifier`

### 4. Hyperparameter Tuning
- Use `GridSearchCV` to find optimal parameters:
  - `max_depth`
  - `min_samples_split`
  - `min_samples_leaf`
  - `criterion` (e.g., "gini" or "entropy")

### 5. Evaluation
- Accuracy Score
- Confusion Matrix
- Classification Report
- Cross-validation score

## 📈 Example Output

```
Best Parameters: {'criterion': 'entropy', 'max_depth': 5, 'min_samples_leaf': 2}
Accuracy Score: 0.88
```

## 🗂️ File Structure

```
├── bank.csv                 # Dataset
├── decision_tree_model.py   # Model training script (optional)
├── DecisionTree_Tuning.ipynb # Jupyter Notebook with code and analysis
├── README.md                # Project documentation
```

## 🔍 Future Improvements

- Feature selection to improve performance
- Try other classifiers (Random Forest, XGBoost)
- Implement pipeline with `Pipeline()` and `ColumnTransformer()`
- Deploy model with Flask or Streamlit
