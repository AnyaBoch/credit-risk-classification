# credit-risk-classification
Module 20

Background
In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.
___________________
An overview of the analysis:

The purpose of this analysis was to train and evaluate a supervised machine learning model for binary classification, specifically for predicting high-risk loans.
____________________

### A summary:
	1.	Data Preprocessing & Splitting
    - Prepare and split the dataset into training and testing sets (80%/20% split).
	2.	Model Training & Predictions
    - Train a logistic regression model on the dataset.
    - Generate predictions based on the trained model.
	3.	Model Evaluation
    - Compute and visualize the confusion matrix to analyze misclassifications.
    - Generate a classification report to assess precision, recall, and F1-score.
	4.	Insights & Improvements
    - Identify class imbalance (highly skewed toward Class 0).
    - Discuss potential improvements (balancing techniques like resampling, class weights).

⸻

### A report:


 ### 🔹 Low risk loans/healthy loans
- Precision = 1.00 → The model predicted Class 0 with 100% accuracy (no false positives).
- Recall = 0.99 → The model identified 99% of actual Class 0 instances (some false negatives exist).
- F1-Score = 1.00 → Since precision and recall are both high, F1-score is also near perfect.
- Support = 15,001 → There were 15,001 actual instances of Class 0 in the dataset.

### 🔹 High risk loans
- Precision = 0.86 → When the model predicted Class 1, it was correct 86% of the time.
- Recall = 0.94 → The model captured 94% of all actual Class 1 instances.
- F1-Score = 0.90 → A good balance between precision & recall.
- Support = 507 → There were 507 actual instances of Class 1.

### 🔹 Overall Model Performance
- Accuracy = 0.99 → The model made correct predictions 99% of the time.
- Macro Avg (0.93 Precision, 0.97 Recall, 0.95 F1) → Shows how well the model performs on average per class.
- Weighted Avg (0.99 across all metrics) → Because Class 0 is dominant, this is close to accuracy.

## Conclusion:

This analysis helps determine the model’s ability to correctly classify high-risk vs. healthy loans. Given the imbalance, additional steps like oversampling or using a different algorithm could improve the model’s performance.
