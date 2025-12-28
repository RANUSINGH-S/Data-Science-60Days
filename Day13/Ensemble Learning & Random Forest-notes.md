Ensemble Learning & Random ForestsObjective: Move from a single Decision Tree to a "Forest" to reduce overfitting and improve prediction stability.1. Core Theory: The "Wisdom of the Crowd"A Random Forest is an ensemble of many Decision Trees. It relies on the principle that many uncorrelated models working together will outperform any of the individual constituent models.Key Mechanisms:Bootstrapping (Bagging): Each tree is trained on a random subset of the data (sampling with replacement). This ensures no two trees are identical.Feature Randomness: At every node split, the tree can only choose from a random selection of features. This prevents one dominant feature (like Alcohol) from making every tree look exactly the same.Aggregation: For classification, the forest takes a "Majority Vote." If 70 trees say "Good Wine" and 30 say "Bad Wine," the final output is "Good."2. Implementation: The "Forest" CodeUsing the same scaled data from Day 12, we transition to the RandomForestClassifier.Pythonfrom sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score, classification_report

# 1. Initialize the Forest
# n_estimators = 100 (Total trees in the forest)
# max_depth = 6 (Prevents individual trees from becoming too complex)
rf_model = RandomForestClassifier(n_estimators=100, max_depth=6, random_state=42)

# 2. Train the model
rf_model.fit(X_train_scaled, y_train)

# 3. Predict and Evaluate
rf_preds = rf_model.predict(X_test_scaled)

print(f"Random Forest Accuracy: {accuracy_score(y_test, rf_preds):.4f}")
print("\nClassification Report:\n", classification_report(y_test, rf_preds))
3. Comparative AnalysisMetricLogistic Regression (Day 11)Decision Tree (Day 12)Random Forest (Day 13)LogicLinear EquationIf-Else BranchesMajority VotingOverfitting RiskLow (High Bias)High (High Variance)Low (Best Balance)Accuracy~74%~72% (Pruned)~78-80% (Highest)InterpretabilityCoefficientsTree PlotFeature Importance4. Feature Importance (Global Insight)While you can't plot 100 trees easily, you can plot which features the Forest found most useful across all trees.Pythonimport pandas as pd
import matplotlib.pyplot as plt

# Extracting importance
importances = rf_model.feature_importances_
feat_importances = pd.Series(importances, index=X.columns).sort_values(ascending=True)

# Visualization
plt.figure(figsize=(8,5))
feat_importances.plot(kind='barh', color='teal')
plt.title("Day 13: Most Important Features for Wine Quality")
plt.show()
✅ Day 13 Completion Checklist[x] Understand why "Random" is in the name (Row and Feature sampling).[x] Observe the accuracy jump from Day 12 to Day 13.[x] Identify that Alcohol and Volatile Acidity remain the top predictors even in a complex ensemble.
