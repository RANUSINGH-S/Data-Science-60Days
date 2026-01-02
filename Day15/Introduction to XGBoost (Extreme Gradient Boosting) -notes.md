Day 15: Introduction to XGBoost (Extreme Gradient Boosting)
XGBoost is a state-of-the-art implementation of Gradient Boosting designed for speed and performance. It is a "sequentially built" model, meaning it learns from its own mistakes.

1. The Core Logic: Sequential Learning
In a Random Forest, trees are independent. In XGBoost, trees are built one after another:

Step 1: Build a simple tree to predict the target.

Step 2: Calculate the errors (residuals) made by that tree.

Step 3: Build a second tree that specifically tries to predict those errors.

Step 4: Combine the trees. Repeat this process hundreds of times.

2. Key Hyperparameters to Know
learning_rate (eta): Controls how much each new tree "corrects" the previous ensemble. A smaller value (like 0.01 or 0.1) makes the model more robust but requires more trees.

n_estimators: The number of sequential trees to build.

max_depth: Limits the depth of each individual tree to prevent it from becoming too complex and overfitting.

gamma: A regularization parameter that decides if a node should split based on the expected reduction in loss.

3. Why XGBoost is a "Winner"
Regularization: It has built-in L1 and L2 regularization which prevents the model from overfitting.

Handling Missing Values: It has a built-in strategy for handling missing data.

Speed: It is highly optimized for parallel processing.

4. Implementation Steps (Python)
A. Installation & Import

Python

# Install if necessary: !pip install xgboost
import xgboost as xgb
from xgboost import XGBClassifier
from sklearn.metrics import accuracy_score
B. Basic Training

Python

# Initialize the model
xgb_model = XGBClassifier(
    n_estimators=100, 
    learning_rate=0.1, 
    max_depth=6, 
    random_state=42,
    eval_metric='logloss' # Common metric for classification
)

# Fit the model on your scaled data
xgb_model.fit(x_train_scaled, y_train)
C. Evaluation

Python

# Predict and check accuracy
preds = xgb_model.predict(x_test_scaled)
print(f"XGBoost Accuracy: {accuracy_score(y_test, preds):.4f}")
5. Summary of Progress So Far
By the end of today, your "Leaderboard" in your notebook should look like this:

Logistic Regression (Day 11): Baseline accuracy.

Decision Tree (Day 12): Good for logic, but prone to high variance.

Random Forest (Day 13-14): Parallel ensemble (Bagging) - currently your best at ~74.24%.

XGBoost (Day 15): Sequential ensemble (Boosting) - Can you beat the 74% mark?

Day 15 Goal: Successfully run your first XGBoost model and compare its test accuracy to your tuned Random Forest from Day 14. 
