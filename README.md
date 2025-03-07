# credit-risk-classification
Module 20

Background
*In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.
___________________
### An overview of the analysis:

The purpose of this analysis is to train and evaluate a supervised machine learning model for binary classification, specifically for predicting high-risk loans.
⸻

### A process:
Stages of the Machine Learning Process in This Analysis

**1. Data Preprocessing**
- Loaded the dataset and explored its structure using Pandas.
- Defined X (features) and y (target: loan risk level).
- Split the dataset into training (80%) and testing (20%) sets using train_test_split.

**2. Creating a logistic regression model with the original data**
- Chosing logistic regression as the supervised machine learning model.
- Training the model on the testing data labels (the X_train and y_train dataset).


**3. Model Performance & Predictions**
- Creating the trained model to predict labels ("prediction") for the test data (X_test).

**4. Model Evaluation**
- Calculated the balanced accuracy score (**96.69%**) to check performance. Balanced_accuracy_score(y_test, prediction) calculates the average recall across all classes, ensuring that minority classes are weighted fairly.
- Created a confusion matrix to see correct vs. incorrect predictions.
- Found that Class "0" (low-risk loans) dominated predictions, showing an imbalance in the data.
- Calculated classification report metrics to see how well the model performed for each class.

6. Visualization 
- Plotted the **confusion matrix** to show model performance.


![alt text](/output/confusion_matrix.png)



- Visualized the **classification report** using a heatmap for better interpretation.


![alt text](/output/risk_classification_report.png)



### A report:


 ### Low risk loans/healthy loans
- Precision = 1.00 --> The model predicted Class "0" with 100% accuracy (no false positives).
- Recall = 0.99 --> The model identified 99% of actual Class 0 instances (some false negatives exist).
- F1-Score = 1.00 --> Since precision and recall are both high, F1-score is also near perfect.
- Support = 15,001 --> There were 15,001 actual instances of Class 0 in the dataset.


### High risk loans
- Precision = 0.86 --> When the model predicted Class "1", it was correct 86% of the time.
- Recall = 0.94 --> The model captured 94% of all actual Class 1 instances.
- F1-Score = 0.90 --> A good balance between precision & recall.
- Support = 507 --> There were 507 actual instances of Class "1".

### Overall Model Performance
- Accuracy = 0.99 --> The model made correct predictions 99% of the time.
- Macro Avg (0.93 Precision, 0.97 Recall, 0.95 F1) --> Shows how well the model performs on average per class.
- Weighted Avg (0.99 across all metrics) → Because Class 0 is dominant, this is close to accuracy.


### Summary:

**What else our Model tells Us**
- The dataset is highly imbalanced: 97% of the loans are classified as low risk (Class "0").

- 3% of the loans are classified as high risk (Class "1").

- The model is heavily biased toward predicting low-risk loans, which aligns with the real-world data where most loans are actually low risk(light google research)

**Is This a Problem?**

Not necessarily. Since the actual loan market has very few high-risk loans, the model correctly reflects that reality. We don’t need to artificially boost the high-risk class just for the sake of balance—this would misrepresent the real-world loan distribution.

