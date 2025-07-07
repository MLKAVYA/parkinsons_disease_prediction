# Parkinson’s Disease Prediction

 This project aims to predict whether a person has Parkinson’s Disease using various voice features. 
The models used include *Random Forest Classifier* and *Logistic Regression*, with a performance comparison using 
confusion matrices and classification reports.
----
## Problem Statement

 Parkinson’s Disease is a progressive nervous system disorder that affects movement.
Early detection is crucial for treatment and quality of life. This project builds a
binary classification model to detect Parkinson’s using biomedical voice measurements.
----
##Dataset

- *Source*: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/parkinsons)
- *Total Records*: 195
- *Features*: 23
- *Target Variable*: status (1 = Parkinson’s, 0 = Healthy)
----
##Exploratory Data Analysis (EDA)

- Checked for missing values.
- Performed correlation analysis.
- Scaled the data using StandardScaler.
-Vocal features like jitter and shimmer showed clear separation between healthy and Parkinson’s individuals.
 Noise-related features (NHR, HNR) were strongly correlated with disease presence, as confirmed by the heatmap.
----
##Models Used

### 1. Random Forest Classifier
- *Accuracy*: 94.87%
- *Confusion Matrix*:[[5 2]
                      [0 32]]
-*Classification Report*:class 0: Precision=1.00 | class 1: Precision=0.94
-*Interpretation*:The model misclassified 2 instances of class 0 as class 1 but correctly classified all class 1 instances.
  It performs excellently, especially for detecting positive cases(plotted Confusion Matrix Heatmap).
### 2.Logistic Regression
-*Accuracy*:89.74%
-*Confusion Matrix*:[[3 4]
                      [0 32]]
-*Classification Report*:class 0: Precision=1.00 | class 1: Precision=0.89
-*Interpretation*:Logistic Regression correctly predicted all class 1 instances but misclassified 4 class 0 instances as class 1. 
  It still performed well but was slightly less accurate than the Random Forest(plotted Confusion Matrix Heatmap).
----
##Conclusion

- *Random Forest* outperformed Logistic Regression in terms of accuracy and precision,making it more reliable model for this problem.
- Both models correctly identified all Parkinson’s patients (*0 False Negatives*).
- Logistic Regression had slightly more false positives compared to Random Forest.

  


 