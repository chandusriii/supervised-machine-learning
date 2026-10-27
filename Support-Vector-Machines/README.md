# Support Vector Machines

This section contains practical SVC and SVR examples plus short concept notes.

## Notebooks

- [SVC Implementation](01_SVC_Implementation.ipynb): Iris classification, scaling, classification metrics, four kernel experiments, and `GridSearchCV`.
- [SVR Implementation](02_SVR_Implementation.ipynb): Diabetes regression, feature/target scaling, Linear and Polynomial kernels, cross-validated hyperparameter search, and LinearSVR.

## Concept notes

- [SVM introduction](concepts/svm_introduction.md)
- [Common SVM kernels](concepts/svm_kernels.md)
- [SVM hyperparameters](concepts/svm_hyperparameters.md)

## Implementation notes

- Scale inputs for SVM models. The SVR notebook fits feature scaling on training data.
- Use pipelines when cross-validating preprocessing to prevent data leakage.
- Select hyperparameters through cross-validation on training data, then evaluate the selected estimator on held-out test data.
- In SVR, the target is standardized for training and predictions can be inverse-transformed for MAE/RMSE in the original target units.
