# SVM Hyperparameters

Hyperparameters are configuration choices made before model fitting. Tune them with cross-validation on training data and evaluate the final selection on a held-out test set.

| Parameter | Used with | Meaning |
|---|---|---|
| `C` | SVC and SVR | Regularization strength trade-off; lower values allow more regularization. |
| `kernel` | SVC and SVR | Kernel function, such as `linear`, `poly`, `rbf`, or `sigmoid` where supported. |
| `gamma` | Relevant nonlinear kernels | Controls the influence range of training examples. |
| `degree` | Polynomial kernel | Polynomial degree. |
| `epsilon` | SVR | Width of the region where errors do not incur the usual epsilon-insensitive loss. |

## GridSearchCV workflow

- Define a parameter grid.
- Use a pipeline so scaling is fit within each training fold.
- Run `GridSearchCV` with an appropriate cross-validation strategy and scoring metric.
- Inspect `best_params_` and `best_score_`.
- Evaluate `best_estimator_` on held-out test data.

Avoid choosing hyperparameters based on repeated test-set scores, because that turns the test set into part of the model-selection process.
