# Skincare Product Recommendation using Machine Learning

## Project Overview

This project builds a **Machine Learning based skincare product recommendation system**.
The system recommends suitable skincare products based on the user's **skin type, skin condition, and desired product type**.

The model predicts the **best skincare product** and provides additional information such as:

* Brand
* Notable Effects
* Product Image

---

# Dataset Description

The dataset contains skincare products and their properties.

## Columns in Dataset

| Column          | Description                                                                    |
| --------------- | ------------------------------------------------------------------------------ |
| skintype        | Skin type suitable for the product (Oily, Dry, Normal, Combination, Sensitive) |
| skin_condition  | Skin concerns like acne, pigmentation, wrinkles, redness, etc.                 |
| product_type    | Type of product (Face Wash, Toner, Serum, Moisturizer, Sunscreen)              |
| product_name    | Name of the skincare product                                                   |
| brand           | Brand of the product                                                           |
| notable_effects | Key benefits such as brightening, acne-free, moisturizing                      |
| picture_src     | URL of the product image                                                       |

---

# Machine Learning Pipeline

## 1 Data Preprocessing

Before training the models:

1. Load dataset using **Pandas**
2. Encode categorical variables using **Label Encoding**
3. Define **features (X)** and **target (y)**
4. Split the dataset into **training and testing sets**

Features used for training:

* skintype
* skin_condition
* product_type

Target variable:

* product_name

---

# Machine Learning Models Implemented

## 1 Logistic Regression

Steps:

* Encode categorical variables
* Split dataset into train and test sets
* Train Logistic Regression model
* Predict product name
* Evaluate accuracy

---

## 2 K-Nearest Neighbors (KNN)

Steps:

* Choose value of **k**
* Train KNN model
* Predict recommended product
* Evaluate model accuracy

---

## 3 Naive Bayes

Steps:

* Train Naive Bayes classifier
* Predict product name
* Evaluate model performance

---

## 4 Decision Tree

Steps:

* Train Decision Tree classifier
* Predict recommended product
* Evaluate model accuracy
* Optional: visualize decision tree

---

## 5 Random Forest

Steps:

* Train Random Forest classifier
* Tune number of trees (n_estimators)
* Predict products
* Evaluate model performance

---

## 6 Support Vector Machine (SVM)

Steps:

* Train SVM classifier
* Use kernel functions (linear or rbf)
* Predict recommended product
* Evaluate accuracy

---

# Model Evaluation

The models are evaluated using **accuracy score** on the test dataset.

Evaluation metric used:

* Accuracy Score

Future improvements can include:

* Precision
* Recall
* F1 Score

---

# Example Recommendation

User Input:

Skin Type: Oily
Skin Condition: Acne
Product Type: Face Wash

Model Output:

Product Name: Example Face Wash
Brand: Example Brand
Notable Effects: Acne control, oil balancing
Product Image: URL of the product image

---

# Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Machine Learning Algorithms

---

# Future Improvements

* Add more skincare products
* Improve recommendation accuracy
* Implement top-3 product recommendations
* Build a web interface using **Streamlit**
* Deploy the model online

---

# Conclusion

This project demonstrates how **machine learning algorithms can be applied to personalized skincare recommendations** by analyzing user skin characteristics and recommending suitable skincare products.
