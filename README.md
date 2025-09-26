# Modeling Adjacent Airport Market Share

This project analyzes how passenger market share shifts between competing adjacent airports that serve overlapping markets. The study focuses on understanding whether larger airports always dominate, or if smaller airports can capture a meaningful share when factors such as pricing, accessibility, and service frequency come into play.

## Project Summary

The dataset used in this project includes more than 44,000 airport-pair records covering the period from January 2022 to December 2023. Each record compares two airports within the same origin or destination cluster. Key engineered features include:

* Fare ratio (larger airport vs. smaller airport)
* Departure count difference
* Capacity difference
* Origin and destination size differences
* Distance between competing airports
* Seasonal (month) and regional indicators
* The dependent variable is the market share percentage of the larger airport.

## Methodology

To capture both interpretability and predictive performance, the following models were applied:
* Ordinary Least Squares (OLS) Regression
* Ridge Regression
* Lasso Regression
* Random Forest Regressor
* XGBoost Regressor

Models were trained using a 70/30 train-test split and evaluated using:
* R² (variance explained)
* RMSE (average prediction error)

## Results

* Random Forest consistently achieved the highest performance, with R² values above 0.84 in several scenarios.
* XGBoost performed especially well in cases where the larger airport lost share to the smaller one.
* OLS, Ridge, and Lasso provided valuable interpretability, showing the marginal effects of pricing, frequency, and capacity.
* Key predictors across models:
  * Fare ratio (competitive pricing strongly influences passenger choice)
  * Departure frequency (higher flight frequency attracts passengers)
  * Seat capacity difference (greater capacity often leads to higher share)
  * Distance (proximity plays a role in accessibility)
  * International status (larger airports dominate in international markets)

## Key Takeaways

* Larger airports do not always hold the majority share.
* Smaller airports can gain advantage through pricing and convenience.
* These results provide insights for airlines, airport authorities, and policymakers in route planning, pricing strategy, and infrastructure decisions.
