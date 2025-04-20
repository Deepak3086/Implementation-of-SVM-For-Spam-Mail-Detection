# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: DEEPAK JG
RegisterNumber:  212224220019
*/

import pandas as pd
data=pd.read_csv("spam.csv", encoding='Windows-1252')
data

data.shape

x=data['v2'].values
y=data['v1'].values
x.shape

y.shape

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2, random_state=0)
x_train

x_train.shape

from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn.metrics import accuracy_score,confusion_matrix,classification_report
acc=accuracy_score(y_test,y_pred)
acc

con=confusion_matrix(y_test,y_pred)
print(con)

cl=classification_report(y_test,y_pred)
print(cl)
```

## Output:
data

![image](https://github.com/user-attachments/assets/a17e3f26-bb89-41c7-9217-e78bcb369aa0)


data.shape()

![image](https://github.com/user-attachments/assets/ebca98b5-28b8-4ce5-8761-0780d7899e0a)

x.shape()

![image](https://github.com/user-attachments/assets/e83a53d1-dd65-4d77-b1d6-9ccce2df42a7)


y.shape()

![image](https://github.com/user-attachments/assets/fd4cf7ac-ff49-487b-b07e-8950887b3797)


x_train

![image](https://github.com/user-attachments/assets/5d7841d4-32a3-4f24-b2c3-a0e653581f63)


x_train.shape()

![image](https://github.com/user-attachments/assets/16237e69-5650-4133-885e-a5bdf38b2579)



y_pred

![image](https://github.com/user-attachments/assets/be79e5e8-547b-47a0-8a0f-a72d8cefded7)


acc (accuracy)

![image](https://github.com/user-attachments/assets/d7b739f6-4da5-4859-9ee4-3118a783d756)


con (confusion matrix)

![image](https://github.com/user-attachments/assets/0cb83cba-4a4f-4f86-99a9-186132c1c3a7)


cl (classification report)

![image](https://github.com/user-attachments/assets/bdf0a845-ff15-4e16-9557-29d652386dd8)



## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
