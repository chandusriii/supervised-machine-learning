# Supervised Machine Learning

A hands-on Python repository for learning supervised machine learning through practical experiments, focused on Support Vector Machines and Ensemble Learning.

## Topics and notebooks

### Support Vector Machines

- [SVC Implementation](Support-Vector-Machines/01_SVC_Implementation.ipynb) — Iris classification, feature scaling, classification metrics, Linear/Polynomial/RBF/Sigmoid kernels, and GridSearchCV.
- [SVR Implementation](Support-Vector-Machines/02_SVR_Implementation.ipynb) — Diabetes regression, feature scaling, kernel comparisons, GridSearchCV, LinearSVR, MAE, RMSE, and R².
- [SVM section guide](Support-Vector-Machines/README.md) | [Introduction](Support-Vector-Machines/concepts/svm_introduction.md) | [Kernels](Support-Vector-Machines/concepts/svm_kernels.md) | [Hyperparameters](Support-Vector-Machines/concepts/svm_hyperparameters.md)

### Ensemble Learning

- [Random Forest and Bagging](Ensemble-Learning/01_Random_Forest_and_Bagging.ipynb) — Decision Tree baseline, Random Forest with OOB evaluation, and Bagging Classifiers using Titanic data.
- [Ensemble section guide](Ensemble-Learning/README.md) | [Introduction](Ensemble-Learning/concepts/ensemble_learning.md) | [Bagging vs Boosting](Ensemble-Learning/concepts/bagging_vs_boosting.md) | [Decision Tree vs Random Forest](Ensemble-Learning/concepts/decision_tree_vs_random_forest.md)

## Learning goals

- Understand supervised classification and regression.
- Explore SVM kernels and key hyperparameters.
- Use cross-validation for model selection.
- Understand Decision Trees, Random Forest, Bagging, Boosting, and out-of-bag evaluation.
- Evaluate models with metrics appropriate to each task.

## Technology stack

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

Install packages and launch Jupyter:

```bash
python -m pip install -r requirements.txt
jupyter notebook
```

Open a notebook and run its cells in order. The Iris and Diabetes datasets are provided by Scikit-learn. The Titanic dataset is loaded by Seaborn and may require internet access on first use.

## Implementation status

The repository includes SVC and SVR notebooks and a Random Forest/Bagging notebook. The SVM notebooks cover all four requested kernel types across the SVC examples, plus GridSearchCV. The ensemble notebook includes Decision Tree, Random Forest, OOB evaluation, and Bagging Classifier examples. Bagging Regressor and a practical Boosting notebook remain planned extensions rather than completed implementations.

The notebooks are organized and have been improved for scaling, preprocessing, and model selection. They still need a full run-all-cells execution pass in a local environment before all results can be considered verified.

## Next improvements

- Execute every notebook from top to bottom and capture clean outputs.
- Add Bagging Regressor and Boosting examples.
- Expand the comparison of classification and regression metrics.
- Document feature importance and model interpretation.

## License

See [LICENSE](LICENSE) for license terms.
