# Common SVM Kernels

A kernel lets an SVM model relationships through a similarity function. The best choice depends on the dataset; compare alternatives using a consistent validation strategy.

## Linear

Useful when a linear decision boundary is appropriate. It is often a strong baseline and can be efficient for high-dimensional data.

## Polynomial

Models interactions with a polynomial kernel. The `degree` parameter controls the polynomial degree, while `C` and other kernel parameters influence the fit.

## Radial Basis Function (RBF)

A flexible nonlinear kernel. The `gamma` parameter controls how far the influence of an individual training example reaches; `C` controls the penalty for training errors.

## Sigmoid

Uses a sigmoid-shaped kernel function. Its behavior depends on its parameters and data scaling, so it should be evaluated empirically rather than presumed to be best.

## Fair comparison checklist

1. Split into train and test sets.
2. Put feature scaling and the classifier inside a pipeline.
3. Compare kernels using cross-validation on training data.
4. Choose metrics suitable for the task and class distribution.
5. Evaluate the selected model once on the held-out test set.
