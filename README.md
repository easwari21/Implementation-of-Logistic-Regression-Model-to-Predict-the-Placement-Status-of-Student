# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required packages.
2. Print the present data and placement data and salary data.
3. Using logistic regression find the predicted values of accuracy      confusion matrices.
4. Display the results.

## Program:
```
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: Easwari M
RegisterNumber: 212223240033
```
```
import pandas as pd
data=pd.read_csv('Placement_Data.csv')
data.head()
data1=data.copy()
data1= data1.drop(["sl_no","salary"],axis = 1)
data1.head()
data1.isnull().sum
data1.duplicated().sum()
x=data1.iloc[:,:-1]
x
y=data1["status"]
y
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size = 0.2,random_state = 0)
from sklearn.linear_model import LogisticRegression
lr = LogisticRegression(solver = "liblinear")
lr.fit(x_train,y_train)
y_pred = lr.predict(x_test)
y_pred
from sklearn.metrics import accuracy_score
accuracy = accuracy_score(y_test,y_pred)
accuracy
from sklearn.metrics import confusion_matrix
confusion = (y_test,y_pred)
confusion
from sklearn.metrics import classification_report
classification_report1 = classification_report(y_test,y_pred)
print(classification_report1)
lr.predict([[1,80,1,90,1,1,90,1,0,85,1,85]])
```

## Output:

### Placement Data:
![the Logistic Regression Model to Predict the Placement Status of Student](dataset.jpg)

### Checking the null() function:

![the Logistic Regression Model to Predict the Placement Status of Student](null.jpg)

### Data Duplicate:

![the Logistic Regression Model to Predict the Placement Status of Student](duplicate.jpg)

### Print Data:

![the Logistic Regression Model to Predict the Placement Status of Student](numerical.jpg)

### Y_prediction array:

![the Logistic Regression Model to Predict the Placement Status of Student](y.jpg)

### Accuracy value:

![the Logistic Regression Model to Predict the Placement Status of Student](accuracy.jpg)

### Confusion array:

![the Logistic Regression Model to Predict the Placement Status of Student](confusion.jpg)

### Classification Report:

![the Logistic Regression Model to Predict the Placement Status of Student](classification.jpg)

### Prediction of LR

![the Logistic Regression Model to Predict the Placement Status of Student](lr.jpg)

## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
