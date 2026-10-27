# Decision Tree vs Random Forest

A Decision Tree makes predictions by applying a sequence of feature-based splits. It is easy to visualize and explain, but a deep tree may overfit and can be sensitive to small changes in training data.

A Random Forest aggregates predictions from many decision trees trained with sample and feature randomness. Aggregation often improves stability and generalization, usually at the cost of reduced interpretability and additional computation.

| Aspect | Decision Tree | Random Forest |
|---|---|---|
| Model | Single tree | Ensemble of trees |
| Interpretability | Usually easier to inspect | Harder to explain as a whole |
| Variance | Can be high | Often reduced through aggregation |
| Compute and storage | Usually lower | Usually higher |
| Feature importance | Available, with caveats | Available, with caveats |

Compare models using the same data split and relevant metrics. Do not rely on training accuracy alone; inspect held-out performance and potential overfitting.
