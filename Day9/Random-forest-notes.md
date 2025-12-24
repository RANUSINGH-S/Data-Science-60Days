🎯 Objective

Improve Random Forest performance systematically

Avoid manual guessing of hyperparameters

Select best model using cross-validated F1-score

🔹 What is GridSearchCV

Exhaustive search over given hyperparameter combinations

Uses cross-validation to evaluate each combination

Selects best model based on chosen scoring metric

Reduces bias from single train–test split

🔹 Why F1-Score was Chosen

Dataset has class imbalance

Accuracy can be misleading

F1-score balances:

Precision (false positives)

Recall (false negatives)

Better metric for real-world classification tasks

🔹 Hyperparameters Tuned & Purpose

n_estimators

Number of trees in the forest

More trees → better stability but slower training

max_depth

Controls tree depth

Prevents overfitting

min_samples_split

Minimum samples required to split a node

Larger value → simpler trees

min_samples_leaf

Minimum samples at leaf node

Smooths predictions

max_features

Number of features considered at each split

Controls randomness and variance

🔹 Cross-Validation Strategy

5-fold cross-validation

Each model evaluated on 5 different splits

Final score = average F1-score across folds

Reduces lucky/unlucky split bias

🔹 Results Summary

F1-score showed marginal improvement

Recall improved slightly

Precision remained stable

Cross-validation variance reduced

Model became more consistent across folds

🔹 Overfitting Analysis

Limiting depth and split parameters reduced overfitting

Tuned model generalized better than untuned model

Stability improved more than raw metric gain

🔹 Why Improvement Was Limited

Titanic dataset is small

Features are limited in complexity

Baseline Random Forest was already strong

GridSearch mainly improved reliability, not dramatic scores

🔹 Issues Faced & Resolution

GridSearchCV failed due to misspelled hyperparameter

Kernel restart required to clear stale parameters

Corrected min_samples_split and reinitialized model

GridSearch executed successfully after cleanup

🏁 Final Decision

Tuned Random Forest selected as final model

Preferred due to better generalization and stability

Model ready for threshold tuning and deployment logic
