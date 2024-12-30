# Amazon Recommendation Systems

This project demonstrates the implementation of recommendation systems on an Amazon dataset using two approaches: **Popularity-Based Recommendations** and **Collaborative Filtering**. The project highlights how recommendation systems can predict user ratings for products efficiently and effectively.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Results and Evaluation](#results-and-evaluation)
- [Technologies Used](#technologies-used)

---

## Project Overview

The goal of this project is to showcase how recommendation systems work on large datasets. Using an Amazon dataset, we implemented two recommendation approaches:

1. **Global Baseline Recommendation**: Predicts ratings based on overall, user, and product mean deviations.
2. **Collaborative Filtering**: Utilizes the Alternating Least Squares (ALS) algorithm for item-item collaborative filtering.

Both methods were evaluated using the Root Mean Square Error (RMSE) metric to measure prediction accuracy.

---

## Dataset

The dataset used in this project is based on Amazon product reviews and contains the following features:

- `User_ID`: Identifier for users.
- `Product_ID`: Identifier for products.
- `Rating`: User's rating for a product.
- `Timestamp`: Time when the rating was given (excluded from modeling).

### Dataset Details:
- **Size**: 318 MB
- **Records**: 7.82 million ratings

---

## Methodology

### Tools:
The project was implemented using **Google Colab** and **Apache Spark**.

### Steps:
1. **Environment Setup**:
   - Installed Spark and configured Google Colab for execution.
   - Uploaded and read the dataset into a Spark DataFrame.

2. **Preprocessing**:
   - Renamed columns for better identification.
   - Verified data integrity (no null values).
   - Converted data types to numerical formats.
   - Removed irrelevant columns (e.g., `Timestamp`).

3. **Global Baseline Recommendation**:
   - Split the dataset (70% training, 30% testing).
   - Computed global, user, and product mean ratings and deviations.
   - Predicted ratings for the test dataset.
   - Evaluated model using RMSE.

4. **Collaborative Filtering**:
   - Used the ALS algorithm for item-item collaborative filtering.
   - Split the dataset (70% training, 30% testing).
   - Trained the ALS model and generated predictions for test data.
   - Evaluated model using RMSE.
   - Generated two product recommendations per user.

---

## Results and Evaluation

Both approaches were tested on the 7.82 million record dataset, and their performance was measured using RMSE.

### Evaluation Results:
1. **Global Baseline Recommendation**:
   - RMSE: 1.42
2. **Collaborative Filtering (ALS)**:
   - RMSE: 0.19

Due to the significantly lower RMSE score, the **Collaborative Filtering (ALS)** approach was chosen as the final model.

---

## Technologies Used

- **Google Colab**: Development environment.
- **Apache Spark**: Data processing and modeling.
- **Python**: Programming language.
- **Spark MLlib**: Library for machine learning algorithms.
- **Pandas**: Data manipulation and analysis.

---

Feel free to clone this repository and explore how recommendation systems are built and evaluated on large datasets. Let us know if you have any questions or need further details!
