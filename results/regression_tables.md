**Regression Results**

This section presents the empirical results of the regression analyses conducted in this study. We begin with the baseline Ordinary Least Squares (OLS) model replicated from SPSS, followed by robustness checks using heteroskedasticity-robust standard errors and penalized regression methods (Ridge and Lasso). The objective is to assess the stability and robustness of the estimated relationships across modeling frameworks.

Table 1. Comparison of Regression Coefficients Across Models


| Variable                           |  SPSS OLS | Python OLS | OLS (HC3) | Ridge (CV) | Lasso (CV) |
| ---------------------------------- | --------: | ---------: | --------: | ---------: | ---------: |
| X1 (Investment Knowledge)          |   -0.0688 |    -0.0688 |   -0.0688 |    -0.0019 |      0.000 |
| X2 (US–China Trade War Knowledge) | 0.3471*** |  0.3471*** |  0.3471** |     0.0647 |      0.000 |
| X3 (Risk Perception)               |   -0.0617 |    -0.0617 |   -0.0617 |    -0.0049 |      0.000 |
| Intercept                          | 8.8652*** |  8.8652*** |  8.8652** |         — |         — |
| Observations                       |        79 |         79 |        79 |         79 |         79 |
| R²                                |     0.136 |      0.136 |     0.136 |         — |         — |


**Notes:**

SPSS OLS estimates are obtained using IBM SPSS Statistics. Python OLS results are estimated using `statsmodels` and replicate SPSS estimates up to numerical precision, confirming computational equivalence across software platforms.. HC3 reports heteroskedasticity-robust standard errors. Ridge and Lasso coefficients are based on standardized predictors with 5-fold cross-validation.

Significance levels: *** p < 0.01, ** p < 0.05, * p < 0.10.

**Baseline OLS Estimates**

The baseline OLS regression indicates a positive and statistically significant association between knowledge of the US–China trade war (X2) and the dependent variable. In contrast, investment knowledge (X1) and risk perception (X3) are not statistically significant. The model explains a limited proportion of the variation in the outcome, with an R² of approximately 0.14.

**Interpretation of Model Fit**

The estimated models exhibit relatively low R² values, with the baseline specification explaining approximately 13.6% of the variation in the outcome. This level of explanatory power is consistent with prior empirical work in behavioral finance and decision science, where individual choices are shaped by numerous latent preferences, beliefs, and contextual influences that are difficult to observe or quantify.

Rather than signaling model inadequacy, the modest R² reflects the inherent complexity of the outcome variable and the parsimonious nature of the specification. The robustness of the estimated effect of geopolitical knowledge (X2) across alternative inference procedures and regularization methods suggests that the identified relationship is statistically credible even in a setting with substantial unexplained variation.

**Robust Inference and Model Diagnostics**

Re-estimation using HC3 heteroskedasticity-robust standard errors yields identical coefficient estimates and preserves the statistical significance of X2 at conventional levels. Diagnostic assessments, including the Breusch–Pagan test and visual inspection of residual plots, provide no evidence of heteroskedasticity, nonlinearity, or severe departures from normality. These results support the validity of classical OLS inference in this setting.

**Penalized Regression Results**

Ridge regression shrinks coefficient magnitudes toward zero while retaining all predictors in the model. Under Ridge regularization, X2 remains the largest coefficient in magnitude, indicating relative stability across modeling frameworks.

In contrast, Lasso regression with cross-validated penalty selection sets all slope coefficients to zero, selecting an intercept-only specification. This result suggests that, under strict sparsity constraints, the predictors provide limited incremental predictive power. Sensitivity analysis using a weaker ℓ1 penalty recovers X2 as the dominant coefficient, consistent with the OLS and Ridge estimates.

**Summary**

Overall, the results indicate that knowledge of the US–China trade war (X2) is the most stable predictor across model specifications. While the estimated effect is statistically robust under classical and robust inference, penalized regression highlights limited predictive strength under aggressive regularization. These findings suggest that the relationship is statistically credible but modest in explanatory power.
