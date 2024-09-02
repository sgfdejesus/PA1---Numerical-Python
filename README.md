# PA2---Numerical-Python
"This repository contains Python code that solves programming problems titled: *Normalization* and *Divisible by 3*."

Below is a preview of the code, but there is also a Jupyter notebook uploaded in the files section.

## 1. Normalization Problem
``` python
import numpy as np

#Create a random 5x5 ndarray
X = np.random.rand(5, 5)

#Calculate the mean and standard deviation of the array
mean_X = X.mean()
std_X = X.std()

#Normalize the array using the formula Z = (X - mean) / std
X_normalized = (X - mean_X) / std_X

#Save the normalized array to a file
np.save('X_normalized.npy', X_normalized)

#Print the original and normalized arrays
print("Original array:\n", X)
print("\nNormalized array:\n", X_normalized)
```

## 2. Divisible by 3 Problem
``` python
import numpy as np

#Create an array with the first 100 positive integers
integers = np.arange(1, 101)

#Square each element to create the 10x10 array
A = integers ** 2
#Reshape to 10x10 ndarray
A = A.reshape(10, 10)

#Determine the elements divisible by 3
divisible_by_3 = A[A % 3 == 0]

#Save the result to a file
np.save('div_by_3.npy', divisible_by_3)

#Print the array and the elements divisible by 3
print("10x10 Array A:\n", A)
print("\nElements divisible by 3:\n", divisible_by_3)
```
