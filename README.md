# Undergraduate Thesis — Python Reconstruction
The Python implementation replicates the original SPSS results and extends the analysis with robustness checks and penalized regression methods.

## Research Topic
Analysis of the influence of investment knowledge, knowledge of the US–China trade war, and risk perception on stock investment decisions in Indonesia.

## Methods
- Ordinary Least Squares (OLS)
- HC3 robust standard errors
- Multicollinearity diagnostics (VIF)
- Heteroskedasticity testing (Breusch–Pagan)
- Regression diagnostics
- Ridge and Lasso regression (robustness)

## Objective
To improve transparency, reproducibility, and methodological rigor using Python.

## Project Structure
data/
  raw/        Original SPSS and cleaned raw survey data
  processed/  Final constructed dataset used for analysis

notebooks/
  01_data_cleaning.ipynb
  02_ols_baseline.ipynb
  03_diagnostics.ipynb
  04_regularization_ridge_lasso.ipynb

figures/
  Residual diagnostics and model plots

results/
  regression_tables.md
  discussions.md
  conclusion.md

## Key Findings
- Knowledge of the US–China trade war (X2) is the only predictor that is consistently statistically significant across models.
- Investment knowledge (X1) and risk perception (X3) are not statistically significant once other factors are controlled for.
- Ridge regression confirms coefficient stability.
- Lasso regression indicates weak overall predictive signal under sparsity constraints.

## Status
Completed (analysis finalized and archived for reproducibility)
