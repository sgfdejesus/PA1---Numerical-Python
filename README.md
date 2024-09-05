# PA2 - Numerical Python
"This repository contains Python code to solve two programming problems titled: **Normalization** and **Divisible by 3**. Each problem involves the use of NumPy for data manipulation and analysis."

Below is a preview of the code, but there is also a Jupyter notebook uploaded in the files section.

---

## 1. Normalization Problem
### Overview
This project normalizes a randomly generated 5x5 ndarray. The normalization is performed by: Centering the data by subtracting the mean and Scaling the data by dividing by the standard deviation. The normalized array is saved as `X_normalized.npy`.

### Code Implementation
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

### Input and Output Example
- **Input:** A randomly generated 5x5 ndarray.
- **Output:** A normalized 5x5 ndarray saved in X_normalized.npy.

<img width="464" alt="Screenshot 2024-09-05 at 6 28 53 PM" src="https://github.com/user-attachments/assets/b1b0b0c2-36ec-4dcf-9382-e17723427a0e">

---

## 2. Divisible by 3 Problem
### Overview
This project creates a 10x10 ndarray where each element is the square of the first 100 positive integers. The task is to determine which elements in this array are divisible by 3 and save the result to a file named `div_by_3.npy`.

### Code Implementation
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

### Input and Output Example
- **Input:** A 10x10 ndarray where each element is the square of the first 100 positive integers.
- **Output:** Elements in the ndarray that are divisible by 3, saved in div_by_3.npy.

<img width="517" alt="Screenshot 2024-09-05 at 6 36 15 PM" src="https://github.com/user-attachments/assets/74e4467c-a3a8-42bf-a282-8b30152af88f">

