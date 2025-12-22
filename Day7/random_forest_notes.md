🔹 Model Used

Random Forest Classifier

Ensemble learning method

Collection of multiple Decision Trees

Final prediction based on majority voting

🔹 Why Random Forest

Single Decision Trees overfit easily

Random Forest reduces variance

Combines predictions from many trees

More stable and reliable than one tree

🔹 Ensemble Learning Concept

Multiple weak models → one strong model

Each tree trained on:

Random subset of data

Random subset of features

Reduces overfitting and noise sensitivity

🔹 Performance Comparison

Outperformed single Decision Tree

More consistent metrics

Better generalization on test data

Balanced precision and recall

🔹 Hyperparameters Used

n_estimators → number of trees

max_depth → controls tree depth

More trees improve stability

Very deep trees can still overfit

🔹 Hyperparameter Observations

Low depth → underfitting

Moderate depth → best balance

Increasing trees does not always increase accuracy

Improves robustness and confidence

🔹 Feature Importance

Extracted using feature_importances_

Averaged importance across all trees

More stable than Decision Tree importance

Less bias toward a single feature

🔹 Important Titanic Features

Sex

Fare

Passenger Class (Pclass)

FamilySize

IsAlone

Results aligned with EDA (Day 3)

🔹 Random Forest Strengths

Handles non-linear relationships

Resistant to overfitting

Works well with tabular data

No feature scaling required

Strong baseline for many ML problems

🔹 Random Forest Limitations

Less interpretable than single tree

Slower training than Logistic Regression

Large models consume more memory

Not ideal for very large datasets

🔹 Final Verdict

Random Forest is superior to single Decision Tree

Good trade-off between performance and stability

Preferred model for structured datasets

Foundation for advanced ensemble methods
