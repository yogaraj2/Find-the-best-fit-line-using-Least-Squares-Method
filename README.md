# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
4. Compute the y -intercept of the line by using the formula:
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: YOGARAJ S
RegisterNumber:  212223040248
*/
```
import numpy as np
import matplotlib.pyplot as plt

X = np.array(eval(input()))
Y = np.array(eval(input()))


X_mean =np.mean(X)
Y_mean=np.mean(Y)
num=0  #for slope
denom=0  #for slope


for i in range(len(X)):
    num+=(X[i] -X_mean)*(Y[i]-Y_mean)
    denom+= (X[i]-X_mean)**2


m=num/denom


b=Y_mean-m*X_mean

print(m,b)

y_predicted=m*X+b
print(y_predicted)


plt.scatter(X,Y)

plt.plot(X,y_predicted,color='green')

plt.show()

## Output:
![Screenshot 2024-02-23 110635](https://github.com/yogaraj2/Find-the-best-fit-line-using-Least-Squares-Method/assets/153482637/26000813-4aa6-4c50-a7f3-42c516eb5226)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
