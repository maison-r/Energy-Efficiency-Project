# Building Energy Load Prediction using Linear Regression

This project aims to predict the **heating load** of different building designs using **supervised learning**. The goal is to explore how design features such as orientation, glazing, and surface area impact heating requirements.

## Dataset
The dataset consists of 768 building design samples with 8 numerical input features and one continuous target (heating load). It was provided as part of a university assignment.

##  Objectives
- Train and evaluate a **linear regression** model
- Explore the effect of **data splitting** methods
- Apply **PCA** for dimensionality reduction
- Investigate the impact of **Ridge regularization**

##  Methods
- Train/test splits: random vs. grouped
- Evaluation metrics: MAE, RMSE, R²
- Dimensionality reduction via PCA
- Regularized regression (Ridge)

##  Results Summary
| Metric         | Linear Reg. | PCA (3 comp) | Ridge + PCA |
|----------------|-------------|--------------|-------------|
| MAE            | 2.15        | ↑ (worse)    | same        |
| RMSE           | 2.97        | ↑            | same        |
| R²             | 0.91        | ↓            | ↓           |

- **Linear regression** with original features performs best.
- **PCA** reduces performance due to loss of signal.
- **Ridge regression** does not improve results, indicating no overfitting.

##  Key Learnings
- Splitting strategy affects generalization
- Model performance depends on feature selection
- PCA and regularization should be validated for impact

## How to Run
```bash
pip install -r Requirements.txt
jupyter lab notebooks/building_energy_prediction.ipynb
