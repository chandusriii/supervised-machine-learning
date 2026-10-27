# Support Vector Machines

This section covers Support Vector Classification (SVC) and Support Vector Regression (SVR) through practical notebooks. The notebooks will be added after review and testing of the original implementations.

## Planned notebooks

- `01_SVC_Implementation.ipynb` — classification workflow, scaling, kernel comparisons, and evaluation.
- `02_SVR_Implementation.ipynb` — regression workflow, scaling, regression metrics, and hyperparameter tuning.

## Concepts

- Support vectors and decision boundaries
- SVC versus SVR
- Linear, Polynomial, RBF, and Sigmoid kernels
- `C`, `epsilon`, `gamma`, and other relevant hyperparameters
- Cross-validation and `GridSearchCV`

## Learning guidelines

Scale numerical features for SVM models. Fit preprocessing only on training folds, preferably through a Scikit-learn `Pipeline`. Use cross-validation for model selection and keep a held-out test set for final evaluation.
