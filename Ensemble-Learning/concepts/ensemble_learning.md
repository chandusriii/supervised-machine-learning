# Introduction to Ensemble Learning

Ensemble learning combines predictions from multiple models. The aim is to improve generalization, stability, or predictive performance compared with relying on a single estimator.

## Common approaches

- **Bagging:** trains models on bootstrap samples and combines their predictions. It can reduce variance for unstable learners such as decision trees.
- **Random Forest:** trains decision trees using bootstrap sampling and randomized feature selection, then aggregates tree predictions.
- **Boosting:** builds a sequence of learners in which later learners focus on improving the ensemble's current performance.

## Evaluation

Use the same train/test split and appropriate metrics when comparing models. For classification, consider accuracy, precision, recall, F1-score, and a confusion matrix. For regression, consider MAE, RMSE, and R². Match the metric to the problem and class balance.
