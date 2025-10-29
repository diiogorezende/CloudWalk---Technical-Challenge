# CloudWalk Technical Challenge - Transaction Analysis and Alert System

## Overview

This project analyzes a financial transaction dataset (`transactions.csv`) to identify spending patterns, calculate descriptive statistics, and visualize trends. Based on the analysis, two main metrics are proposed (`Burn Rate` and `Monthly Pace`), and an alert system is detailed, using the "Monthly Pace" metric to help users manage their cash flow.

## Included Files

* **`analysis.ipynb`**: Main Jupyter notebook containing the exploratory data analysis (EDA), calculation of descriptive statistics by category, seasonality analysis, and visualization of spending patterns from the `transactions.csv` file.
* **`report.md`**: Summary report presenting the main findings of the analysis performed in `analysis.ipynb` and the formal definitions of the proposed metrics.
* **`monthly_pace.ipynb`**: Jupyter notebook that defines and demonstrates the `calculate_monthly_pace` function, one of the proposed metrics for the alert system. This notebook expects a processed file (`debit_transactions_processed.csv`).
* **`alert_system_proposal.md`**: Proposal detailing an alert system for users based on the "Monthly Pace" metric.
* **`README.md`**: This file, explaining the project and how to reproduce the results.

## Prerequisites and Setup

1.  **Python**: Ensure you have Python 3.10 or above installed.
2.  **Python Libraries**: Install the necessary libraries listed at the beginning of the Jupyter notebooks. You can install them using pip:
    ```
    pip install pandas numpy matplotlib seaborn scipy json python-dateutil jupyter
    ```
4.  **Jupyter Notebook/Lab**: You will need Jupyter Notebook or Jupyter Lab to run the `.ipynb` files.

## Data

* **`transactions.csv`**: The `analysis.ipynb` notebook expects this file to be located **one directory level above** the folder where the notebook is located (i.e., in `../transactions.csv`). Make sure to place the data file in this location before running the analysis.
* **`debit_transactions_processed.csv`**: The `monthly_pace.ipynb` notebook expects this file (containing only processed debit transactions) to be located **one directory level above** (`../debit_transactions_processed.csv`).

## How to Reproduce the Results

1.  **Clone**: Clone this repo.
2.  **Set Up Environment**: Follow the steps in the "Prerequisites and Setup" section to install Python, and install the necessary libraries.
3.  **Position Data Files**:
    * Place the `transactions.csv` file in the **parent** directory of the directory containing the notebooks.
    * Place the `debit_transactions_processed.csv` file in the **parent** directory (or modify `monthly_pace.ipynb` to read it from another location or generate it).
4.  **Run `analysis.ipynb`**:
    * Start Jupyter Notebook/Lab in your terminal from the project directory or use directly from VSCode.
    * Open the `analysis.ipynb` file.
    * Run all cells sequentially.
    * Observe the outputs, including generated tables, statistics, and plots.
5.  **Run `monthly_pace.ipynb`**:
    * Open the `monthly_pace.ipynb` file in Jupyter.
    * Run the cells. This notebook defines the `calculate_monthly_pace` function and shows an example of its use with a specific date.
6.  **Review Reports**: Open and read the `report.md` and `alert_system_proposal.md` files to understand the analysis summary, metrics, and the alert system proposal.

## Main Results and Outputs

* **`analysis.ipynb`**: Provides a detailed analysis of the transaction data, including spending distribution by category, monthly trends, and identification of categories with higher variability.
* **`monthly_pace.ipynb`**: Defines the `calculate_monthly_pace` function, which projects total monthly spending based on the current pace.
* **`report.md`**: Formally documents the analysis findings and metric definitions.
* **`alert_system_proposal.md`**: Describes the logic and components of a proactive alert system for users.