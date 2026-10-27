# Ensemble Learning

This section explores how combining models can improve predictive performance and robustness. Existing experiments focus on Decision Trees, Random Forest, and Bagging Classifiers.

## Planned notebooks

- `01_Random_Forest_and_Bagging.ipynb` — Decision Tree baseline, Random Forest, out-of-bag evaluation, and Bagging Classifier examples.

## Concepts

- Ensemble learning overview
- Bagging versus Boosting
- Decision Tree versus Random Forest
- Bootstrap samples and out-of-bag (OOB) evaluation
- Bagging Classifier and Bagging Regressor
- Comparing models using appropriate metrics

## Learning guidelines

Use consistent train/test splits when comparing models. Keep imputation and encoding inside a preprocessing pipeline fitted on training data. Set random seeds where suitable for reproducible experiments. OOB evaluation is available for compatible bootstrap-based estimators when enabled, but it does not replace careful test-set evaluation in every setting.

Boosting and Bagging Regressor are planned extensions until their implementations are added and tested.
