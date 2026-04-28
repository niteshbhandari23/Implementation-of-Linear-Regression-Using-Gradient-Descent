# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Generate multivariate dataset and split into training and testing sets.
2. Scale features using StandardScaler for better SGD performance.
3. Train the SGDRegressor on training data.
4. Predict test values and evaluate using MSE and R² score.

## Program:
```
/*
Program to implement the linear regression using gradient descent.
Developed by: NITESH BHANDARI K
RegisterNumber:  212225240101


import numpy as np
import matplotlib.pyplot as plt

# Input data
x = np.array(eval(input("Enter population values: ")))
y = np.array(eval(input("Enter profit values: ")))

# Number of training examples
m = len(x)

# Initialize parameters
theta0 = 0
theta1 = 0

# Learning rate
alpha = 0.01

# Number of iterations
iterations = 1000

# Gradient Descent
for i in range(iterations):
    h = theta0 + theta1 * x
    
    temp0 = (1/m) * np.sum(h - y)
    temp1 = (1/m) * np.sum((h - y) * x)
    
    theta0 = theta0 - alpha * temp0
    theta1 = theta1 - alpha * temp1

# Predicted values
prediction = theta0 + theta1 * x

# Output
print("Intercept (theta0):", theta0)
print("Slope (theta1):", theta1)

# Graph
plt.scatter(x, y, color='blue', label="Training Data")
plt.plot(x, prediction, color='red', label="Regression Line")
plt.xlabel("Population")
plt.ylabel("Profit")
plt.title("Linear Regression using Gradient Descent")
plt.legend()
plt.show()
*/
```

## Output:
<img width="581" height="440" alt="image" src="https://github.com/user-attachments/assets/7054e74e-5225-445a-861b-3c83a14cd5cb" />


## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
