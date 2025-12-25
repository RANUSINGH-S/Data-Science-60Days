🎯 Objective

Optimize model decision-making, not model structure

Replace default 0.5 threshold with a data-driven threshold

Balance precision and recall based on task requirements

🔹 Probability vs Class Prediction

predict_proba() outputs probabilities (0–1)

predict() converts probabilities into classes

Default conversion uses threshold = 0.5

Threshold value directly controls model behavior

🔹 Why 0.5 Threshold Is Arbitrary

Not derived from data

Ignores class imbalance

Ignores cost of false positives vs false negatives

Often suboptimal for real-world problems

🔹 Effect of Threshold Changes

Increase threshold

Precision increases

Recall decreases

Fewer positive predictions

Decrease threshold

Recall increases

Precision decreases

More positive predictions

🔹 Precision–Recall Tradeoff

Precision focuses on correctness of positive predictions

Recall focuses on capturing all actual positives

Improving one usually harms the other

Tradeoff must be aligned with problem goals

🔹 Threshold Evaluation Strategy

Generated predictions across multiple thresholds

Calculated precision, recall, and F1-score for each

Compared metric changes systematically

Selected threshold with maximum F1-score

🔹 Precision–Recall Curve

Visualizes tradeoff between precision and recall

Independent of fixed threshold

Helps understand model behavior across all thresholds

More informative than ROC for imbalanced datasets

🔹 Final Threshold Selection

Optimal threshold chosen based on highest F1-score

Achieved better balance between precision and recall

Model decision logic improved without retraining

🔹 Key Takeaway

Model performance ≠ model decisions

Same model can behave differently with different thresholds

Threshold tuning is critical in production systems

🏁 Final Decision

Tuned threshold adopted instead of default 0.5

Improved decision quality and metric balance

Model is now decision-aware and business-aligned
I tuned the classification threshold using precision–recall analysis instead of relying on the default 0.5. This allowed me to control false positives and false negatives and select a threshold that maximized F1-score and aligned with real-world decision requirements.
