# Support Vector Machines

This section contains practical Support Vector Classification (SVC) and Support Vector Regression (SVR) examples, plus short concept notes.

## Notebooks

- [01 — SVC Implementation](01_SVC_Implementation.ipynb): Iris classification, feature scaling, classification metrics, four kernel experiments, and `GridSearchCV`.
- [02 — SVR Implementation](02_SVR_Implementation.ipynb): Diabetes regression, feature and target scaling, Linear and Polynomial kernels, hyperparameter search, `LinearSVR`, MAE, RMSE, and R².

## Concept notes

- [SVM introduction](concepts/svm_introduction.md)
- [Common SVM kernels](concepts/svm_kernels.md)
- [SVM hyperparameters](concepts/svm_hyperparameters.md)

## Practical guidance

- SVM models are sensitive to feature magnitudes; scaling numerical inputs is generally important.
- Fit preprocessing only on training data. Use a pipeline when cross-validating so each fold learns its own preprocessing.
- Tune hyperparameters on training data with cross-validation, then evaluate the selected estimator on held-out test data.
- In the SVR notebook, the target is standardized for the experiment. Predictions are inverse-transformed for MAE and RMSE in the original target units.
- R² is scale invariant when the target and predictions are transformed consistently.
