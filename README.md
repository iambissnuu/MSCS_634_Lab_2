# Lab 2: Classification Using KNN and RNN Algorithms

## Overview
This lab explores the performance of K-Nearest Neighbors (KNN) and Radius Neighbors (RNN) classifiers using the Wine dataset from scikit-learn. The objective is to analyze how different parameter values affect classification accuracy and to compare the effectiveness of both models.

---

## Dataset Description
The dataset used in this lab is the Wine dataset provided by scikit-learn, originally sourced from the UCI Machine Learning Repository. It contains 178 samples with 13 numerical features representing chemical properties of wine. The dataset is divided into three target classes.

---

## Methodology

### Data Preparation
The dataset was loaded into a Pandas DataFrame and explored using basic techniques such as viewing the first few rows and analyzing class distribution. The features were standardized using StandardScaler to ensure that all variables contribute equally to distance calculations. The dataset was then split into 80% training data and 20% testing data.

---

### KNN Model
The K-Nearest Neighbors classifier was implemented using k values of 1, 5, 11, 15, and 21. The model was trained on the training set and evaluated on the test set. Accuracy was recorded for each value of k.

---

### RNN Model
The Radius Neighbors classifier was implemented using radius values of 350, 400, 450, 500, 550, and 600, as specified in the assignment. The model was trained and evaluated similarly to KNN.

---

## Results and Observations

### KNN Observations
The KNN classifier demonstrated strong and stable performance across different values of k. The highest accuracy was achieved at k = 15, indicating that a moderate number of neighbors provides the best balance between overfitting and generalization.

---

### RNN Observations
The RNN classifier produced the same accuracy across all radius values. This indicates that the selected radius values are too large for the scaled dataset, causing most data points to be grouped together. As a result, the model struggles to distinguish between classes and achieves lower accuracy.

This highlights the sensitivity of RNN to the radius parameter and the importance of selecting appropriate values.

---

### Model Comparison
The KNN model outperformed the RNN model in this experiment. KNN provided consistent and high accuracy due to its use of a fixed number of neighbors.

In contrast, RNN relies on a distance threshold, making it highly sensitive to parameter selection and feature scaling. The results demonstrate that inappropriate radius values can significantly reduce model performance.

---

## When to Use KNN vs RNN

- KNN is preferable when the dataset has relatively uniform density and when a fixed number of neighbors is desired.
- RNN is more suitable for datasets with varying densities, where grouping based on distance is more meaningful.

---

## Challenges
One challenge in this lab was understanding the impact of parameter selection, particularly for the RNN model. The large radius values required by the assignment did not align well with the scaled dataset, leading to reduced performance.

---

## Conclusion
This lab demonstrated the importance of parameter tuning in classification algorithms. KNN proved to be more robust and reliable for this dataset, while RNN requires careful selection of radius values to perform effectively.
