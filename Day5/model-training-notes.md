Purpose

Train a machine learning model to predict survival

Evaluate model performance using standard metrics

Learn feature influence and baseline model behavior

Steps Followed

Load Cleaned Data

Titanic dataset after feature engineering and encoding

All features numeric, no missing values

Define Features & Target

X = all features except Survived

y = Survived

Train-Test Split

80% training, 20% testing

random_state=42 for reproducibility

Train Logistic Regression

Binary classification model

max_iter=1000 to ensure convergence

Fitted on training data

Predictions

Predicted y_pred for test data

Evaluation Metrics

Accuracy: Overall correctness of predictions

Precision: Correctly predicted survivors / all predicted survivors

Recall: Correctly predicted survivors / all actual survivors

F1-Score: Harmonic mean of precision & recall

Confusion Matrix: Shows TP, TN, FP, FN

Observations / Insights

Accuracy ~78% (example; check your run)

Non-survivors predicted slightly better than survivors

Key influential features: Sex, FamilySize, IsAlone

Logistic Regression assumes linear relationships — may miss non-linear patterns

Ensemble or tree-based models could improve performance

Limitations

Cannot capture non-linear relationships well

Sensitive to correlated features

Baseline model; more advanced models (Decision Trees, Random Forest) recommended next
