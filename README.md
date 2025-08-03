                                                               week 1 

# 📊 Introduction to Data, Data Analytics, and Machine Learning

This document provides a beginner-friendly overview of key concepts in data analysis and machine learning. Whether you're just starting with data science or need a quick refresher.

---

## 📌 What is Data?

**Data** refers to raw facts and figures collected from observations, measurements, transactions, etc. It has no meaning unless processed.

- Example:
  - Numbers: `21, 35, 47`
  - Text: `"Red"`, `"India"`, `"Sunny"`

---

## 📌 What is Data Analytics?

**Data Analytics** is the process of collecting, cleaning, transforming, and interpreting data to discover useful insights for decision-making.

- Example:
  - Finding which product sold the most last month.
  - Analyzing website traffic to improve performance.

---

## 📌 Data Analyst vs Data Scientist

| Feature           | Data Analyst                                | Data Scientist                               |
|-------------------|----------------------------------------------|----------------------------------------------|
| **Goal**          | Understand trends and patterns               | Predict future outcomes                      |
| **Focus**         | Reporting and visualization                  | Modeling and experimentation                 |
| **Tools**         | Excel, SQL, Power BI, Tableau                | Python, R, TensorFlow, Scikit-learn          |
| **Output**        | Dashboards, reports                          | Predictive models, algorithms                |

---

## 📌 Types of Data

| Type                  | Description                                | Example                          |
|-----------------------|--------------------------------------------|----------------------------------|
| **Structured**        | Organized into tables                      | SQL Databases, Excel             |
| **Unstructured**      | No specific format                         | Images, Videos, Emails           |
| **Semi-Structured**   | Partial structure                          | JSON, XML, HTML logs             |
| **Quantitative**      | Numeric and measurable                     | Age, Salary                      |
| **Qualitative**       | Descriptive or categorical                 | Gender, Country, Color           |

---

## 📌 Types of Learning in AI/ML

| Type                    | Description                                        | Example                         |
|-------------------------|----------------------------------------------------|---------------------------------|
| **Supervised Learning** | Input and labeled output available                 | Email spam detection            |
| **Unsupervised Learning** | Only input, no labels                             | Customer segmentation           |
| **Semi-Supervised**     | Few labeled and many unlabeled examples            | Webpage classification          |
| **Reinforcement Learning** | Agent learns through rewards/punishments        | Game AI, robotic control        |

---

## 📌 Types of Data Analysis

| Type                  | Description                                        |
|-----------------------|----------------------------------------------------|
| **Descriptive**       | Summarizes past data (what happened)               |
| **Diagnostic**        | Investigates causes (why it happened)              |
| **Predictive**        | Forecasts future outcomes                          |
| **Prescriptive**      | Suggests actions based on predictions              |
| **Exploratory**       | Finds unknown patterns or relationships            |

---

## 📌 Mean, Median, Mode in Data Analysis

| Term     | Description                          | Python Example                        |
|----------|--------------------------------------|----------------------------------------|
| **Mean** | Average value                        | `df['col'].mean()`                     |
| **Median** | Middle value in sorted data        | `df['col'].median()`                   |
| **Mode** | Most frequently occurring value      | `df['col'].mode()`                     |

---

## 📌 Example of a Dataset

```csv
Name, Age, Gender, Score
Alice, 24, Female, 85
Bob, 27, Male, 78
Charlie, , Male, 92
Diana, 23, Female,
📌 What is the method called? (Listwise Deletion)
Listwise Deletion is a method for handling missing data by removing any row that contains even a single missing value.

Pros: Simple and easy to implement

Cons: Can lead to significant data loss

📌 How to Perform Listwise Deletion in Python (Pandas)
python
Copy
Edit
import pandas as pd

# Load data
df = pd.read_csv('data.csv')

# Drop rows with any missing values
df_clean = df.dropna()

# Show cleaned data
print(df_clean)
📝 License
This project is free to use for learning and educational purposes.
                                                                                    week 2
from pathlib import Path

# Content for the README.md file on NumPy fundamentals
numpy_readme_content = """
# 🧮 NumPy Fundamentals

This document provides an overview of essential NumPy operations for beginners, including array creation, reshaping, random generation, vector operations, and memory efficiency.

---

## 📌 What is NumPy?

**NumPy** (Numerical Python) is a powerful library for numerical computing in Python. It offers fast operations on arrays and matrices, and is the foundation for most data science libraries.

---

## 📌 Basic Array Creation

```python
import numpy as np

# 1D Array
arr1 = np.array([1, 2, 3])

# 2D Array
arr2 = np.array([[1, 2], [3, 4]])

# Zeros and Ones
zeros = np.zeros((2, 3))
ones = np.ones((3, 3))

# Empty Array
empty = np.empty((2, 2))
📌 Array Generation Functions
python
Always show details

Copy
# Range of values
np.arange(0, 10, 2)       # [0 2 4 6 8]

# Evenly spaced numbers
np.linspace(0, 1, 5)      # [0.   0.25 0.5  0.75 1. ]

# Identity matrix
np.eye(3)                 # 3x3 Identity matrix
📌 Random Generation Functions
python
Always show details

Copy
# Random floats between 0 and 1
np.random.rand(3, 2)

# Random integers
np.random.randint(1, 10, size=(2, 3))

# Normal distribution
np.random.randn(4)

# Seed for reproducibility
np.random.seed(42)
📌 Array Attributes
python
Always show details

Copy
arr = np.array([[1, 2, 3], [4, 5, 6]])

arr.shape      # (2, 3)
arr.ndim       # 2 (dimensions)
arr.size       # 6 (total elements)
arr.dtype      # int64 (data type)
arr.itemsize   # 8 (bytes per element)
📌 Data Types in NumPy
python
Always show details

Copy
# Specifying data types
np.array([1, 2, 3], dtype='float32')
np.array([1, 2, 3], dtype='int8')
📌 Performance and Memory Efficiency
NumPy uses contiguous memory blocks and vectorized operations, making it significantly faster and more memory-efficient than Python lists.

python
Always show details

Copy
import time

a = list(range(1000000))
b = np.arange(1000000)

# Performance comparison (list vs array operations)
📌 Vectorized Operations
python
Always show details

Copy
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

# Element-wise operations
a + b     # [5 7 9]
a * b     # [4 10 18]
a ** 2    # [1 4 9]
📌 Reshaping and Resizing
python
Always show details

Copy
arr = np.arange(12)

# Reshape to 3x4
arr.reshape(3, 4)

# Flatten array
arr.flatten()

# Resize (in-place)
arr.resize((2, 6))
📌 Useful Array Methods
python
Always show details

Copy
arr.sum()           # Sum of all elements
arr.mean()          # Mean
arr.std()           # Standard deviation
arr.max()           # Maximum value
arr.min()           # Minimum value
arr.argmin()        # Index of min
arr.argmax()        # Index of max
arr.T               # Transpose
📝 License
This project is free to use for educational purposes.


