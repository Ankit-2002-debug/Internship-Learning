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
