# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Load independent variables (X) and the dependent variable (y).
<br>

### Step2

Add intercept term: Add a column of ones to X for the intercept.
<br>
### Step3

Use the formula β = (X^T X)^(-1) X^T y to compute the regression coefficients.
<br>
### Step4

Compute predictions using y_pred = X * β.
<br>
### Step5

Calculate performance metrics like Mean Squared Error (MSE) or R-squared.
<br>
## Program:
```
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("C:\\Users\\Keerthivasan\\Downloads\\carsemmision.csv")
df
```
```
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:',regr.intercept_)
predictedCO2 = regr.predict([[3300, 1300]])
print('Predicted CO2 for the corresponding weight and volume',predictedCO2)
```
## Output:
![Screenshot 2024-12-11 174100](https://github.com/user-attachments/assets/8a04eca7-f0b4-4ad4-a4c2-39b7ebd88fce)

### Insert your output
![Screenshot 2024-12-11 174146](https://github.com/user-attachments/assets/910f0e59-7308-45a4-82ef-12524c2ba249)

<br>

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
