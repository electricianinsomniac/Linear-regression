# Linear-regression
 implement linear regression with one variable to predict profits for a restaurant franchise.
 
 ## Background 
 This repository is created to complete the assignment: C1_W2_Linear_Regression
 
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

# exercise
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
