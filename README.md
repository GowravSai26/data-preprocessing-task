# Data-Preprocessing-Task
Repository to showcase data preprocessing tasks.

# Task 1: Data Cleaning and Preprocessing

## Project Objective

The objective of this task is to clean and prepare the raw Titanic dataset to make it suitable for machine learning applications. This notebook walks through the standard steps of a data preprocessing workflow.

---

## Steps Implemented

The following data cleaning and preprocessing steps were performed:

1.  **Data Exploration:** The dataset was initially loaded and inspected to identify basic information like data types, null values, and statistical summaries.

2.  **Handling Missing Values:** Missing data in the `age` and `embarked` columns were filled using the median and mode respectively. The `deck` column was dropped due to a high number of missing entries.

3.  **Categorical Encoding:** Categorical features such as `sex` and `embarked` were converted into numerical format using one-hot encoding so they can be used by ML models.

4.  **Feature Scaling:** Numerical features (`age`, `fare`) were standardized to ensure they are on a similar scale, preventing features with larger values from dominating the model.

5.  **Outlier Removal:** Outliers in the `fare` column were visualized using a boxplot and subsequently removed using the Interquartile Range (IQR) method to improve model robustness.

---

## Tools and Libraries Used

* **Python**
* **Pandas** for data manipulation and analysis
* **NumPy** for numerical operations
* **Matplotlib & Seaborn** for data visualization
* **Scikit-learn** for feature scaling

---

## How to Run

1.  Clone the repository to your local machine.
2.  Create and activate a Python virtual environment.
3.  Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```
4.  Open the `code-book.ipynb` notebook in VS Code or any Jupyter environment.