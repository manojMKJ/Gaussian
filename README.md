# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import the numpy module to use the built-in functions for calculation
2. give the prepared matrix and assign in np.array()
3. Using np.linalg.matrix_inv(),we can find the Gaussian Elimination of a matrix
4. End the program

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Manoj kumar G
RegisterNumber: 22005014
*/
import numpy as np
n=int(input())
arr=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
for j in range(n+1):
arr[i][j]=int(input())
for i in range(n):
for j in range(i+1,n):
ratio=arr[j][i]/arr[i][i]
for k in range(n+1):
arr[j][k]=arr[j][k]-ratio*arr[i][k]
x[n-1]=arr[n-1][n]/arr[n-1][n-1]
for i in range(n-2,-1,-1):
x[i]=arr[i][n]
for j in range(i+1,n):
x[i]=x[i]-arr[i][j]*x[j]
x[i]=x[i]/arr[i][i]
for i in range(n):
print("X%d = %0.2f" %(i,x[i]),end=" ")
```

## Output:
![image](https://github.com/manojMKJ/Gaussian/assets/120717614/21a68144-28de-452f-9745-d43eda44f038)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.
