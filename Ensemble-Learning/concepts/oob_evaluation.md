# Out-of-Bag (OOB) Evaluation

Bootstrap-based ensemble estimators train each base learner on a sample drawn with replacement. Some training observations are not selected for a particular learner's bootstrap sample; those observations are called out-of-bag for that learner.

When supported and enabled, an estimator can aggregate predictions for training observations that were out-of-bag and use them to calculate an internal performance estimate. In Scikit-learn's `RandomForestClassifier`, this can be enabled with `oob_score=True` when bootstrap sampling is used.

## How to use it

```python
from sklearn.ensemble import RandomForestClassifier

model = RandomForestClassifier(
    n_estimators=300,
    bootstrap=True,
    oob_score=True,
    random_state=42
)
model.fit(X_train, y_train)
print(model.oob_score_)
```

## Important caveats

- OOB performance is an internal estimate, not a replacement for a separate test set.
- The estimate can be less stable when the forest has too few trees.
- Preprocessing should be considered carefully; if learned transformations are fit once on all training rows before the forest bootstraps, those transformations have seen rows that may later be OOB for individual trees.
- Use task-appropriate metrics and compare with held-out test performance.
