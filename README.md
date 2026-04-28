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
import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("Startup.csv")
X = data['R&D Spend'].values
y = data['Profit'].values
X = (X - X.mean()) / X.std()
m = 0
b = 0
learning_rate = 0.01
epochs = 1000
n = len(X)
for i in range(epochs):
    y_pred = m * X + b
    dm = (-2/n) * np.sum(X * (y - y_pred))
    db = (-2/n) * np.sum(y - y_pred)
    m = m - learning_rate * dm
    b = b - learning_rate * db
print("Slope (m):", m)
print("Intercept (b):", b)
y_pred = m * X + b
plt.scatter(X, y)
plt.plot(X, y_pred)
plt.xlabel("R&D Spend (Normalized)")
plt.ylabel("Profit")
plt.title("Gradient Descent on 50_Startups Dataset")
plt.show()
*/
```

## Output:
<img width="993" height="725" alt="expr3ml" src="https://github.com/user-attachments/assets/e0e24c82-0965-41ec-a0ed-7d2466e079dc" />


## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
