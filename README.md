# Lab 2: Classification Using KNN and RNN Algorithms

## Overview
This lab explores the performance of K-Nearest Neighbors (KNN) and Radius Neighbors (RNN) classifiers using the Wine dataset from scikit-learn. The objective is to analyze how different parameter values affect classification accuracy and to compare the effectiveness of both models.

---

## Dataset Description
The Wine dataset is obtained from the scikit-learn library and is originally sourced from the UCI Machine Learning Repository. It contains 178 samples with 13 numerical features representing chemical properties of wines. The dataset is divided into three target classes.

---

## Methodology

### Data Preparation
The dataset was loaded and converted into a Pandas DataFrame. Basic exploration was performed, including viewing dataset structure and class distribution. The data was standardized using StandardScaler to ensure consistent scaling across features. The dataset was then split into 80% training and 20% testing sets.

---

### KNN Model
The K-Nearest Neighbors classifier was implemented using multiple values of k: 1, 5, 11, 15, and 21. The model was trained on the training set and evaluated on the test set. Accuracy was recorded for each value of k.

---

### RNN Model
The Radius Neighbors classifier was implemented using radius values: 350, 400, 450, 500, 550, and 600. The model was trained and evaluated similarly to KNN, and accuracy values were recorded.

---

## Results and Observations

### KNN Observations
The KNN model showed that accuracy varies with different values of k. Smaller values of k may lead to overfitting, while larger values help smooth the decision boundary. Moderate values of k provided the best performance.

---

### RNN Observations
The RNN model's performance was highly dependent on the radius value. Smaller radii resulted in fewer neighbors being considered, while larger radii introduced more data points, which could include noise.

---

### Model Comparison
KNN provided more stable and consistent results compared to RNN. Since KNN always considers a fixed number of neighbors, it is less sensitive to data distribution. In contrast, RNN relies on distance thresholds, making it more sensitive to scaling and density.

---

## Challenges
One challenge in this lab was selecting appropriate radius values for the RNN model, as its performance is highly sensitive to the scale of the data. Additionally, understanding the trade-off between bias and variance in KNN required careful observation of results.

---

## Conclusion
This lab demonstrated that parameter selection plays a crucial role in classification performance. KNN proved to be more reliable for this dataset, while RNN may be more suitable for datasets with varying densities.
