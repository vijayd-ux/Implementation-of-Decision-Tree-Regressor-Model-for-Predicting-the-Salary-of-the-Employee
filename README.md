# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Load the Dataset
2. Split the Data
3. Train the model
4. Predict and Evaluate

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by:VIJAY D
RegisterNumber:  212225230300

import pandas as pd
import numpy as np
from sklearn.tree import DecisionTreeRegressor, plot_tree
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score
import matplotlib.pyplot as plt
df = pd.read_csv("Salary.csv")
print("Dataset Preview:")
print(df.head())







X = df[["Level"]]   
y = df["Salary"]     
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.3, random_state=42
)
model = DecisionTreeRegressor(
    criterion="squared_error",
    max_depth=3,
    random_state=42
)






model.fit(X_train, y_train)
y_pred = model.predict(X_test)
mse = mean_squared_error(y_test, y_pred)
rmse = np.sqrt(mse)
print("MAE  :", mean_absolute_error(y_test, y_pred))
print("MSE  :", mse)
print("RMSE :", rmse)
print("R2   :", r2_score(y_test, y_pred))
plt.figure(figsize=(16, 10))
plot_tree(
    model,
    feature_names=["Level"],
    filled=True
)







plt.title("Decision Tree Regressor for Employee Salary Prediction")
plt.show()
new_exp = [[5]]
predicted_salary = model.predict(new_exp)
print("\nPredicted Salary for 5 years experience:", predicted_salary[0])
*/
```

## Output:
<img width="359" height="267" alt="image" src="https://github.com/user-attachments/assets/1064f9bd-ecbd-4ea5-9918-eeb34aae3b91" />
<img width="1135" height="730" alt="image" src="https://github.com/user-attachments/assets/a9c87280-7c0a-4e01-93f0-4077e9caa4d3" />



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
