# Introduction to Support Vector Machines

Support Vector Machines (SVMs) are supervised learning methods used for classification and regression. In classification, an SVM seeks a decision boundary with a large margin between classes. The training examples that determine the boundary are called support vectors.

## SVC and SVR

- **Support Vector Classification (SVC):** predicts discrete class labels.
- **Support Vector Regression (SVR):** predicts continuous target values while using an epsilon-insensitive loss formulation.

## Why scaling matters

SVM optimization and distance-based kernel calculations can be sensitive to feature magnitudes. Scaling numerical features is generally important. Fit preprocessing only on the training data; using a Scikit-learn `Pipeline` helps prevent leakage during cross-validation.

## Important parameters

- `C`: controls the trade-off between margin width and training errors.
- `kernel`: selects the decision function similarity used by the model.
- `gamma`: controls the influence range of individual training examples for kernels such as RBF, polynomial, and sigmoid.
- `degree`: polynomial-kernel degree.
- `epsilon`: width of the insensitive tube in SVR.

Parameter effects depend on the dataset and should be assessed using cross-validation rather than assumed in advance.

