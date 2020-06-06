# Exploring linear model

1. Check if there's atleast one non-zero coefficient in the model, using F-statistic.
2. How strong is the relationship?
	- Use Residual Standard Error (RSE) to find out error rate
	- Use R-squared to find out how much variability in Y can be explained by the model
3. Which feature contributes to Y?
	- Examine p-value associated with each predictor's t-statistic
4. How much is the effect of each predictor on Y
	- Standard error of predictor can be used to construct 95% confidence intervals on the Coefficient
5. How accurately can we predict Y?
	- We use confidence interval or prediction interval.
	- Prediction interval accounts for uncertainity associated with irreducible error, so it is always wider than confidence interval.
6. Is the relationship linear?
	- This effect can be observed in residual plot
	
# Potential Problems

Common problems while fitting linear regression models are discussed below:
1. Non-linearity of the data
	- Residual plots are helpful in identifying non linearity.
	- In case of non-linearity, use non-linear transformations of the predictors, such as log X, sqrt(X), and X^2 , in the regression model.
2. Correlated error
	- can narrow confidence intervals
	- can occur when correlated observations are available in the dataset (usually in time series)
3. Non-constant variances in the errors, or heteroscedasticity
	- Variance in error terms may increase with value of response (**funnel shape** of residual plot)
	- Transforming Y *(log or sqrt)* could reduce heteroscedasticity
4. Outliers
	- can arise due to incorrect recording or observation and a variety of reasons.
	- addressing outliers can improve RSE and R-squared.
5. High leverage points
	- removing the high leverage observation has a much more substantial impact on the least squares line than removing outliers.
	- we can compute *leverage statistic* to quantify an observation's leverage.
6. Collinearity
	- *Collinearity* refers to the situation in which two or more predictor variables are closely related to one another.
	- Collinearity would increase Standard error of predictors
	- *Variance Inflation Factor* (VIF) is the ration of variance of predictor coefficient, if fit on its own.
	- Smallest possible VIF is 1 (absence of collinearity)
	- As a rule of thumb, a VIF value that exceeds 5 or 10 indicates problematic amount of collinearity.
