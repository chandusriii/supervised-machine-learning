# Ensemble Learning

This section explores ensemble methods through hands-on classification and regression examples.

## Notebooks

- [Random Forest and Bagging](01_Random_Forest_and_Bagging.ipynb) — compares a Decision Tree baseline, Random Forest with out-of-bag (OOB) evaluation, and Bagging Classifiers using the Titanic dataset.
- [Bagging Regressor and Boosting](02_Bagging_Regressor_and_Boosting.ipynb) — an additional learning example comparing Decision Tree regression, Bagging Regressor, AdaBoost Regressor, and Gradient Boosting Regressor using the Diabetes dataset.

## Concept notes

- [Ensemble learning introduction](concepts/ensemble_learning.md)
- [Bagging vs Boosting](concepts/bagging_vs_boosting.md)
- [Decision Tree vs Random Forest](concepts/decision_tree_vs_random_forest.md)
- [Out-of-Bag evaluation](concepts/oob_evaluation.md)

## Key ideas

- Bagging aggregates models trained on bootstrap samples.
- Random Forest also introduces randomness in feature selection when growing trees.
- OOB evaluation uses training observations left out of a tree's bootstrap sample.
- Boosting builds an ensemble sequentially, with each stage attempting to improve the existing ensemble.
- Compare methods on the same held-out data and use metrics suited to classification or regression.

The Bagging Regressor and Boosting notebook is an additional learning example created to extend the original classification experiments; it is not part of the original uploaded code.
