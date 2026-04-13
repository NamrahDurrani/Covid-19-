# Covid-19-
#  COVID-19 Data Analysis using Machine Learning & Neural Networks

##  Project Overview

This project focuses on applying **Supervised Learning, Unsupervised Learning, and Neural Networks** on a COVID-19 dataset to analyze patterns and compare different machine learning approaches.

The dataset used is *country_wise_latest.csv*, containing global COVID-19 statistics such as confirmed cases, deaths, recoveries, and weekly trends.

---

##  Objectives
* Applyed **regression technique** using randomforest regressor
* Apply **classification techniques** using supervised learning
* Explore **unsupervised learning methods** for pattern discovery
* Implement **neural networks** and understand their working
* Compare **traditional machine learning vs deep learning**
* Perform **regression analysis** and evaluate model performance

---

# 1. Supervised Learning (Classification)

##  Problem

Convert continuous COVID-19 data into a **binary classification problem**:

* 0 → Low Death Cases
* 1 → High Death Cases

##  Model Used

* Random Forest Classifier

##  Steps

* Data preprocessing and cleaning
* Feature selection
* Target creation (Death_Class using median threshold)
* Model training and testing
* Evaluation using:

  * Accuracy
  * Precision
  * Recall
  * F1-score
  * Confusion Matrix

##  Outcome

Random Forest performed well in capturing non-linear relationships and provided strong baseline classification performance.

---

#  2. Unsupervised Learning

##  Techniques Used

* K-Means Clustering
* PCA (Principal Component Analysis)

##  Goals

* Identify hidden patterns in COVID-19 data
* Group countries based on similarity
* Visualize clusters in reduced dimensions

##  Process

* Removed target variable
* Applied feature scaling
* Used **Elbow Method** to determine optimal clusters
* Applied K-Means clustering
* Reduced dimensions using PCA for visualization

##  Insights

Clusters revealed natural groupings such as:

* Low impact countries
* Medium impact countries
* High impact countries

---

#  3. Neural Network (Classification)

##  Model

* Feedforward Neural Network using Keras

##  Key Concepts Applied

* **Backpropagation** → updating weights using error
* **Gradient Descent (Adam Optimizer)** → minimizing loss
* **Learning Rate** → controlling update step size

##  Architecture

* Input Layer
* Hidden Layers (ReLU activation)
* Output Layer (Sigmoid for binary classification)

##  Evaluation

* Accuracy
* Confusion Matrix
* Training vs Validation Accuracy Graph

##  Observation

* Model learned effectively
* Validation accuracy was high due to small dataset
* Demonstrated strong generalization with some variance

---

#  4. Regression Analysis

##  Problem

Predict continuous variable:

* Target → **Deaths**

---

##  Models Used

###  Linear Regression

* Traditional machine learning approach
* Simple and interpretable

###  Neural Network Regression

* Multi-layer model for capturing complex patterns
* Linear activation in output layer

---

##  Evaluation Metrics

* MSE (Mean Squared Error)
* RMSE (Root Mean Squared Error)
* R² Score

---


##  Important Finding (Data Leakage)

Initially, models showed unrealistic performance due to:

* Derived features (e.g., death ratios)
* Mathematical relationship:

  * Confirmed = Deaths + Recovered + Active

After removing these, realistic results were obtained.

---

##  Final Comparison

| Model             | Performance                                                   |
| ----------------- | ------------------------------------------------------------- |
| Linear Regression | Strong baseline                                               |
| Neural Network    | Comparable, depends on tuning                                 |
| Insight           | Simpler models can outperform deep learning on small datasets |

---

#  Technologies Used

* Python
* Pandas, NumPy
* Scikit-learn
* TensorFlow / Keras
* Matplotlib, Seaborn



