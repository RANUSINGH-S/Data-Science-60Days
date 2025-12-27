Decision Trees & The Art of Pruning
1. Decision Trees vs. Logistic Regression
Logistic Regression: A linear classifier that draws a straight line (hyperplane) to separate classes. It assumes features have a direct, additive relationship with the target.

Decision Tree: A non-linear classifier that splits data based on a series of "Yes/No" questions. It excels at capturing feature interactions (e.g., "High Alcohol is only good if Volatile Acidity is low").

2. How Trees Make Decisions (Gini Impurity)
The tree decides where to "cut" the data based on Gini Impurity.

It looks for the split that creates the most "pure" groups (groups where most items belong to a single class).

Gini = 0 means a node is perfectly pure (all "Good" or all "Bad" wine).

3. The Overfitting Problem (High Variance)
An unconstrained tree (no max_depth limit) is a "greedy" learner. It will keep splitting until every single data point is accounted for.

The Symptom: You see 100% Training Accuracy but much lower Test Accuracy.

The Reason: The model has "memorized" the noise and specific examples in the training set rather than learning general patterns.

4. Pruning (Hyperparameter Tuning)
Pruning is the process of limiting the tree's growth to improve its ability to work on new data (generalization).

max_depth: The most common way to prune. It limits how many levels of questions the tree can ask.

The Sweet Spot: We use a loop to find the depth where the Test Accuracy is at its peak. After this point, the model begins to overfit.

5. Key Visualization: plot_tree
Visualizing the tree allows us to see the Root Node (the most important feature used for the first split) and the logic flow.

Observation from today: Alcohol is frequently the root node, confirming our Day 11 SHAP findings.
