# Regularized-Regression-In-LM

This project focuses on eliminating insignificant predictors from a linear regression model using two approaches: Lasso regression and Ordinary regression. The dataset used is stored in the file "test_sample.csv", which consists of 490 columns labeled Y, X0, X1, ..., X489.

In the Lasso regression approach, the LassoCV class from the sklearn module is utilized with default parameters. By finding the optimal value of α (αmin) through LassoCV, the model is trained. The regressors that are eliminated by Lasso regression, among X0, X1, ..., X489, are identified by their corresponding indices.

For the Ordinary regression approach, two-sided p-values (Pr(>|t|)) are employed to determine which coefficients of the linear model should be eliminated. Coefficients with p-values greater than 0.1 are considered insignificant. The indices of the eliminated regressors among X0, X1, ..., X489 are obtained.

The arrays of indices of eliminated regressors is finally returned.
