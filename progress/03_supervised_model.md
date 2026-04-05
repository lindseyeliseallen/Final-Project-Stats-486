# Supervised Modeling

## Problem Context and Research Question

Our goal is to predict whether a patient will be readmitted to the hospital within 30 days. We used binary classification where patients readmitted within 30 days are considered high risk. This is important because understanding which patients are more likely to be readmitted can help healthcare providers know when to intervene and show what factors they should look at.
---

## Supervised Models Implemented

We used a logistic regression model and a random forest model. Logistic regression was used as a baseline because it is simple and easy to interpret. Random forest was used as a more flexible model to find more complex relationships in the data.

We split the data into training and testing sets using an 80/20 split. We also used stratification and class weighting since only about 11% of patients are readmitted within 30 days, showing there was a class imbalance. We tuned the hyperparameters using 5-fold cross-validation on the training data.

We looked at F1 score and ROC-AUC to evaluate the models, and we didn't focus on accuracy since there was class imbalance.

| Model                | Hyperparameters                          | Validation                         | F1    | ROC-AUC |
|---------------------|------------------------------------------|------------------------------------|-------|---------|
| Logistic Regression | C (tuned), class_weight = balanced       | 5-fold CV + train/test split       | 0.257 | 0.644   |
| Random Forest       | n_estimators = 200, max_depth = 10       | 5-fold CV + train/test split       | 0.273 | 0.668   |

---

## Model Comparison and Selection

Logistic regression worked well for a starting point to show us some of the obvious relationships in the data. The random forest model performed slightly better based off of F1 score and ROC-AUC. 

One of the biggest challenges was the class imbalance. We used class weighting and better metrics helped us avoid that issue and ended up choosing random forest as the stronger model.

---

## Explainability and Interpretability

We looked at feature importance from the random forest to help us better understand how the model was making predictions. The most important features were number of inpatient visits, discharge disposition, number of medications, and number of diagnoses.

This matches what we saw during EDA, where patients with more diagnoses and higher healthcare use tended to have a higher risk of readmission.

---

## Final Takeaways

Although performance is not extremely high, our results show that patients with more prior hospital visits and higher medical complexity are more likely to be readmitted within 30 days. Even though the model is not perfect, it still helps answer our research question by showing which factors are most associated with higher risk.