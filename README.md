# The Bias-Variance Tradeoff: Choosing How Flexible a Model Should Be

## Objective

I examined how model complexity affects bias, variance, and prediction error, and used cross-validation to select a polynomial degree.

## Methodology

- I simulated nonlinear data using a known true curve.
- I fitted polynomial models with different degrees.
- I decomposed prediction error into bias squared and variance using 200 new samples at each of six degrees.
- I compared training error with error on 2,000 new observations for polynomial degrees 1 through 15.
- I used 5-fold cross-validation to select a polynomial degree.
- I used nested cross-validation to estimate the prediction error of the full model-selection process.
- I wrote `kfold_mse()` to calculate cross-validation error for different polynomial degrees and numbers of folds.
- I compared degrees 4 and 5 using 10-fold cross-validation.
- I examined prediction error after fitting models with more coefficients than training observations.

## Key Findings

Variance was **0.0180** for degree 5 and increased to **0.0994** for degree 15. The held-out prediction error was lowest at degree **5**, showing that additional complexity eventually hurt performance on
