---
{"dg-publish":true,"permalink":"/machine-learning/lecture-1/regression-and-classification/","dgPassFrontmatter":true}
---

#### **Regression:**

1. **Definition:** Regression is a type of supervised learning algorithm used to predict continuous numerical values. It establishes a relationship between independent variables(x) and dependent variables(y) in the form of a mathematical model or function.
    
2. **Example:** Predicting house prices based on features like square feet, number of bedrooms, and location.
    
3. **Mathematical Representation:** The basic form of a linear regression model with one independent variable is given by:
    
    - **Simple Linear Regression:** $y = mx + c$
    - **Multiple Linear Regression:** $y = b0 + b1x1 + b2x2 + ... + bnxn$

4. **Objective:** The goal of regression is to minimize the error or the difference between the predicted value and the actual value, often measured using metrics like Mean Squared Error (MSE) or Root Mean Squared Error (RMSE).

##### Formulae:

1. **Residual Sum of Squares (RSS):**
    - RSS measures the difference between the predicted values and the actual values.
    - Mathematical Formula: 
	$RSS = \sum_{i=1}^{n} (y_i - \hat{y}_i)^2$

2. **Mean Squared Error (MSE):**
    
    - MSE calculates the average squared difference between the actual and predicted values.
    - Mathematical Formula: 
    $MSE = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2$

3. **Root Mean Squared Error (RMSE):**
    
    - RMSE is the square root of the MSE and provides the error in the same units as the response variable.
    - Mathematical Formula: 
    $RMSE = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2}$

4. **Mean Absolute Error (MAE):**
    
    - MAE measures the average absolute differences between actual and predicted values.
    - Mathematical Formula: 
    $MAE = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i|$

In these formulas:

- $y_i$ - represents the actual value.
- $\hat{y}_i$ - represents the predicted value.
- $n$ - is the number of samples.

#### **Classification:**

1. **Definition:** Classification is a type of supervised learning algorithm used to categorize data into discrete classes or categories based on past observations. It predicts the class label for the given input data.
    
2. **Example:** Email spam classification, where emails are classified as spam or non-spam.
    
3. **Mathematical Representation:** Classification problems can be solved using various algorithms such as logistic regression, support vector machines, decision trees, or neural networks. The basic logistic regression model can be represented as:
    
    - **Logistic Regression:** 
		     $h(x) = \frac{1}{1 + e^{-(b0 + b1x1 + b2x2 + ... + bnxn)}}$

4. **Objective:** In classification, the algorithm aims to minimize misclassification by adjusting the decision boundary separating different classes. Common evaluation metrics for classification include accuracy, precision, recall, F1 score, ROC curve, and AUC.
##### Formulae:

1. **Accuracy:**
    
    - Accuracy measures the proportion of correct predictions out of the total predictions made.
    - Mathematical Formula: 
    $Accuracy = \frac{TP + TN}{TP + TN + FP + FN}$
    
2. **Precision:**
    
    - Precision quantifies the accuracy of the positive predictions made.
    - Mathematical Formula: 
    $Precision = \frac{TP}{TP + FP}$
    
3. **Recall (Sensitivity):**
    
    - Recall measures the proportion of actual positives that were correctly identified.
    - Mathematical Formula:
    $Recall = \frac{TP}{TP + FN}$
    
4. **F1 Score:**
    
    - F1 score is the harmonic mean of precision and recall, providing a balance between the two metrics.
    - Mathematical Formula:
    $F1 = 2 \times \frac{Precision \times Recall}{Precision + Recall}$

In these formulas:
- $TP$ - is the number of true positives.
- $TN$ - is the number of true negatives.
- $FP$ - is the number of false positives.
- $FN$ - is the number of false negatives.
#### **Differentiation between Regression and Classification:**

1. **Output Type:** Regression predicts continuous values, while classification predicts discrete class labels.
2. **Evaluation:** Regression is evaluated using metrics like RMSE, MAE, while classification typically uses accuracy, precision, recall, etc.
3. **Models:** Regression can use models like linear regression, polynomial regression, and neural networks. Classification can use models like logistic regression, decision trees, and SVMs.

## View Next Topics:

### [[Machine Learning/Lecture 1/Clustering\|Clustering]]:

### [[Machine Learning/Lecture 1/Training the Model\|Training the Model]]: