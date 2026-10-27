# Supervised Machine Learning

A hands-on Python repository documenting practical experiments with supervised machine learning. The project focuses on Support Vector Machines (SVC and SVR) and Ensemble Learning, with beginner-friendly notebooks, explanations, and model evaluation.

> This repository is a work in progress. The notebook links below will become available as the corresponding notebooks are added and reviewed.

## Learning goals

- Understand classification and regression workflows.
- Explore Support Vector Classification (SVC) and Support Vector Regression (SVR).
- Compare Linear, Polynomial, RBF, and Sigmoid SVM kernels.
- Understand hyperparameters and model selection with `GridSearchCV`.
- Explore Decision Trees, Random Forest, Bagging, Boosting, and out-of-bag (OOB) evaluation.
- Evaluate models using metrics appropriate to each task.
- Practice reproducible experiments and clear documentation.

## Repository roadmap

### Support Vector Machines

| Planned notebook | What it covers |
|---|---|
| `01_SVC_Implementation.ipynb` | SVC classification workflow, feature scaling, kernel experiments, and classification metrics. |
| `02_SVR_Implementation.ipynb` | SVR regression workflow, scaling, regression metrics, and hyperparameter search. |

Topics to document alongside the notebooks include support vectors, decision boundaries, SVM hyperparameters, kernel functions, and `GridSearchCV`.

### Ensemble Learning

| Planned notebook | What it covers |
|---|---|
| `01_Random_Forest_and_Bagging.ipynb` | Decision Tree, Random Forest, OOB evaluation, and Bagging Classifier experiments. |

Planned extensions include Bagging Regressor, Boosting, and a comparison of tree-based ensemble approaches. These are roadmap items until their implementations are added and tested.

## Planned structure

```text
supervised-machine-learning/
├── README.md
├── requirements.txt
├── .gitignore
├── LICENSE
├── Support-Vector-Machines/
│   ├── README.md
│   ├── 01_SVC_Implementation.ipynb
│   ├── 02_SVR_Implementation.ipynb
│   └── concepts/
└── Ensemble-Learning/
    ├── README.md
    ├── 01_Random_Forest_and_Bagging.ipynb
    └── concepts/
```

The structure is a roadmap; folders and notebooks will be added as the existing work is organized.

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

Open a notebook and run its cells in order. Individual notebooks may have additional dataset or environment requirements; these should be documented in their own README files.

## Datasets and evaluation

The current learning plan uses familiar educational datasets, including Iris for classification, Diabetes for regression, and Titanic for classification experiments. The final notebook documentation should identify the exact dataset source and preprocessing used.

Candidate evaluation metrics include:

- **Classification:** accuracy, precision, recall, F1-score, and confusion matrix.
- **Regression:** R², Mean Absolute Error (MAE), and Root Mean Squared Error (RMSE).

Use metrics appropriate to each task and evaluate model-selection choices on training data with cross-validation before making a final assessment on held-out test data.

## Contribution and learning approach

This is a personal learning portfolio. Existing implementations will be preserved where practical. Corrections, refactoring, and new examples will be documented so the distinction between original experiments and later improvements remains clear.

## Future improvements

- Add and test the original SVC, SVR, and Random Forest notebooks.
- Explain SVM kernel types and key hyperparameters.
- Demonstrate robust preprocessing with Scikit-learn pipelines.
- Compare models with appropriate evaluation metrics and cross-validation.
- Add Bagging Regressor and Boosting examples.
- Add concise concept notes, diagrams, and reproducible results.

## License

See [LICENSE](LICENSE) for license terms.
