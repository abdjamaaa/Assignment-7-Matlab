# Assignment-7-Matlab
# Data Visualization Project: Iris & Loan Data Analysis

## Project Overview
The purpose of this project is to perform exploratory data analysis (EDA) using Python and the Matplotlib library. The project is divided into two main tasks:
1. **Fisher's Iris Analysis**: Using biological data to visualize how physical traits (petals and sepals) differentiate species.
2. **Loan Portfolio Analysis**: Using real-world financial data to discover trends in borrowing purposes, interest rate distributions, and repayment risks.

## Class Design and Implementation

### 1. `IrisVisualizationProject`
This class encapsulates the logic for loading and visualizing the Iris dataset. It utilizes a modular approach where each visualization is handled by a specific method.

* **Attributes**:
    * `iris_df`: A Pandas DataFrame that stores the measurements and species labels.
* **Methods**:
    * `__init__`: Loads the dataset using `sklearn.datasets` and prepares the DataFrame.
    * `plot_petal_comparison`: Creates a **Scatter Plot** to illustrate species clustering based on petal length and width.
    * `plot_sepal_distribution`: Generates a **Histogram** to show the frequency distribution of sepal widths.
    * `plot_trait_boxplot`: Produces a **Box Plot** to visualize the statistical variance and medians of sepal lengths across species.

### 2. `LoanDataAnalysis`
This class is designed to process financial datasets and provide insights into lending patterns. It includes robust error handling to ensure the program runs even if the source file is missing.

* **Attributes**:
    * `df`: A Pandas DataFrame containing loan records.
* **Methods**:
    * `__init__`: Attempts to load `loan_data.csv`. If the file is not found, it generates a "Mock" dataset mirroring the Kaggle structure to maintain program functionality.
    * `plot_loan_purpose`: A **Bar Chart** that identifies the most common reasons for loan applications.
    * `plot_interest_distribution`: A **Histogram** showing the spread of interest rates.
    * `plot_repayment_status`: A **Pie Chart** illustrating the ratio of 'Fully Paid' vs 'Defaulted' loans.

## Analysis and Conclusions
Based on the visualizations generated:
* **Iris Insights**: The scatter plot clearly shows that *Iris Setosa* is easily distinguishable from other species based on petal dimensions, while *Versicolor* and *Virginica* have slight overlaps.
* **Loan Insights**: The bar chart indicates that "Debt Consolidation" is the primary driver of loan volume. The pie chart shows a significant minority of loans (approx 15-20%) fall into the "Not Fully Paid" category, suggesting a need for stricter credit grading for high-interest loans.

## Limitations
* **Memory**: The classes load the entire CSV into memory; for extremely large datasets (multi-gigabyte), a chunking method or Dask would be required.
* **Scope**: The visualizations provide a high-level overview but do not yet include predictive modeling (Machine Learning).

## Generative AI Disclosure
Generative AI (Pilot Cohub) was used to assist in the architectural design of the Python classes and to ensure the documentation met the specific criteria of the assignment rubric. A full chat log is included in the repository as `AI_Chat_Log.md`.
