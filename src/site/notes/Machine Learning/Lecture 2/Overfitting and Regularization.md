---
{"dg-publish":true,"permalink":"/machine-learning/lecture-2/overfitting-and-regularization/","dgPassFrontmatter":true}
---

---
## Overfitting

![Pasted image 20240715161729.png](/img/user/Machine%20Learning/Lecture%202/Pasted%20image%2020240715161729.png)
- Overfitting is when the model performs well in training but poorly on test data, leading to low training error and high test error.
	- High variance
	- Low Bias
#### How to Fix:

1. **Adding More Data**:
    - Retrain the algorithm on a larger, more diverse dataset to improve model performance.
    - Consider data augmentation to artificially increase the size of the dataset, introducing new variations to improve generalization.
2. **Regularization**:
    - Introduce a complexity penalty to the model to prioritize simpler solutions and reduce overfitting.
    - Various regularization techniques exist to prevent overfitting by restricting the model's complexity.
3. **Removing Features**:
    - Simplify the data by removing irrelevant or complex features to reduce overfitting.
---
## Regularization
### Ridge Regression / L2 Regularization

- Shrinkage technique that aims to solve Overfitting by shrinking some of the model's coefficients towards 0.
	- $beta_{\text{ridge}} = (X^T X + \lambda I)^{-1} X^T y$
	- Where: 
		- $X$ is the matrix of predictor variables. 
		- $y$ is the vector of observed values. 
		- $lambda$ is the regularization parameter.
		- $I$ is the identity matrix.
		- $beta_{\text{ridge}}$ represents the ridge regression coefficients.
- Pros:
	- Solves Overfitting
	- Lower model variance
	- Computationally cheap
- Cons
	- low interpretability

### Lasso Regression / L1 Regularization

- Shrinkage technique that aims to solve Overfitting by shrinking some of the model's coefficients towards 0 and setting some to 0 itself.
	- Lasso Regression Formula
	- The objective function for Lasso regression is given by
	- $\hat{\beta} = \arg\min_{\beta} \left\{ \frac{1}{2n} \sum_{i=1}^n \left( y_i - \sum_{j=1}^p x_{ij} \beta_j \right)^2 + \lambda \sum_{j=1}^p |\beta_j| \right\}$

- **Objective Function:**

	- The Lasso regression aims to minimize the following objective function:
	- $J(\beta) = \frac{1}{2n} \sum_{i=1}^n \left( y_i - \sum_{j=1}^p x_{ij} \beta_j \right)^2 + \lambda \sum_{j=1}^p |\beta_j|$

- **Residual Sum of Squares:**

	- The first term is the residual sum of squares, which measures the difference between the observed and predicted values
	- $\frac{1}{2n} \sum_{i=1}^n \left( y_i - \sum_{j=1}^p x_{ij} \beta_j \right)^2$

- **Regularization Term:**

	- The second term is the L1 regularization term, which is the sum of the absolute values of the coefficients
	- $\lambda \sum_{j=1}^p |\beta_j|$
   
- **Combine Terms:**

	- The Lasso regression combines these two terms to form the objective function that needs to be minimized
	- $J(\beta) = \frac{1}{2n} \sum_{i=1}^n \left( y_i - \sum_{j=1}^p x_{ij} \beta_j \right)^2 + \lambda \sum_{j=1}^p |\beta_j|$

- **Optimization Problem:**

	- The goal is to find the coefficients \(\beta\) that minimize the objective function \(J(\beta)\):
	- $\hat{\beta} = \arg\min_{\beta} J(\beta)$
- Pros
	- Solves Overfitting
	- Easy to understand
	- High interpretability
	- Feature selection
- Cons
	- Higher variance than Ridge.
---
## View Next Topics

### [[Machine Learning/Lecture 2/Linear Regression Model\|Linear Regression Model]]