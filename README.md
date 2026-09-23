# Logistic Regression: 30 Practical Projects

<div align="center">

[![Python](https://img.shields.io/badge/Python-3.9%2B-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![scikit--learn](https://img.shields.io/badge/scikit--learn-Modeling-F7931E?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Projects](https://img.shields.io/badge/Projects-30-6C63FF)](#project-highlights)
[![License](https://img.shields.io/badge/License-MIT-22C55E)](LICENSE)

### A visual, interview-ready portfolio of binary classification projects

From predicting student outcomes to detecting spam, this notebook demonstrates how logistic regression turns real-world questions into measurable decisions.

[Explore the notebook](./logistic_regression_30_Practical_.ipynb) · [Run in Colab](https://colab.research.google.com/github/sgsinghashka-del/Logistic-Regression_30-Practical-Projects/blob/main/logistic_regression_30_Practical_.ipynb)

![Portfolio preview](./assets/project-preview.svg)

</div>

---

## Why this project stands out

This is more than a single model: it is a repeatable classification workflow applied to **30 practical scenarios**. Each mini-project follows the same professional pattern:

1. Load and inspect a focused dataset.
2. Prepare features and encode the target label.
3. Train a `LogisticRegression` model.
4. Evaluate predictions with accuracy and a classification report.
5. Visualize the decision context.
6. Test a new, user-provided example.

The result is a compact portfolio that is easy to explain in an interview and easy to extend with better datasets, validation, and deployment.

## Project highlights

| # | Business question | Main feature | Output |
|---:|---|---|---|
| 01 | Will a student pass? | Study hours | Pass / Fail + probability |
| 02 | May an employee leave? | Years in company | Stay / Leave |
| 03 | Is an email spam? | Email text | Spam / Not spam |
| 04 | Will a visitor purchase? | Time spent | Purchase / No purchase |
| 05 | Is an employee promotion-ready? | Years of experience | Promoted / Not promoted |
| 06 | Is an employee likely to be absent? | Previous absences | Absent / Present |
| 07 | Will a product be returned? | Days used | Returned / Not returned |
| 08 | Will a candidate be selected? | Interview score | Selected / Not selected |
| 09 | Will an offer be accepted? | Offered salary | Accepted / Rejected |
| 10–30 | Additional practical classification problems | Structured and text features | Binary predictions |

> The notebook is the source of truth for the complete set of 30 exercises and their datasets.

## Visual portfolio map

| Area | Examples | Techniques demonstrated |
|---|---|---|
| **People & careers** | Attrition, promotion, absenteeism, selection | Numeric features, label mapping, probability estimates |
| **Customer behavior** | Purchase, returns, offer acceptance | Decision boundaries, exploratory plots, predictions |
| **Communication** | Email spam detection | TF–IDF vectorization + logistic regression |
| **Education** | Pass/fail prediction | Train/test split, metrics, interactive inference |

## Quick start

### 1. Clone the repository

```bash
git clone https://github.com/sgsinghashka-del/Logistic-Regression_30-Practical-Projects.git
cd Logistic-Regression_30-Practical-Projects
```

### 2. Create an environment

```bash
python -m venv .venv

# macOS/Linux
source .venv/bin/activate

# Windows PowerShell
.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch the notebook

```bash
jupyter notebook logistic_regression_30_Practical_.ipynb
```

Or open the notebook directly in Google Colab using the badge above.

## Example workflow

```python
from sklearn.linear_model import LogisticRegression
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score, classification_report

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42, stratify=y
)

model = LogisticRegression()
model.fit(X_train, y_train)

predictions = model.predict(X_test)
print(f"Accuracy: {accuracy_score(y_test, predictions):.2%}")
print(classification_report(y_test, predictions))
```

For text classification, the notebook adds a `TfidfVectorizer` before fitting the model so that email language can be represented numerically.

## What to discuss in an interview

- **Why logistic regression?** It is fast, interpretable, and naturally provides class probabilities for binary decisions.
- **What does the probability mean?** It is the model's estimated likelihood for the positive class—not a guarantee.
- **Why split the data?** To evaluate how the model performs on examples it did not train on.
- **What would you improve?** Add cross-validation, stronger datasets, feature scaling where appropriate, threshold tuning, confusion matrices, ROC-AUC, and a reproducible pipeline.
- **What is the main limitation?** Results are only as reliable as the small teaching datasets and selected features; they should not be used for high-impact decisions without deeper validation and bias review.

## Repository structure

```text
.
├── logistic_regression_30_Practical_.ipynb  # Main portfolio notebook
├── assets/
│   └── project-preview.svg                  # README visual preview
├── requirements.txt                          # Reproducible Python dependencies
├── .gitignore                                # Clean Python/Jupyter defaults
├── LICENSE                                   # MIT license
└── README.md                                 # Project guide and interview notes
```

## Roadmap

- [ ] Add a `data/` directory with documented schemas for every exercise.
- [ ] Refactor repeated code into reusable training/evaluation functions.
- [ ] Add confusion matrices and ROC-AUC to each classification task.
- [ ] Add cross-validation and a reproducible random seed strategy.
- [ ] Publish a lightweight Streamlit demo.
- [ ] Add automated notebook execution with GitHub Actions.

## Responsible use

These examples are educational demonstrations. The datasets are small and should not be treated as production-ready evidence, especially for employment, education, or other high-impact decisions. Validate models on representative data, inspect errors, and assess fairness before real-world use.

## License

Distributed under the MIT License. See [LICENSE](./LICENSE).

---

<div align="center">

**Built as a practical machine-learning learning portfolio.**

</div>
