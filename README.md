# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. import the required libraries.
2. Upload and read the dataset.
3. Check for any null values using the isnull() function
4. From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.
5.  Find the accuracy of the model and predict the required values by importing the required
module from sklearn.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Magesh V
RegisterNumber: 212222040092
import pandas as pd
data=pd.read_csv("/content/Employee.csv")

print('data.info:')
data.info()

print('data.isnull().sum():')
data.isnull().sum()

print('value_count: ')
data["left"].value_counts()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()

data["salary"]=le.fit_transform(data["salary"])
data.head()

*x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()**

y=data["left"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)

from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy

dt.predict([[0.5,0.8,9,260,6,0,1,2]])
*/
```

## Output:
Initial data set
![Screenshot 2023-10-12 092325](https://github.com/magesh534/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/135577936/811c0f72-054a-4099-ba6e-ef782eeb36e5)
Data Info
![Screenshot 2023-10-12 092854](https://github.com/magesh534/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/135577936/7e480048-75aa-46c0-96bd-4defba482e34)
Optimization of null values
![Screenshot 2023-10-12 092956](https://github.com/magesh534/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/135577936/d88449d3-eaa4-40ea-b695-92e358955e5e)
Assignment of X and Y values
![Screenshot 2023-10-12 093249](https://github.com/magesh534/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/135577936/775406df-949b-439d-8a27-0c8425a24b54)
Converting string literals to numerical values using label encoder
![Screenshot 2023-10-12 093304](https://github.com/magesh534/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/135577936/5d8fde41-30a8-49fd-953c-acca1b09318c)
Accuracy

![Screenshot 2023-10-12 093318](https://github.com/magesh534/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/135577936/bfe39807-23a7-4ffb-8243-04e8ab1c8833)

Prediction
![Screenshot 2023-10-12 093352](https://github.com/magesh534/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/135577936/779e97fd-c1ad-4747-8ab0-dcfb6d7107d7)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
