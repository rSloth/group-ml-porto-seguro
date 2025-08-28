# Porto Seguro - Safe Driver Prediction

- Company:         Porto Seguro (insurance)
- Task:            Predict whether a driver will file an insurance claim in the next year
- Target Variable: Binary (target = 0 or 1)
- Why good:        Large insurance dataset, real business case, tabular only
- Link:            [Porto Seguro Safe Driver]("https://www.kaggle.com/competitions/porto-seguro-safe-driver-prediction/overview")

This project explores different machine learning models to predict the probability that a driver will initiate an insurance claim. The dataset is provided by Porto Seguro through a Kaggle competition.

## 📁 Project Structure

```
group-ml-porto-seguro/
├── data/                  # empty
├── eda/                   # Exploratory Data Analysis
├── models/                # All model notebooks and comparison tables
│   ├── baseline_reg.ipynb
│   ├── Luca_models.ipynb
│   ├── robin_random_forest.ipynb
│   ├── singe_tree.ipynb
│   ├── Model_Comparison_Table.md
├── requirements.txt       # List of dependencies
├── README_NEW.md          # Project documentation
```

## Objective

The goal is to build and compare multiple ML models to identify those most effective in predicting the probability of a car insurance claim. 

## Models Implemented

- Dummy Classifier (Baseline)
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Random Forest (with and without SMOTE)
- XGBoost (with scale_pos_weight and SMOTE)
- Voting Classifier (Soft Voting with and without weights)

See [`Model_Comparison_Table.md`](./models/Model_Comparison_Table.md) for full performance metrics.

## Metrics Used

- Precision, Recall, F1-score
- ROC-AUC Score
- Confusion Matrix

Due to heavy class imbalance, **Recall on class 1** and **ROC-AUC** were key indicators of model effectiveness.

## Installation

To run the project locally:

```bash
git clone https://github.com/your-username/group-ml-porto-seguro.git
cd group-ml-porto-seguro
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## How to Run

Run the notebooks under the `models/` directory to reproduce results. For model comparison, check:

```bash
models/Model_Comparison_Table.md
```

## Team

- Luca 
- Marcel
- Robin
---

## Notes

- SMOTE was carefully applied **only to training data** to prevent data leakage.
- Feature scaling was avoided where not necessary (e.g. tree-based models).
