🔹 Why Model Comparison is Needed

Single accuracy score is misleading

Train-test split may be biased

Different models behave differently on same data

Fair evaluation is required before deployment

🔹 Models Compared

Logistic Regression

Decision Tree

Random Forest

Same dataset and same split used for fairness

🔹 Limitations of Accuracy

Does not handle class imbalance well

Ignores confidence of predictions

Two models can have same accuracy but different behavior

🔹 ROC Curve

Plots True Positive Rate vs False Positive Rate

Shows trade-off between sensitivity and specificity

Visual comparison of model performance

🔹 ROC-AUC Score

Measures ability to separate classes

Value ranges from 0 to 1

0.5 → random guessing

Closer to 1 → better model

Threshold-independent metric

🔹 ROC-AUC Observations

Logistic Regression performed reasonably

Decision Tree showed unstable behavior

Random Forest achieved highest ROC-AUC

Ensemble model handled class separation best

🔹 Cross-Validation Concept

Splits data into multiple folds

Trains and tests model multiple times

Reduces dependency on a single split

Provides reliable performance estimate

🔹 Cross-Validation Results

Evaluated using F1-score

Mean score indicates average performance

Standard deviation indicates stability

Lower std → more stable model

🔹 Model Stability Analysis

Logistic Regression → stable but limited

Decision Tree → high variance

Random Forest → best balance of bias and variance

🔹 Final Model Selection

Random Forest selected as final model

Highest ROC-AUC score

Consistent cross-validation performance

Suitable for structured tabular data

🔹 Key Takeaways

Always compare multiple models

Use ROC-AUC instead of accuracy alone

Cross-validation is essential

Ensemble models often perform better
