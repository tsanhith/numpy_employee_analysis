# Employee Data Analysis with NumPy

## Project Overview

This project is a practical demonstration of data cleaning and analysis using the NumPy library in Python. Starting with a raw, messy dataset of 40 employees, this analysis walks through the essential steps of data preparation, identifies key insights, and answers practical questions about the relationship between salary and performance.

The primary goal is to showcase a complete data analysis workflow, from handling erroneous data to deriving actionable insights.

---

## Data Cleaning and Preparation

The initial dataset contained several common issues that required cleaning before any analysis could be performed. The following steps were taken to ensure data quality:

1.  **Handled Missing Values (`NaN`):**
    * Missing salary values were replaced with the **mean** of all valid salaries.
    * Missing performance scores were replaced with the **rounded mean** of all valid scores to maintain the integer format of the scores.

2.  **Handled Infinite Values (`inf`):**
    * Infinite salary values, likely data entry errors, were replaced with the **maximum valid salary** found in the dataset.

3.  **Corrected Erroneous Zeros:**
    * Salaries recorded as `0` were treated as missing data and replaced with the **mean** of all other valid salaries.

4.  **Clipped Outlier Data:**
    * Performance scores greater than the maximum possible value of 10 were **clipped** down to 10 to correct for data entry errors.

---

## Key Analyses and Insights

After cleaning the data, several analyses were conducted to uncover trends and insights.

### 1. Average Performance by Salary Bracket
To understand the relationship between compensation and performance, employees were grouped into three salary brackets.

* **Low Bracket (< ₹50,000):** Average Score: **6.00**
* **Mid Bracket (₹50k - ₹75k):** Average Score: **7.21**
* **High Bracket (> ₹75,000):** Average Score: **8.88**

**Insight:** There is a clear positive trend where higher salary brackets are associated with higher average performance scores.

### 2. Salary vs. Performance Correlation
A correlation coefficient was calculated to measure the statistical relationship between salary and performance score.

* **Correlation Coefficient:** `0.52`

**Insight:** This indicates a **moderate positive correlation**. While not a perfect relationship, it confirms that, in general, as salary increases, performance scores also tend to increase.

### 3. Identifying Underpaid High-Performers
An analysis was conducted to find employees who had a high performance score (>= 8) but a below-average salary.

**Insight:** Several high-performing employees were identified as potentially being underpaid, providing a valuable list for management to review for salary adjustments and retention efforts.

### 4. Ranking Top Employees
A composite score was created to rank all employees, giving **60% weight to their normalized salary** and **40% weight to their normalized performance score**.

**Insight:** This provided a final, weighted ranking of the top 5 employees based on a combination of both their compensation and their contribution, offering a more holistic view of top talent.

---

## Technologies Used

* **Python**
* **NumPy**
* **Google Colab / Jupyter Notebook**
