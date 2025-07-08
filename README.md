# Parkinson's Disease Prediction Using Machine Learning

This project aims to predict Parkinson's disease based on voice measurements using two machine learning models: **Random Forest** and **Logistic Regression**.
 The goal is to evaluate the impact of **feature correlation** on model performance and interpretability.

---

## Dataset

- Source: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/parkinsons)
- Contains 195 instances with 23 biomedical voice features and a binary target (`status`)
  - `status = 1`: Parkinson’s disease
  - `status = 0`: Healthy

---

## 📊 Exploratory Data Analysis

- Checked feature distributions by class
- Plotted feature importances and correlation heatmap
- Observed **strong correlation** between many `Jitter`, `Shimmer`, and related features
###Distribution of Parkinson\'s Status![Distribution of Parkinson\'s Status](C:\\Users\\USER\\Downloads\\images\\Distribution of Parkinson\'s Status.png)
###Distribution of {feature} by Status![Distribution of {feature} by Status](C:\\Users\\USER\\Downloads\\images\\Distribution of {feature} by Status.png)
###{feature} vs Status![{feature} vs Status](C:\\Users\\USER\\Downloads\\images\\feature vs status.png)
###Feature Correlation Heatmap![Feature Correlation Heatmap](C:\\Users\\USER\\Downloads\\images\\Feature Correlation Heatmap.png)



---

## 🧪 Models Used

- **Logistic Regression** (for simplicity and interpretability)
- **Random Forest Classifier** (for performance and robustness to multicollinearity)

---

## 🧹 Feature Engineering

- Identified and dropped **highly correlated features** (`correlation > 0.95`):
  - `MDVP:RAP`, `Jitter:DDP`, `MDVP:PPQ`, `MDVP:Jitter(Abs)`
  - `MDVP:Shimmer(dB)`, `Shimmer:APQ3`, `Shimmer:APQ5`, `MDVP:APQ`, `Shimmer:DDA`, `spread1`
- Standardized features using `StandardScaler`

---

## ⚙️ Model Performance Comparison

| Model                  | Feature Set   | Accuracy | Precision (0) | Precision (1) |
|------------------------|---------------|----------|----------------|----------------|
| Random Forest          | Full          | 0.9487   | 1.00           | 0.94           |
| Random Forest          | Reduced       | 0.9230   | 1.00           | 0.94           |
| Logistic Regression    | Full          | 0.8974   | 1.00           | 0.89           |
| Logistic Regression    | Reduced       | 0.8974   | 1.00           | 0.89           |
###Random Forest ~ Confusion Matrix![Random Forest ~ Confusion Matrix](C:\\Users\\USER\\Downloads\\images\\Random_Forest~Confusion_Matrix.png)
###Logistic Regression ~ Confusion Matrix![Logistic Regression ~ Confusion Matrix](C:\\Users\\USER\\Downloads\\images\\Logistic Regression ~ Confusion Matrix.png)


---

## 📌 Conclusion

- **Random Forest with full features** achieved the best accuracy (94.87%).
- **Logistic Regression** performed consistently well with fewer features and is easier to interpret.
- Dropping highly correlated features helped simplify the model **without affecting Logistic Regression's accuracy**, but slightly reduced Random Forest accuracy.

---

## 📈 Accuracy Comparison (Bar Plot)

###Model Accuracy Comparison![Model Accuracy](C:\\Users\\USER\\Downloads\\images\\Model Accuracy Comparison.png)

---

## 📁 Files

- `parkinsons_prediction.ipynb`: Main notebook
- `README.md`: Project documentation
- `requirements.txt`: Package list
- `/plots`: Visuals including bar plots and confusion matrices

---

## 📚 Requirements

Install packages using:

```bash
pip install -r requirements.txt
 Author
Kavya M
Data Science Enthusiast | B.Sc. Physics | M.Sc. Physics (IGNOU)


