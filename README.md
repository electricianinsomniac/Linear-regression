# Linear-regression
 implement linear regression with one variable to predict profits for a restaurant franchise.
 
 ## Background 
 This repository is created to complete the assignment: [C1_W2_Linear_Regression](C1_W2_Linear_Regression.ipynb)
 
 ## Introduction
 Practice Lab: Linear Regression

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
