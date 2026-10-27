# Supervised Machine Learning

A hands-on Python repository documenting practical experiments with supervised machine learning, focused on Support Vector Machines and Ensemble Learning. It is intended to be a beginner-friendly learning resource and a record of practical work.

## Topics and notebooks

### Support Vector Machines

- [SVC Implementation](Support-Vector-Machines/01_SVC_Implementation.ipynb) — classification with the Iris dataset, feature scaling, SVC evaluation, kernel experiments, and `C` comparisons.
- [SVR Implementation](Support-Vector-Machines/02_SVR_Implementation.ipynb) — regression with the Diabetes dataset, kernel experiments, `GridSearchCV`, and `LinearSVR`.
- [SVM concept notes](Support-Vector-Machines/README.md) — section guide, [introduction](Support-Vector-Machines/concepts/svm_introduction.md), [common kernels](Support-Vector-Machines/concepts/svm_kernels.md), and [hyperparameters](Support-Vector-Machines/concepts/svm_hyperparameters.md).

### Ensemble Learning

- [Random Forest and Bagging](Ensemble-Learning/01_Random_Forest_and_Bagging.ipynb) — Decision Tree, Random Forest with OOB evaluation, and Bagging Classifier experiments using the Titanic dataset.
- [Ensemble concept notes](Ensemble-Learning/README.md) — section guide, [ensemble learning overview](Ensemble-Learning/concepts/ensemble_learning.md), [Bagging vs Boosting](Ensemble-Learning/concepts/bagging_vs_boosting.md), and [Decision Tree vs Random Forest](Ensemble-Learning/concepts/decision_tree_vs_random_forest.md).

> **Status:** The notebooks are organized baseline implementations. They still require a full execution/review pass and some improvements noted during code review, including feature scaling for SVR, using the selected `GridSearchCV` estimator, and leakage-safe preprocessing for the Titanic example. Planned topics such as Bagging Regressor and a practical Boosting notebook are not implemented yet.

## Learning objectives

- Understand classification and regression workflows.
- Explore SVC and SVR, their kernels, and key hyperparameters.
- Learn model selection using cross-validation and `GridSearchCV`.
- Understand Decision Trees, Random Forest, Bagging, Boosting, and OOB evaluation.
- Choose suitable evaluation metrics and build reproducible experiments.

## Technologies

Python, Jupyter Notebook, NumPy, Pandas, Scikit-learn, Matplotlib, and Seaborn.

## Setup

Clone the repository:

```bash
git clone https://github.com/chandusriii/supervised-machine-learning.git
cd supervised-machine-learning
```

Create and activate a virtual environment.

**Windows PowerShell**

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

**macOS / Linux**

```bash
python -m venv .venv
source .venv/bin/activate
```

Install dependencies and launch Jupyter:

```bash
python -m pip install -r requirements.txt
jupyter notebook
```

Open a notebook and run its cells in order. The Titanic notebook downloads its dataset via Seaborn, so it needs network access the first time it loads the dataset. Scikit-learn supplies the Iris and Diabetes datasets.

## Evaluation metrics

The notebooks currently demonstrate accuracy and classification reports for classification, and R² for regression. Improvements planned include confusion matrices, MAE/RMSE for regression, and more consistent cross-validation-based comparisons.

## Next improvements

- Add the RBF kernel to the explicit SVC kernel comparison.
- Put scaling and model fitting into Scikit-learn pipelines where appropriate.
- Avoid using the test set repeatedly for hyperparameter choices.
- Use `grid_search.best_estimator_` after GridSearchCV.
- Add reproducible `random_state` settings and improve categorical preprocessing in the Titanic experiment.
- Add Bagging Regressor and Boosting examples.

## License

See [LICENSE](LICENSE) for licensing terms.
