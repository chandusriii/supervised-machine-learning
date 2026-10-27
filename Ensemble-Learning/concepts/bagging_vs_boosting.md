# Bagging vs Boosting

## Bagging

Bagging (bootstrap aggregating) fits separate base learners on bootstrap samples and combines their predictions. Models can be trained independently. It often helps reduce variance, especially for high-variance learners.

Examples include `BaggingClassifier`, `BaggingRegressor`, and Random Forest (which adds feature randomization to tree bagging).

## Boosting

Boosting combines learners sequentially. Each new learner is trained to improve the current ensemble, with the specific mechanism depending on the boosting algorithm. Boosting can build strong predictors from simpler learners but requires careful tuning and validation.

## Practical comparison

| Aspect | Bagging | Boosting |
|---|---|---|
| Training pattern | Learners are generally independent | Learners are built sequentially |
| Primary intuition | Stabilize predictions by aggregation | Correct errors or optimize an additive model stage by stage |
| Example methods | Bagging, Random Forest | AdaBoost, Gradient Boosting |

Compare methods on the same split, with a clear baseline, appropriate metrics, and cross-validation for model selection.
