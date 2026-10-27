# Ensemble Learning

This section explores ensemble methods through hands-on classification and regression examples.

## Notebooks

- [01 — Random Forest and Bagging](01_Random_Forest_and_Bagging.ipynb): compares a Decision Tree baseline, Random Forest with out-of-bag (OOB) evaluation, and Bagging Classifiers using the Titanic dataset.
- [02 — Bagging Regressor and Boosting](02_Bagging_Regressor_and_Boosting.ipynb): additional learning example comparing Decision Tree regression, Bagging Regressor, AdaBoost Regressor, and Gradient Boosting Regressor using the Diabetes dataset. This extension was added separately from the original uploaded notebook.

## Concept notes

- [Ensemble learning introduction](concepts/ensemble_learning.md)
- [Bagging vs Boosting](concepts/bagging_vs_boosting.md)
- [Decision Tree vs Random Forest](concepts/decision_tree_vs_random_forest.md)
- [Out-of-Bag evaluation](concepts/oob_evaluation.md)

## Key ideas

- Bagging aggregates learners trained on bootstrap samples and can reduce variance.
- Random Forest combines bootstrap samples with randomized feature selection when growing trees.
- OOB evaluation uses training observations left out of each tree's bootstrap sample; it complements but does not replace held-out test evaluation.
- Boosting builds an ensemble sequentially, with each stage improving the ensemble according to the boosting algorithm.
- Compare methods on the same split and use metrics suited to the prediction task.
