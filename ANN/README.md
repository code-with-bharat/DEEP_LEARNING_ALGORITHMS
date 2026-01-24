# Student Exam Score Prediction (Regression)

## Overview
This project focuses on predicting **student exam scores** using various **machine learning regression algorithms** and comparing their performance with a **Neural Network (NN)** model.  
The primary evaluation metric used is **Root Mean Squared Error (RMSE)**.

The goal is not only to achieve good predictive performance but also to understand **which type of model is more suitable** for this kind of dataset.

---

## Problem Statement
Given a set of student-related features, the task is to predict a **continuous exam score**.  
This is a **regression problem**, and model performance is evaluated using RMSE.

---

## Models Used
The following regression models were implemented and evaluated:

- Linear Regression  
- Ridge Regression  
- Lasso Regression  
- Elastic Net  
- LightGBM Regressor  
- Neural Network (Feedforward Fully Connected Network)

---

## Evaluation Metric
**Root Mean Squared Error (RMSE)** was used as the evaluation metric.

- RMSE penalizes large errors more heavily
- It is well-suited for continuous target variables like exam scores
- Lower RMSE indicates better model performance

---

## Neural Network Configuration
- Fully connected (Dense) layers
- ReLU activation for hidden layers
- Linear activation for output layer
- Trained using Mean Squared Error (MSE) loss
- RMSE used for evaluation

---

## Results & Observations
After experimenting with multiple machine learning models and a neural network, the following observations were made:

- Tree-based and linear models (especially LightGBM) achieved **lower or comparable RMSE** compared to the neural network.
- The neural network did **not outperform traditional ML models** on this dataset.
- This behavior is expected because:
  - The dataset size is **small to medium**
  - The feature set is **simple and tabular**
  - The relationships between features and target are **not highly complex**

---

## Conclusion
Based on the experimental results, the following conclusions were drawn:

- **Neural Networks are not always the best choice for tabular regression problems**, especially when:
  - The dataset is small or medium-sized
  - Features are simple and well-structured
  - The problem does not involve highly non-linear or hierarchical patterns
- Traditional machine learning models such as **Linear models and Gradient Boosting methods** often perform better and are easier to train and tune for such tasks.
- Model selection should be guided by **data characteristics**, not model complexity.

---

## Key Learning
> Increasing model complexity does not guarantee better performance.  
> Understanding the data and choosing an appropriate model is more important than using advanced algorithms blindly.

---

## Tech Stack
- Python
- NumPy
- Pandas
- Scikit-learn
- LightGBM
- TensorFlow / Keras
- Matplotlib / Seaborn

---

## Future Improvements
- Advanced feature engineering
- Cross-validation for more robust evaluation
- Exploring alternative loss functions (Huber, MAE)
- Error analysis by score ranges

---

## Output Format
Predictions are generated in the following format:

```text
id,exam_score
630000,97.5
630001,89.2
630002,85.5
