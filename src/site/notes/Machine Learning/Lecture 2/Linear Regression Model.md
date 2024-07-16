---
{"dg-publish":true,"permalink":"/machine-learning/lecture-2/linear-regression-model/","dgPassFrontmatter":true}
---

## Terms
### Dependent Variable
- Dependent variables are measured or tested and depend on independent variables.
### Independent Variable
- Independent variables are manipulated and believed to have an effect on the dependent variable.
### Statistical Significant Effect
- Statistical significant variables are unlikely to have occurred by chance, likely to be real (not due to a random chance).
## Linear Regression
![linear regression.webp](/img/user/Machine%20Learning/Lecture%202/linear%20regression.webp)
- Statistical model that helps model the impact of a unit change in a variable(independent) on the values of another target variable (dependent), when their relationship is linear in nature.
- TYPES:
	- 1 Independent Variable $\rightarrow$ Simple Linear Regression.
	- 2 or more Independent Variables $\rightarrow$ Multiple Linear Regression.

### Simple Linear Regression

- The formula for simple linear regression is: $y = \beta_0 + \beta_1 x + \epsilon$ ,Where:
	- $y$ is the dependent variable (the outcome you are trying to predict).
	- $x$ is the independent variable (the predictor).
	- $\beta_0$ is the y-intercept of the regression line.
	- $\beta_1$ is the slope of the regression line.
	- $\epsilon$ is the error term (the difference between the observed and predicted values).
### Multiple Regression Formula

- The formula for multiple regression is: $y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \cdots + \beta_p x_p + \epsilon$ Where:
	- $y$ is the dependent variable (the outcome you are trying to predict).
	- $x_1, x_2, \ldots, x_p$ are the independent variables (the predictors).
	- $\beta_0$ is the y-intercept of the regression plane (or hyperplane).
	- $\beta_1, \beta_2, \ldots, \beta_p$ are the coefficients (slopes) for each predictor.
	- $\epsilon$ is the error term (the difference between the observed and predicted values).
## Linear Regression Estimation
### Ordinary Least Squares (OLS)

- Estimation technique used for estimating unknown parameters in a linear regression model to predict the response/dependent variable.
- OLS aims to find the best fitting regression line by minimizing the sum of squared errors.
- We estimate the error term as residuals and minimize the sum of squares of residuals.
- The OLS regression model for simple linear regression is given by:$y = \beta_0 + \beta_1 x + \epsilon$, where:
	- $y$ is the dependent variable (the outcome you are trying to predict).
	- $x$ is the independent variable (the predictor).
	- $\beta_0$ is the y-intercept of the regression line.
	- $\beta_1$ is the slope of the regression line.
	- $\epsilon$ is the error term (the difference between the observed and predicted values).
## Linear Regression Assumptions (5)

##### A1 - Linearity
- model is linear in parameters (aka) relationship between dependent variables and independent variables is linear.
- Check by plotting residuals to fitted values $\rightarrow$ if not linear $\rightarrow$ estimate will be biased and hence linearity assumption is violated.
- Use more flexible models ($Eg$: tree based models).
##### A2 - Random Sample 
- all observations in the sample are randomly selected.
- Check by plotting residuals then taking the mean of the residuals $\rightarrow$ if mean is not around 0 $\rightarrow$ OLS is biased and hence random sample assumption is violated.(Systematically over/under predicting the variable).
##### A3 - Exogeneity
- each independent variable is uncorrelated with the error terms.
	- (aka) independent variables are not affected by error terms in the model
	- (or) independent variables are assumed to be determined independent of errors in the model.
- It is a key assumption $\rightarrow$ allows to interpret estimated coefficient $\rightarrow$ represent true causal effect of independent variables on dependent variables. variables when satisfying this assumption $\rightarrow$ exogeneous
- else $\rightarrow$ endogenous.
- Endogeneity $\rightarrow$ Independent variables corelating with error terms.
- ***Causes*** -
	###### - Omitted Variable Bias
	- important vector of a dependent variable is not included in the model.
	###### - Reverse Causality 
	- dependent variable affects the independent variable.
##### A4 - Homoscedasticity/Homogeneity of Variance
variance of all error terms in constant.
Importance : to use statistical techniques and make inferences about parameters of the model. If errors not homoscedastic $\rightarrow$ results of techniques $\rightarrow$ misleading/invalid $\rightarrow$ heteroscedasticity.
Heteroscedasticity $\rightarrow$ Variance of all error terms is ***NOT*** constant.
	Coefficient (might be) $\rightarrow$ Accurate.
	But, Corresponding standard error, Student T test, P value, Confidence intervals $\rightarrow$ Not Accurate.

##### A5 - No Perfect MultiCollinearity
there are no exact linear relationships between the independent variables.