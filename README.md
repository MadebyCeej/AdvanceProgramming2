# Numerical Python Problems

This repository contains two Python programs that demonstrate basic applications of the NumPy library, such as array creation, normalization, and filtering with conditions.

---

## Problems Covered

### 1. Normalization Problem

**Intruction:**  
Create a random 5x5 NumPy array and normalize it using the formula: (X - mean) / std. Save the normalized array as `X_normalized.npy`.  

---

### 2. Divisible by 3 Problem

**Intruction:**  
Create a 10x10 NumPy array containing the squares of the first 100 positive integers (1² to 100²). From this array, determine all numbers divisible by 3 and save them as `div_by_3.npy`.  

---

## Example Code and How to Run

```python
import numpy as np

# ============================
# PROBLEM 1: NORMALIZATION
# ============================

# MAKE A RANDOM 5X5 ARRAY
X = np.random.rand(5, 5)

# FORMULA: (X - MEAN) / STD
X_normalized = (X - X.mean()) / X.std()

# SAVE IT TO FILE
np.save("X_normalized.npy", X_normalized)

# SHOW RESULTS
print("ORIGINAL ARRAY:\n", X)
print("\nNORMALIZED ARRAY:\n", X_normalized)


# ============================
# PROBLEM 2: DIVISIBLE BY 3
# ============================

# MAKE SQUARES FROM 1^2 TO 100^2
A = np.arange(1, 101)**2
A = A.reshape(10, 10)  # PUT INTO 10X10 SHAPE

# PICK NUMBERS DIVISIBLE BY 3
div_by_3 = A[A % 3 == 0]

# SAVE THEM TO FILE
np.save("div_by_3.npy", div_by_3)

# SHOW RESULTS
print("\n10X10 ARRAY OF SQUARES:\n", A)
print("\nNUMBERS DIVISIBLE BY 3:\n", div_by_3)


# ============================
# HOW TO RUN
# ============================

# 1. ENSURE YOU HAVE PYTHON INSTALLED ON YOUR SYSTEM
# 2. INSTALL NUMPY IF YOU DON’T ALREADY HAVE IT:
#    pip install numpy
# 3. CLONE THIS REPOSITORY OR DOWNLOAD THE PYTHON FILE
# 4. OPEN A TERMINAL OR COMMAND PROMPT
# 5. RUN THE PYTHON FILE USING THE FOLLOWING COMMAND:
#    python experiment2.py
