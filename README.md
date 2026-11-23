# Experiment 1: Exploring NumPy and Pandas

## Aim

To understand the use of NumPy and Pandas for performing basic data
manipulation and analysis in Python.

## Algorithm

1.  Import the NumPy library for matrix and numerical operations.
2.  Define a two-dimensional square matrix `A` and a vector `b`.
3.  Compute the transpose of matrix `A` to interchange rows and columns.
4.  Calculate the inverse of matrix `A` using `np.linalg.inv(A)` (ensure
    `A` is non-singular).
5.  Solve the linear equation `A × x = b` using `np.linalg.solve(A, b)`.
6.  Perform eigen decomposition to find eigenvalues and eigenvectors
    using `np.linalg.eig(A)`.
7.  Display the results for the matrix, transpose, inverse, solution
    vector, and eigenvalues.
8.  End the program.

## Formulas / Theory

-   **Transpose:** `Aᵀ` --- interchange rows and columns.
-   **Inverse:** `A⁻¹ = adj(A) / |A|`, provided `det(A) ≠ 0`.
-   **Linear system:** `A × x = b  ⇒  x = A⁻¹b`.
-   **Eigen decomposition:** `A v = λ v`, where `λ` is an eigenvalue and
    `v` is an eigenvector.

## Coding
import numpy as np  
import pandas as pd  

# Define a matrix and vector  
A = np.array([[2, 1],  
              [1, 3]])    

b = np.array([5, 6])  

# Display original matrix  
print("Original Matrix A:")  
print(A)  

# Transpose of matrix  
print("\nTranspose of Matrix A:")  
print(A.T)  

# Inverse of matrix  
print("\nInverse of Matrix A:")  
print(np.linalg.inv(A))  

# Solve linear equations  
print("\nSolution of A x = b:")    
print(np.linalg.solve(A, b))  

# Eigenvalues and Eigenvectors  
eigenvalues, eigenvectors = np.linalg.eig(A)  

print("\nEigenvalues:")  
print(eigenvalues)    

print("\nEigenvectors:")  
print(eigenvectors)  

## Output
Original Matrix A:    
[[2 1]  
 [1 3]]  

Transpose of Matrix A:   
[[2 1]  
 [1 3]]  

Inverse of Matrix A:    
[[ 0.6 -0.2]  
 [-0.2  0.4]]  

Solution of A x = b:  
[1.8 1.4]  

Eigenvalues:    
[1.38196601 3.61803399]  

Eigenvectors:  
[[-0.85065081 -0.52573111]   
 [ 0.52573111 -0.85065081]]  

## Result

