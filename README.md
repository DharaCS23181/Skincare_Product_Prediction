# Skincare Product Recommendation System (Machine Learning + Knowledge-Based)

## Project Overview

This project builds a **skincare product recommendation system** that suggests suitable skincare products based on a user's skin profile. The system combines **knowledge-based logic** (ingredient–condition mapping) with **machine learning** to recommend appropriate skincare products.

The system analyzes a user's **age, skin type, hydration level, oil level, sensitivity, and skin conditions** to determine the most suitable products. The final output provides **top product recommendations** ranked by product rating.

This project demonstrates how **data preprocessing, feature engineering, recommendation logic, and machine learning models** can be integrated into a practical AI application.

---

## Objectives

* Build a skincare recommendation system based on user skin characteristics.
* Integrate ingredient knowledge with product data.
* Generate a dataset for machine learning training.
* Train multiple machine learning models to predict recommended skincare products.
* Compare model performance.

---

## Datasets Used

### 1. Skin Profile Dataset

Contains user skin characteristics.

Columns:

* Age
* Gender
* Hydration_Level
* Oil_Level
* Sensitivity
* Skin_Type

This dataset simulates user skin profiles.

---

### 2. Ingredient Knowledge Dataset

Contains skincare ingredients and the skin conditions they help treat.

Columns:

* name (ingredient name)
* who_is_it_good_for (skin conditions the ingredient helps with)
* who_should_avoid (optional safety information)

This dataset is used to **map skin conditions to useful ingredients**.

---

### 3. Product Dataset

Contains skincare products and their properties.

Columns:

* Label (product type such as cleanser, moisturizer, etc.)
* brand
* name (product name)
* price
* rank (product rating)
* ingredients
* combination
* dry
* normal
* oily
* sensitive

The binary columns indicate whether a product is suitable for each skin type.

---

## Data Processing Steps

### 1. Skin Condition Generation

A new column **skin_condition** is generated based on user features such as:

* Oil level
* Hydration level
* Age
* Sensitivity

Example conditions:

* acne
* pigmentation
* wrinkles
* fine lines
* dry and dehydrated skin
* enlarged pores
* redness

This step simulates realistic skincare concerns.

---

### 2. Ingredient Mapping

The ingredient dataset is used to map:

```
skin_condition → suitable ingredients
```

Example:

```
acne → salicylic acid
wrinkles → retinol
dry skin → hyaluronic acid
```

---

### 3. Product Matching

Products are filtered based on:

1. Skin type compatibility
2. Presence of relevant ingredients
3. Product ranking (rating)

The system returns the **Top 3 recommended products** sorted by rating.

---

## Final Dataset

After processing, the final dataset contains:

* Age
* Gender
* Hydration_Level
* Oil_Level
* Sensitivity
* Skin_Type
* skin_condition
* recommended_product

This dataset is used to train machine learning models.

---

## Machine Learning Models Implemented

The following six machine learning models are used to predict the recommended product:

1. Logistic Regression
2. K-Nearest Neighbors (KNN)
3. Decision Tree
4. Random Forest
5. Support Vector Machine (SVM)
6. Naive Bayes

Each model learns the relationship between **user skin features and recommended products**.

---

## Model Features (Input Variables)

The models use the following features:

* Age
* Gender
* Hydration_Level
* Oil_Level
* Sensitivity
* Skin_Type
* skin_condition

Target variable:

```
recommended_product
```

---

## Workflow

1. Load datasets
2. Clean and preprocess data
3. Generate skin conditions
4. Map ingredients to conditions
5. Match products using ingredient filtering
6. Generate recommended products
7. Create final ML dataset
8. Train machine learning models
9. Evaluate model accuracy

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Jupyter Notebook / Google Colab

---

## Output

For each user profile, the system recommends skincare products suitable for their skin type and condition.

Example output:

| Skin Type | Skin Condition | Recommended Product            |
| --------- | -------------- | ------------------------------ |
| Oily      | Acne           | Salicylic Acid Treatment Serum |
| Dry       | Wrinkles       | Retinol Anti-Aging Cream       |
| Normal    | Pigmentation   | Vitamin C Brightening Serum    |

---

## Future Improvements

Possible enhancements include:

* Incorporating dermatologist-approved ingredient rules
* Adding price-based filtering
* Personalized ranking using user feedback
* Deep learning recommendation systems
* Real-time web or mobile application integration

---

## Conclusion

This project demonstrates how **data science and machine learning can be applied to personalized skincare recommendations**. By combining domain knowledge (ingredients and skin conditions) with machine learning models, the system can provide intelligent product suggestions tailored to individual skin profiles.
