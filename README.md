# Interpretable Machine Learning for Tennis Match Prediction

An end-to-end machine learning project exploring ATP tennis match
prediction, temporal validation and model interpretability.

Developed as part of my Computer Science dissertation at the
University of York.

## Project Overview

This project investigates whether machine learning models can
accurately predict professional tennis match outcomes and how
their predictions can be explained.

Using ATP singles match data from 2013–2024, I developed a
pipeline covering data preparation, feature engineering,
model training, evaluation and interpretability analysis.

A particular focus was avoiding data leakage by ensuring
predictions were based only on information available before
each match.

## Technologies Used

- Python
- pandas and NumPy
- scikit-learn
- XGBoost
- SHAP
- Matplotlib
- Jupyter Notebook

## Machine Learning Pipeline

The project is organised into six notebooks:

| Notebook | Description |
|---|---|
| `01_data_loading.ipynb` | Loads and combines ATP match, ranking and player data |
| `02_data_cleaning.ipynb` | Cleans and prepares datasets |
| `03_feature_engineering.ipynb` | Creates pre-match predictive features |
| `04_modeling.ipynb` | Trains and evaluates machine learning models |
| `05_shap.ipynb` | Investigates model predictions using SHAP |
| `06_results_visualisations.ipynb` | Produces results tables and visualisations |

All notebooks are located in the `notebooks/` directory.

## Predictive Features

Features include:

- ATP ranking differences
- Elo rating differences
- Surface-specific player performance
- Recent match form
- Rolling serve and return statistics

Features were constructed using historical information to
avoid incorporating future match results into predictions.

## Models Evaluated

Four machine learning approaches were compared:

1. Logistic Regression
2. Decision Tree
3. Random Forest
4. XGBoost

## Evaluation Methodology

The models were assessed using rolling-origin validation,
which better reflects real-world prediction than randomly
splitting historical tennis matches.

Performance was evaluated using:

- Accuracy
- Log loss
- Brier score

## Key Results

- Classification accuracy ranged from approximately **64.5% to 65.7%**.
- More complex models did not consistently outperform simpler alternatives.
- Elo ratings and ranking differences were important predictive features.
- SHAP analysis helped explain both overall model behaviour and individual predictions.

These findings highlight the value of combining predictive
performance with interpretability.

## Repository Structure

```text
tennis-match-prediction/
├── notebooks/
│   ├── 01_data_loading.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_feature_engineering.ipynb
│   ├── 04_modeling.ipynb
│   ├── 05_shap.ipynb
│   └── 06_results_visualisations.ipynb
├── data/
├── outputs/
├── README.md
└── .gitignore
```

## Data Sources

This project uses historical ATP tennis data compiled by
Jeff Sackmann:

https://github.com/JeffSackmann/tennis_atp

The original datasets are not included in this repository.

The source data is subject to its own licensing terms,
including attribution and non-commercial restrictions.

## Reproducibility

The notebooks are provided in pipeline order.

The full pipeline requires the original ATP datasets and
the relevant Python dependencies.

Detailed setup instructions will be added as the repository
is prepared for public release.

## Author

**Bailey Horsley**

MEng Computer Science — University of York