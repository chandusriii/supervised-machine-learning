# Ensemble Learning

This section explores ensemble methods through hands-on classification examples.

## Notebook

- [Random Forest and Bagging](01_Random_Forest_and_Bagging.ipynb) — compares a Decision Tree baseline, Random Forest with out-of-bag (OOB) evaluation, and Bagging Classifiers using the Titanic dataset.

## Concept notes

- [Ensemble learning introduction](concepts/ensemble_learning.md)
- [Bagging vs Boosting](concepts/bagging_vs_boosting.md)
- [Decision Tree vs Random Forest](concepts/decision_tree_vs_random_forest.md)
- [Out-of-Bag evaluation](concepts/oob_evaluation.md)

## Key ideas

- Bagging aggregates models trained on bootstrap samples.
- Random Forest also introduces randomness in feature selection when growing trees.
- OOB evaluation uses training observations left out of a tree's bootstrap sample.
- Compare methods on the same held-out data and use classification metrics suitable for the task.

## Planned additions

Bagging Regressor and a practical Boosting example are roadmap items and have not yet been added as notebooks.
