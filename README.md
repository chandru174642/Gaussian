# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import the numpy module and sys module to use the built-in functions for calculation 2. Get the size of the matrix from user and create empty matrix and vector
3. using for loop get elements for matrix and vector
4. Using another for loop to take each element in the matrix
5. solve row echelon form
6. perform back substitution
7. print the value in two decimal points 8. End the program

## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: CHANDRU.P
RegisterNumber:23007250 
'''
import numpy as np
n=int(input())
arr=np.zeros((n,n+1))
res=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        arr[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
           ratio=arr[j][i]/arr[i][i]
           for k in range(n+1):
               arr[j][k]=arr[j][k]-ratio*arr[i][k]
res[n-1]=arr[n-1][n]/arr[n-1][n-1]
for i in range(n-1,-1,-1):
    res[i]=arr[i][n]
    for j in range(i+1,n):
        res[i]=res[i]-arr[i][j]*res[j]
    res[i]=res[i]/arr[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,res[i]),end=" ")
        
        
*/
```

## Output:

![Screenshot 2023-12-28 090336](https://github.com/chandru174642/Gaussian/assets/139841798/3355dcd7-caf0-4db7-991a-81c7058a175d)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

