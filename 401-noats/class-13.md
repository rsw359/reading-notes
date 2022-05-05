# Class-13

## ****Linear Regression in Python****

Regression searches for relationships among variables.

Generally, in regression analysis, you usually consider some phenomenon of interest and have a number of observations. Each observation has two or more features. Following the assumption that (at least) one of the features depends on the others, you try to establish a relation among them.

Regression is finding a **function that maps some features or variables to others**

The dependent features are called the **dependent variables**, **outputs**, or **responses**.

The independent features are called the **independent variables**, **inputs**, or **predictors**.

The purpose of regression is to answer whether and how some phenomenon influences another or **how several variables are related**

### **Simple Linear Regression**

Simple or single-variate linear regression is the simplest case of linear regression with a single independent variable, 𝐱 = 𝑥.

### **Python Packages for Linear Regression**

The package **NumPy** is a fundamental Python scientific package that allows many high-performance operations on single- and multi-dimensional arrays. It also offers many mathematical routines.

The package **scikit-learn**
 is a widely used Python library for machine learning, built on top of NumPy and some other packages. It provides the means for preprocessing data, reducing dimensionality, implementing regression, classification, clustering, and more.

There are five basic steps when you’re implementing linear regression:

1. Import the packages and classes you need.
2. Provide data to work with and eventually do appropriate transformations.
3. Create a regression model and fit it with existing data.
4. Check the results of model fitting to know whether the model is satisfactory.
5. Apply the model for predictions.

The Y variable in a  model is the variable that is being predicted.(response variable)

The x variable that is used to help predict the y.(explanatory variable)

It must be determined whether the relation between the two is strong enough to reach a conclusion about the response.
