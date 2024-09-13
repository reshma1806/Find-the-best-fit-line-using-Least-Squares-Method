# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

Step 1: Start the program.

Step 2: Get the independent variable X and dependent variable Y.

Step 3: Calculate the mean of the X -values and the mean of the Y -values.4

Step 4: Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">

Step 5: Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">

Step 6: Use the slope m and the y -intercept to form the equation of the line.

Step 7: Obtain the straight line equation Y=mX+b and plot the scatterplot.

Step 8: Stop the program.


## Program:

Program to implement univariate Linear Regression to fit a straight line using least squares.

Developed by: RESHMA S M

RegisterNumber: 212223080044 

```
import numpy as np
import matplotlib.pyplot as plt

# Preprocessing Input data
X=np.array(eval(input()))
Y=np.array(eval(input()))

# Mean
X_mean=np.mean(X)
Y_mean=np.mean(Y)
num=0
denom=0

# to find sum of(xi-x') & (yi-y') & (xi-x')^2
for i in range(len(X)):
    num+=(X[i]-X_mean)(Y[i]-Y_mean)
    denom+=(X[i]-X_mean)**2

# calculate slope
m=num/denom

# calculate intercept
b=Y_mean-m*X_mean
print(m,b)

# Line equation
y_predicted=m*X+b
print(y_predicted)

# to plot graph
plt.scatter(X,Y)
plt.plot(X,y_predicted,color='red')
plt.show()
```

## Output:

14,24,53,76

23,61,43,25

-0.15976517454659817 44.67019603732047

[42.43348359 40.83583185 36.20264179 32.52804277]


![Screenshot 2024-08-22 200918](https://github.com/user-attachments/assets/5d1f3da4-364d-4ce4-81e9-c603b05839f2)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
