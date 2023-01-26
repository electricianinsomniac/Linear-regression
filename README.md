# Linear-regression
 implement linear regression with one variable to predict profits for a restaurant franchise.
 
 ## Background 
 
 Linear regression is a statistical method used to model the relationship between a dependent variable (also known as the outcome or response variable) and one or more independent variables (also known as predictors or explanatory variables). The goal of linear regression is to find the best-fitting line through a set of data points. The line is represented by an equation of the form Y = a + bX, where Y is the dependent variable, X is the independent variable, a is the y-intercept (the point where the line crosses the y-axis), and b is the slope of the line (the change in Y for a unit change in X). Linear regression can be used for both simple linear regression (one independent variable) and multiple linear regression (more than one independent variable).
 
  ## Introduction
 Practice Lab: Linear Regression
 
  This repository is created to complete the assignment: [C1_W2_Linear_Regression](C1_W2_Linear_Regression.ipynb)
 
 ![image](https://user-images.githubusercontent.com/110273737/212011832-98010378-675c-4105-a53e-28098421d925.png)
 
### How Linear Regression Work 

Linear regression works by finding the line that best fits the data points. The line is represented by the equation Y = a + bX, where Y is the dependent variable, X is the independent variable, a is the y-intercept, and b is the slope of the line.

The slope of the line represents the relationship between the independent variable and the dependent variable. If the slope is positive, it means that as the independent variable increases, the dependent variable also increases. If the slope is negative, it means that as the independent variable increases, the dependent variable decreases.

The y-intercept represents the point at which the line crosses the y-axis. It represents the value of the dependent variable when the independent variable is zero.

The objective of linear regression is to minimize the sum of the squared differences between the predicted values of the dependent variable (obtained from the equation) and the actual values of the dependent variable. This process is called "Ordinary Least Squares" (OLS) method, it finds the line that minimizes the sum of the squared differences between the predicted values and the actual values.

Once the line is determined, it can be used to make predictions about the dependent variable for new values of the independent variable. Linear regression assumes that the relationship between the independent variable and the dependent variable is linear, and that the residuals (the differences between the predicted values and the actual values) are normally distributed and have constant variance.

# Packages
First, let's run the cell below to import all the packages that you will need during this assignment.

- numpy is the fundamental package for working with matrices in Python.
- matplotlib is a famous library to plot graphs in Python.
- utils.py contains helper functions for this assignment. You do not need to modify code in this file.

```
import numpy as np
import matplotlib.pyplot as plt
from utils import *
import copy
import math
%matplotlib inline
```

# Problem Statement
Suppose you are the CEO of a restaurant franchise and are considering different cities for opening a new outlet.
- You would like to expand your business to cities that may give your restaurant higher profits.
- The chain already has restaurants in various cities and you have data for profits and populations from the cities.
- You also have data on cities that are candidates for a new restaurant.
- For these cities, you have the city population.
 
Can you use the data to help you identify which cities may potentially give your business higher profits?

# exercise1
```
### START CODE HERE ###  
    # Variable to keep track of sum of cost from each example
    cost_sum = 0

    # Loop over training examples
    for i in range(m):
        # Your code here to get the prediction f_wb for the ith example
        f_wb = 
        # Your code here to get the cost associated with the ith example
        cost = 

        # Add to sum of cost for each example
        cost_sum = cost_sum + cost 

    # Get the total cost as the sum divided by (2*m)
    total_cost = (1 / (2 * m)) * cost_sum
    ### END CODE HERE ### 
 ```
    
    - There is the full answer section for exercise1 
    
 ```
    ### START CODE HERE ### 
    for i in range(m):
        f_wb_i=np.dot(x[i],w)+b
        total_cost=total_cost+(f_wb_i-y[i])**2
    total_cost= total_cost /(2*m)  
    ### END CODE HERE ### 
```
# exercise2
```
### START CODE HERE ### 
    # Loop over examples
    for i in range(m):  
        # Your code here to get prediction f_wb for the ith example
        f_wb = 

        # Your code here to get the gradient for w from the ith example 
        dj_dw_i = 

        # Your code here to get the gradient for b from the ith example 
        dj_db_i = 

        # Update dj_db : In Python, a += 1  is the same as a = a + 1
        dj_db += dj_db_i

        # Update dj_dw
        dj_dw += dj_dw_i

    # Divide both dj_dw and dj_db by m
    dj_dw = dj_dw / m
    dj_db = dj_db / m
    ### END CODE HERE ### 
```

    - Here is the full answer section for exercise2
    
    
```
    ### START CODE HERE ###
    for i in range(m): 
        f_wb = w * x[i] + b
        dj_dw_i = (f_wb - y[i]) * x[i]
        dj_db_i = f_wb - y[i]
        dj_db += dj_db_i
        dj_dw += dj_dw_i
    dj_dw = dj_dw / m
    dj_db = dj_db / m
    ### END CODE HERE ### 
    
````
