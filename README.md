# Dry Bean Classification using Machine Learning

## 📌 Project Overview

This project focuses on classifying dry bean varieties using Machine Learning classification algorithms. It uses the Dry Bean Dataset from the UCI Machine Learning Repository, which contains numerical features extracted from images of dry beans.

The project compares multiple classification models, including Decision Trees, Bagging, Random Forest, Gradient Boosting, and XGBoost. It also explores dimensionality reduction and feature selection techniques to evaluate their effects on model performance.

## 🎯 Project Objectives

* Explore and visualize the dataset.
* Clean the data and prepare it for Machine Learning.
* Analyze feature relationships and correlations.
* Train and evaluate a Decision Tree classifier.
* Improve Decision Tree performance using different splitting criteria, tree depths, and cost-complexity pruning.
* Apply Bagging with SVM and Decision Tree base estimators.
* Train and tune a Random Forest classifier.
* Tune a Gradient Boosting classifier.
* Build and evaluate an XGBoost classifier.
* Compare all models using classification metrics.
* Apply Principal Component Analysis (PCA).
* Perform feature selection using feature importance scores.
* Compare model performance before and after complexity reduction.

## 📊 Dataset

**Dataset:** Dry Bean Dataset

**Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/602/dry+bean+dataset)

The dataset contains measurements extracted from images of dry beans belonging to seven different varieties.

* **Number of samples:** 13,611 before cleaning
* **Number of features:** 16 numerical features
* **Target column:** `Class`
* **Number of classes:** 7

The features describe physical characteristics such as area, perimeter, aspect ratio, and compactness.

## 🛠️ Technologies and Libraries

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost

## ⚙️ Project Workflow

### 1. Data Exploration and Preprocessing

* Load the dataset using Pandas.
* Check missing values, duplicate rows, and data types.
* Remove duplicate rows when necessary.
* Explore feature relationships using a scatterplot matrix.
* Analyze feature correlations using a heatmap.
* Split the dataset into training and testing sets using an 80/20 ratio, `random_state=42`, and stratification.

### 2. Decision Tree Classification

* Train a baseline Decision Tree classifier.
* Visualize the tree up to depth 4.
* Interpret the top splitting nodes.
* Evaluate training and testing accuracy.
* Display the confusion matrix.
* Experiment with Gini and Entropy splitting criteria.
* Tune `max_depth` and apply cost-complexity pruning using `ccp_alpha`.

### 3. Bagging and Random Forest

* Apply Bagging with SVM and Decision Tree base estimators.
* Compare their accuracy and confusion matrices.
* Train a baseline Random Forest classifier.
* Tune the number of estimators.
* Experiment with different `max_features` settings.
* Extract and visualize the top 8 important features.

### 4. Boosting Algorithms

* Train a Gradient Boosting classifier.
* Tune the number of estimators and learning rate.
* Plot training and testing accuracy against the number of estimators.
* Build an XGBoost classifier using selected hyperparameters.
* Experiment with `subsample` values of 0.6, 0.8, and 1.0.

### 5. Model Comparison

Compare Decision Tree, Bagged SVM, Bagged Decision Tree, Random Forest, Gradient Boosting, and XGBoost using:

* Accuracy
* Weighted Precision
* Weighted Recall
* Weighted F1-score

Use a summary table to identify the strongest and weakest models across the evaluation metrics.

### 6. Dimensionality Reduction and Feature Selection

**Principal Component Analysis (PCA)**

* Plot the explained variance ratio.
* Determine the number of components needed to retain 95% of the variance.
* Visualize the first two principal components.
* Retrain the selected model using the reduced feature representation.

**Feature Selection**

* Rank the original features using Random Forest feature importance.
* Select the top 6 features.
* Retrain the selected model using only those features.
* Visualize the selected feature importance scores.

### 7. Final Evaluation

Compare the original best model with the PCA-reduced and feature-selected versions using accuracy, weighted precision, weighted recall, and weighted F1-score.

Analyze the trade-offs between predictive performance, model complexity, and interpretability.

## 📈 Evaluation Metrics

* **Accuracy:** The proportion of correctly classified samples.
* **Precision:** How many predicted samples of a class are correct.
* **Recall:** How many actual samples of a class are correctly identified.
* **F1-score:** The harmonic mean of precision and recall.
* **Confusion Matrix:** Shows correct and incorrect predictions for each bean variety.

Weighted averages are used for multi-class Precision, Recall, and F1-score to account for differences in class sizes.

## 📂 Project Structure

```text
Dry-Bean-Classification-ML/
│
├── Dry_Bean_Classification.ipynb
├── README.md
└── requirements.txt
```

*Note: Update the notebook filename in this structure if your actual filename is different.*

## 🚀 How to Run the Project

1. Clone or download this repository.

2. Install the required libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn xgboost openpyxl jupyter
   ```

3. Download the dataset from the [UCI dataset page](https://archive.ics.uci.edu/dataset/602/dry+bean+dataset).

4. Extract the ZIP file and place the Excel dataset where the notebook expects it.

5. Open the notebook:

   ```bash
   jupyter notebook
   ```

6. Run the notebook cells in order.

## 👨‍💻 Author

**Marwan Tamer**

AI & Machine Learning Student

Interested in Machine Learning, Deep Learning, Data Analysis, and Artificial Intelligence.

## 📚 Dataset Reference

Koklu, M., & Ozkan, I. A. (2020). *Multiclass Classification of Dry Beans Using Computer Vision and Machine Learning Techniques.* Computers and Electronics in Agriculture, 174, 105507.

Dataset: [UCI Machine Learning Repository — Dry Bean Dataset](https://archive.ics.uci.edu/dataset/602/dry+bean+dataset)
