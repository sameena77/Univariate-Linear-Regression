# Exp:9 Implementation of Univariate Linear Regression
# Date:11.05.2024
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
Developed by: Sameena J
RegisterNumber: 2305002019

import numpy as np
import matplotlib.pyplot as plt

X = np.array(eval(input()))
Y = np.array(eval(input()))

Xmean = np.mean(X)
Ymean = np.mean(Y)
num,den = 0,0
for i in range(len(X)):
    num += (X[i]-Xmean)*(Y[i]-Ymean)
    den += (X[i]-Xmean)**2
m = num/den
c = Ymean-m*Xmean
    
print (m, c)

Y_pred = m*X + c
print (Y_pred)

plt.scatter(X,Y)
plt.plot(X,Y_pred,color="red")
plt.show()

```
## Output :
![qr](https://github.com/sameena77/Univariate-Linear-Regression/assets/155620541/e0ff3281-06c8-47e2-9375-fc924cdac0d0)
![li re2](https://github.com/sameena77/Univariate-Linear-Regression/assets/155620541/0a8d3807-e840-44a6-ad7a-846fc0c1f0ae)



## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
