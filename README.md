# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required library and read the dataframe.

2.Write a function computeCost to generate the cost function.

3.Perform iterations og gradient steps with learning rate.

4.Plot the Cost function using Gradient Descent and generate the required graph
## Program:
```
/*
Program to implement the linear regression using gradient descent.
Developed by:    Naveen sairam b
RegisterNumber:  24009928
import numpy as np
import pandas as pd
from sklearn.preprocessing import StandardScaler
def linear_regression(x1,y,learning_rate=0.01,num_iters=1000):
    x=np.c_[np.ones(len(x1)),x1]
    theta=np.zeros(x.shape[1]).reshape(-1,1)
    for _ in range(num_iters):
        predictions=(x).dot(theta).reshape(-1,1)
        errors =(predictions-y).reshape(-1,1)
        theta-=learning_rate*(1/len(x1))*x.T.dot(errors)
    return theta
data=pd.read_csv('50_Startups.csv',header=None)
print(data.head())
x=(data.iloc[1:,:-2].values)
print(x)
x1=x.astype(float)
scaler=StandardScaler()
y=(data.iloc[1:,-1].values).reshape(-1,1)
print(y)
x1_scaled=scaler.fit_transform(x1)
y1_scaled=scaler.fit_transform(y)
print(x1_scaled)
print(y1_scaled)
theta=linear_regression(x1_scaled,y1_scaled)
new_data=np.array([165349.2,136897.8,471784.1]).reshape(-1,1)
new_scaled=scaler.fit_transform(new_data)
prediction=np.dot(np.append(1,new_scaled),theta)
prediction=prediction.reshape(-1,1)
pre=scaler.inverse_transform(prediction)
print(f"predicted value: {pre}")
*/
```

## Output:
## data
![image](https://github.com/user-attachments/assets/0d90d2fa-710a-4801-8011-9f023540ad86)

## value of x
![image](https://github.com/user-attachments/assets/a589dc83-b93e-4432-b3bb-430a387cd9de)

## value of x1_scaled
![image](https://github.com/user-attachments/assets/5b42660f-d3f4-4afa-9874-12a8672167ab)
## predicted value
![image](https://github.com/user-attachments/assets/c41a810e-ad22-4572-b486-c33b156da857)




## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
