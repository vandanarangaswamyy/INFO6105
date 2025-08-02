**Goldman Sachs - Stock Return Prediction Model**

This project implements and evaluates various statistical models to predict stock returns using a combination of financial and technical analysis features. The focus is on understanding the contribution of different predictors and improving the accuracy of return predictions.Project Overview
The project explores four key models:

1. CAPM Augmented Model: Extends the traditional Capital Asset Pricing Model by including additional macroeconomic variables like interest rate spreads (T10Y2Y) and currency exchange rates (DEXUSEU).
Focuses on the significance of the market risk premium (Mkt-RF) in predicting returns.

2. Fama-French Technical Model: Combines the Fama-French three-factor model with technical indicators such as the Relative Strength Index (RSI_15) and On-Balance Volume (OBV).
Aims to capture both market effects and trading signals.

3. Augmented AR(1) Model: Incorporates an autoregressive component to account for temporal dependencies in returns. Includes features like BBP_10_2.0 and BAMLH0A0HYM2 to reflect bond market conditions.

4. Kalman Filter Model: Utilizes financial indicators like Mkt-RF, RSI_15, and SMA_10. Although named a Kalman Filter model, it currently uses OLS regression for simplicity.

_Methodology_

1. Data Preparation: Loads and cleans feature data from GS_FeatureMart_New.csv.
Calculates log returns for Goldman Sachs' stock and aligns them with the feature set.
Scales numeric features and handles missing values to ensure robust model fitting.


2. Model Fitting and Evaluation: Uses Ordinary Least Squares (OLS) regression to fit models.
Evaluates model performance using R-squared, adjusted R-squared, and correlation coefficients.
Conducts a hard-threshold analysis to identify significant predictors based on p-values.


_Results Summary_

The Fama-French Technical Model shows the highest explanatory power with an R-squared of 0.3280 and a correlation of 0.5727.
The CAPM Augmented Model and Kalman Filter Model provide moderate performance, effectively using market risk factors.
The Augmented AR(1) Model highlights the importance of autoregressive terms but has the lowest overall predictive power.
