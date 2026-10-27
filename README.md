# Supervised Machine Learning

A hands-on Python repository for learning supervised machine learning through practical experiments, focused on Support Vector Machines and Ensemble Learning.

The goal is to keep the examples beginner-friendly while making the experiments reproducible and explaining important modelling choices. Original uploaded notebooks are kept as the basis of the project; added examples are labelled as extensions.

## Contents

### Support Vector Machines

| Notebook / Guide | What you'll learn |
|---|---|
| [SVC Implementation](Support-Vector-Machines/01_SVC_Implementation.ipynb) | Iris classification, feature scaling, classification metrics, Linear/Polynomial/RBF/Sigmoid kernels, and GridSearchCV |
| [SVR Implementation](Support-Vector-Machines/02_SVR_Implementation.ipynb) | Diabetes regression, feature and target scaling, Linear/Polynomial kernels, GridSearchCV, LinearSVR, MAE, RMSE, and R² |
| [SVM section guide](Support-Vector-Machines/README.md) | How to navigate the SVM material |
| [SVM introduction](Support-Vector-Machines/concepts/svm_introduction.md) | SVC vs. SVR, support vectors, and feature scaling |
| [SVM kernels](Support-Vector-Machines/concepts/svm_kernels.md) | Linear, Polynomial, RBF, and Sigmoid kernels |
| [SVM hyperparameters](Support-Vector-Machines/concepts/svm_hyperparameters.md) | C, gamma, degree, epsilon, and tuning workflow |

### Unsupervised Learning

| Notebook / Guide | What you'll learn |
|---|---|
| [Clustering fundamentals notebook](Unsupervised-Learning/01_KMeans_Iris_Elbow_Silhouette.ipynb) | Iris features, K-Means, inertia, elbow method, silhouette score, and cluster visualization |
| [Hierarchical and DBSCAN notebook](Unsupervised-Learning/02_Hierarchical_Dendrogram_DBSCAN.ipynb) | Dendrograms, linkage, K-Means vs. hierarchical clustering, DBSCAN, noise points, and cluster evaluation |
| [Unsupervised learning guide](Unsupervised-Learning/README.md) | Definitions, practical trade-offs, workflow, and official Scikit-learn documentation |

### Ensemble Learning

| Notebook / Guide | What you'll learn |
|---|---|
| [Random Forest and Bagging](Ensemble-Learning/01_Random_Forest_and_Bagging.ipynb) | Decision Tree baseline, Random Forest, OOB evaluation, Bagging Classifiers, and test-set comparison |
| [Bagging Regressor and Boosting](Ensemble-Learning/02_Bagging_Regressor_and_Boosting.ipynb) | Additional example comparing Decision Tree regression, Bagging Regressor, AdaBoost Regressor, and Gradient Boosting Regressor |
| [Ensemble section guide](Ensemble-Learning/README.md) | How to navigate ensemble learning material |
| [Ensemble introduction](Ensemble-Learning/concepts/ensemble_learning.md) | Overview of ensemble methods |
| [Bagging vs. Boosting](Ensemble-Learning/concepts/bagging_vs_boosting.md) | Key differences and examples |
| [Decision Tree vs. Random Forest](Ensemble-Learning/concepts/decision_tree_vs_random_forest.md) | Interpretability, variance, and practical comparison |
| [Out-of-Bag evaluation](Ensemble-Learning/concepts/oob_evaluation.md) | OOB estimates and caveats |

## Learning objectives

- Understand supervised classification and regression.
- Learn unsupervised learning and clustering methods, including K-Means, hierarchical clustering, and DBSCAN.
- Explore SVM kernels and important model hyperparameters.
- Use pipelines and cross-validation to tune models.
- Learn the differences between Decision Trees, Random Forest, Bagging, and Boosting.
- Evaluate models with metrics suited to their prediction task.
- Recognize potential data leakage and the importance of a held-out test set.

## Repository structure

```text
supervised-machine-learning/
├── README.md
├── requirements.txt
├── .gitignore
├── LICENSE
├── .github/
│   └── workflows/
│       └── validate-notebooks.yml
├── Support-Vector-Machines/
│   ├── README.md
│   ├── 01_SVC_Implementation.ipynb
│   ├── 02_SVR_Implementation.ipynb
│   └── concepts/
│       ├── svm_introduction.md
│       ├── svm_kernels.md
│       └── svm_hyperparameters.md
└── Ensemble-Learning/
    ├── README.md
    ├── 01_Random_Forest_and_Bagging.ipynb
    ├── 02_Bagging_Regressor_and_Boosting.ipynb
    └── concepts/
        ├── ensemble_learning.md
        ├── bagging_vs_boosting.md
        ├── decision_tree_vs_random_forest.md
        └── oob_evaluation.md
```

## Technology stack

- Python
- Jupyter Notebook
- NumPy and Pandas
- Scikit-learn
- Matplotlib
- Seaborn

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

Open a notebook and run its cells from top to bottom.

## Datasets

- **Iris:** included with Scikit-learn and used for SVC classification.
- **Diabetes:** included with Scikit-learn and used for SVR and regression-ensemble examples.
- **Titanic:** loaded by Seaborn; initial loading may require internet access.

## Evaluation metrics

**Classification:** accuracy, precision, recall, F1-score, classification report, and confusion matrix.

**Regression:** mean absolute error (MAE), root mean squared error (RMSE), and coefficient of determination (R²).

Choose metrics based on the problem and data. Avoid comparing models using unrelated metrics or different test splits.

## Implementation and validation status

The notebooks are organized and revised, and supporting topic notes have been added. The repository includes a GitHub Actions workflow intended to execute the notebooks on pushes and pull requests. Check the **Actions** tab for the result of the latest workflow run.

Notebook execution has not yet been independently confirmed from this chat session. Please check the workflow result or run each notebook from top to bottom after installing the dependencies before treating its numerical outputs as validated. Dataset access and library-version differences may affect execution.

The Bagging Regressor and Boosting notebook is an additional learning example created to extend the original classification experiments; it is not part of the original uploaded notebook.

## Future improvements

- Confirm all notebooks execute end-to-end in a clean environment.
- Add visual comparisons of model metrics.
- Explore feature importance and model interpretation.
- Add additional cross-validation and hyperparameter-search examples.
- Expand to other supervised learning algorithms.

## License

See [LICENSE](LICENSE) for the license terms.
