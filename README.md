# Implementation of Univariate Linear Regression
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
Program to develop to implement univariate Linear Regression to fit a straight line using least squares.

Developed by : GOKULRAJ.K
Register no : 25017714
```
```
import matplotlib.pyplot as plt
X= np.array([0,1,2,3,4,5,6,7,8,9])
Y= np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(X,Y)
plt.show()
X_Mean=np.mean(X)
Y_Mean=np.mean(Y)
num=0
den=0
for i in range(len(X)):
    num+=(X[i]-X_Mean)*(Y[i]-Y_Mean)
    den+=(X[i]-X_Mean)**2

m=num/den
b=Y_Mean-(m*X_Mean)
print(f"Slope : {m}\nIntercept : {b}")
Y_Pred=(m*X)+b
print(f"Predicted values are : \n{Y_Pred}")
plt.scatter(X,Y,color='Red')
plt.plot(X,Y_Pred,color='Blue')
plt.show()
```
## Output
<img width="1032" height="506" alt="Screenshot 2025-12-14 112449" src="https://github.com/user-attachments/assets/62789083-2a84-49e6-ab11-973530de1e8f" />
<img width="1033" height="447" alt="Screenshot 2025-12-14 112512" src="https://github.com/user-attachments/assets/c2324de7-4f9b-4ad4-9dad-c9a77b7b9f0b" />
<img width="1029" height="466" alt="Screenshot 2025-12-14 112535" src="https://github.com/user-attachments/assets/ce0f437e-7fd6-484f-aec2-6cb2c6fcb49e" />

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
