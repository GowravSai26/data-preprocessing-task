# Task 1: Interview Questions and Answers

A summary of the interview questions and their answers related to the data cleaning and preprocessing task.

---

## 1. What are the different types of missing data?

Not all missing data is the same; the reason it's missing helps determine the best way to handle it. There are three main types:

* **Missing Completely at Random (MCAR):** The missing data has no relationship with any other value in the dataset. It's like a random glitch, such as a survey respondent accidentally skipping a question.
* **Missing at Random (MAR):** The missingness is related to another variable we have information about. For example, if men are less likely to answer a survey question about anxiety, the missing "anxiety" data is related to the "gender" column.
* **Missing Not at Random (MNAR):** The missingness is related to the value of the missing data itself. For instance, people with very high incomes might intentionally skip the "income" question.

---

## 2. How do you handle categorical variables?

Machine learning models require numerical input, so categorical variables (text labels) must be converted into numbers. The two most common methods for this are **One-Hot Encoding** and **Label Encoding**.

---

## 3. What is the difference between normalization and standardization?

Both are feature scaling techniques used to bring numerical data to a common scale, but they use different methods:

* **Normalization (Min-Max Scaling):** This scales all data to a fixed range, typically **0 to 1**. It's useful when the data does not follow a Gaussian (bell curve) distribution.
* **Standardization (Z-score Scaling):** This rescales data to have a **mean of 0 and a standard deviation of 1**. It's less affected by outliers and is preferred for algorithms that assume a Gaussian distribution.

---

## 4. How do you detect outliers?

Outliers are data points that are significantly different from the rest. They can be detected using:

* **Visual Methods:**
    * **Box Plots:** Points that fall outside the "whiskers" of the plot are potential outliers.
    * **Scatter Plots:** Can reveal points that are far from the main cluster of data.
* **Statistical Methods:**
    * **Interquartile Range (IQR):** The mathematical method behind box plots. Any point outside a calculated range is considered an outlier.
    * **Z-score:** Calculates how many standard deviations a data point is from the mean. A high Z-score (e.g., > 3) indicates an outlier.

---

## 5. Why is preprocessing important in ML?

Preprocessing is crucial because real-world data is often messy, and models need clean, well-structured data to learn effectively. This follows the **"Garbage In, Garbage Out"** principle. A well-prepared dataset leads to more accurate and reliable models, as many algorithms cannot handle non-numeric, unscaled, or missing data.

---

## 6. What is one-hot encoding vs label encoding?

These are two primary methods for converting categorical data into numbers:

* **Label Encoding:** Assigns a unique integer to each category (e.g., `Red`=0, `Green`=1, `Blue`=2). The main drawback is that it can create a false sense of order that the model might misinterpret. It's best used for **ordinal data**, where a natural order exists (e.g., `Small`=0, `Medium`=1, `Large`=2).
* **One-Hot Encoding:** Creates a new binary (0/1) column for each category. It treats all categories equally without implying any order. It's best used for **nominal data**, where no intrinsic order exists (e.g., city names, colors).

---

## 7. How do you handle data imbalance?

Data imbalance occurs when one category is much more common than another (e.g., 99% non-fraud vs. 1% fraud transactions). This can bias a model to always predict the majority class. You can handle this by:

* **Resampling the Data:**
    * **Oversampling:** Create more synthetic examples of the minority class.
    * **Undersampling:** Remove some examples from the majority class.
* **Using Better Metrics:** Don't rely on accuracy. Use metrics like **Precision, Recall, and F1-Score**, which provide a better view of performance on the rare, minority class.

---

## 8. Can preprocessing affect model accuracy?

**Yes, significantly.** Proper preprocessing, such as correctly handling missing values and scaling features, provides the model with high-quality data, which almost always improves its performance and reliability. Conversely, poor preprocessing can confuse the model, introduce bias, and severely harm its accuracy.