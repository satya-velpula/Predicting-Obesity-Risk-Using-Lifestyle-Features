# Predicting Obesity Risk Using Lifestyle Features  
### A Comparative and Interpretable Machine Learning Study

This project applies machine learning techniques to predict **obesity risk** using lifestyle and demographic data.  
The study compares multiple classification models and uses interpretable methods to identify the most influential lifestyle predictors.

---

## Research Question
**How accurately can machine learning models predict obesity risk using lifestyle and demographic features, and which lifestyle factors contribute most to prediction performance?**

---

## Objectives
- Preprocess lifestyle dataset while removing BMI-related leakage variables.
- Train multiple machine learning models for obesity classification.
- Evaluate models using **Accuracy, Precision, Recall, F1-score, and ROC-AUC**.
- Interpret model predictions using **feature importance techniques**.
- Compare results with findings from existing research.

---

## Dataset
- ~20,000 observations
- Lifestyle, nutrition, exercise, and demographic features
- Target variable:

Obesity_Risk = 1 if BMI ≥ 30 else 0


BMI and body composition variables were removed from the model to **avoid data leakage**.

---

## Machine Learning Models
The following models were trained and compared:

- Logistic Regression
- Random Forest
- Gradient Boosting
- CatBoost

Random Forest was further optimized using **hyperparameter tuning**.

---

## Model Evaluation

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

Additional validation methods:

- ROC Curve comparison
- Cross-validation
- Overfitting detection

---

## Key Results

| Model | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|------|---------|---------|---------|---------|---------|
| Random Forest | 0.9910 | 0.9784 | 0.9759 | 0.9772 | 0.9989 |
| Random Forest (Tuned) | 0.9900 | 0.9820 | 0.9670 | 0.9745 | 0.9987 |
| CatBoost | 0.9863 | 0.9779 | 0.9518 | 0.9647 | 0.9987 |
| Gradient Boosting | 0.9425 | 0.9241 | 0.7719 | 0.8412 | 0.9805 |
| Logistic Regression | 0.9068 | 0.8388 | 0.6527 | 0.7341 | 0.9380 |

The **Initial Random Forest model achieved the best performance but I chose tuned random forest to interpret feature to avoid any overfitting**.

---

## Model Interpretability

To identify the most important lifestyle predictors, **Permutation Feature Importance** was used.

Important predictors included variables related to:

- physical activity
- dietary intake
- heart rate indicators
- demographic characteristics

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- CatBoost
- Matplotlib
- Seaborn

---

## How to Run

Clone the repository:

```bash
git clone https://github.com/yourusername/obesity-risk-prediction.git
```
## License

This project is licensed under the **Apache License 2.0**.

You may use, modify, and distribute this software in accordance with the terms of the license.

See the full license here:  
https://www.apache.org/licenses/LICENSE-2.0
