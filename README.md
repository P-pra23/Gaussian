# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
Step 1: import numpy as np 
Step2: import sys 
Step 3: get input from the user 
Step 4: calculate the X0, X1 and X2 values by Gaussian elimination. 
Step 5: print the values Step 6: End the program

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Prathikshaa 
RegisterNumber: 212224100043
*/

import numpy as np
import sys

n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)

for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
        
        
for i in range(n):
    if a[i][i]==0.0:
        sys.exit('Divide by zero detected!');
        
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        
        for k in range(n+1):
            a[j][k]=a[j][k]- ratio*a[i][k]
         
        

x[n-1]=a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]

    x[i]=x[i]/a[i][i]

for i in range(n):
    print('X%d = %0.2f' %(i,x[i]),end = ' ')
```

## Output:
<img width="1156" height="973" alt="image" src="https://github.com/user-attachments/assets/dcb63e4f-77aa-4bf1-bec1-bff9d4e3b225" />

<img width="654" height="587" alt="image" src="https://github.com/user-attachments/assets/a3c8d9c3-06c2-4fff-8930-f47d3ceb6b64" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

