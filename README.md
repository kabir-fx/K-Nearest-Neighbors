# K-Nearest Neighbors (K-NN) Analysis

This directory contains an implementation of **K-Nearest Neighbors (K-NN)**, a simple yet powerful classification algorithm that classifies data points based on the majority class of their nearest neighbors.

## Dataset Overview

The model uses the `Social_Network_Ads.csv` dataset, which includes:

- **Features**:
  - `Age`: The age of the user.
  - `EstimatedSalary`: The estimated annual salary of the user.
- **Target**:
  - `Purchased`: Binary classification (0 = No, 1 = Yes) indicating if the user purchased the product.

## Implementation Steps

The implementation follows these key steps:

1.  **Data Preprocessing**:
    - Split the dataset into Training (75%) and Test (25%) sets.
    - Applied **Feature Scaling** (Standardization) to normalize `Age` and `Salary`, which is critical for distance-based algorithms like K-NN.
2.  **Model Training**:
    - Used `sklearn.neighbors.KNeighborsClassifier` with `n_neighbors = 5`.
    - Metric used: **'minkowski'** with `p = 2` (equivalent to Euclidean distance).
3.  **Prediction and Evaluation**:
    - Predicted a new result for Age 30 and Salary $87k.
    - Evaluated the model using a **Confusion Matrix**.
4.  **Visualization**:
    - Plotted decision boundaries for both Training and Test sets to show how the K-NN algorithm partitions the feature space.

## Results

The K-NN model demonstrates high performance:

- **Accuracy**: 93% on the test set.
- **Confusion Matrix**:
  - True Negatives: 64
  - False Positives: 4
  - False Negatives: 3
  - True Positives: 29
- The model effectively identifies the non-linear relationship between age, salary, and purchasing behavior.
