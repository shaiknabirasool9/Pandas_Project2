# Pandas Data Analysis Project

A hands-on exploration of an e-commerce orders dataset using Python and Pandas. The notebook inspects the raw data, identifies data-quality issues, normalizes text values, and examines order distributions. A separate cleaned/exported CSV is included with additional derived fields.

## Objectives

- Inspect the dataset's structure, column types, missing values, and duplicate records.
- Identify inconsistent text values and normalize selected categories.
- Explore order distributions by city, customer, and payment mode.
- Review the provided cleaned dataset and its derived sales and date fields.

## Dataset

The raw file, [`Pandas_Dataset.csv`](./Pandas_Dataset.csv), contains 121 order records and 12 columns, including order and delivery dates, customer, city, product category, quantity, unit price, discount, payment method, and rating.

The project also includes [`cleaned_sales_data.csv`](./cleaned_sales_data.csv), a 120-record export with additional fields such as revenue, discount amount, final revenue, delivery duration, sales labels, and calendar attributes. The export is included as a project artifact; the notebook does not currently show the complete steps that produced it.

### Data privacy

The CSV files contain a `Customer` field with names. Confirm that these are synthetic or otherwise approved for public release before publishing either dataset. Do not commit real personal information without appropriate permission.

## Technologies

- Python
- Pandas
- NumPy (imported in the notebook)
- Jupyter Notebook format
- Google Colab (notebook metadata and its current input path indicate a Colab workflow)

## Data cleaning and exploration

The notebook:

- Inspects the dataset's shape, columns, data types, sample rows, and missing-value counts.
- Identifies a duplicate order record.
- Checks value counts for city, customer, and payment mode.
- Strips leading and trailing whitespace from object columns in a working copy.
- Normalizes the city variants `Hyd` and `HYD` to `Hyderabad`, and `B'lore` to `Bangalore`.

The notebook identifies missing values in `Quantity`, `Discount_Percent`, `Rating`, and `Delivery_Date`, but does not show a missing-value imputation or removal step. It also identifies a duplicate but does not show its removal. The cleaned export contains fewer records, but the notebook does not show the full cleaning/export pipeline that produced it.

## Analysis and reported results

The notebook prints exploratory counts for cities, customers, and payment modes. After the text normalization, the notebook output shows Hyderabad (27), Chennai (24), Bangalore (23), Delhi (21), Mumbai (17), and Pune (9). These counts are from the 121-row working dataset and include the duplicate record identified by the notebook.

The cleaned export includes fields for `Revenue`, `Discount_Amount`, `Final_Revenue`, `Delivery_Days`, sales/customer labels, and date breakdowns. The notebook does not currently calculate or report aggregate revenue totals, category rankings, monthly revenue trends, or chart-based findings. Any sample figures in the accompanying overview image are illustrative and are not presented here as computed results.

## How to run

### Google Colab

1. Open `Pandas_Task_2.ipynb` in Google Colab.
2. Upload `Pandas_Dataset.csv` to the Colab session so it is available at `/content/Pandas_Dataset.csv`.
3. Run the notebook cells from top to bottom.

### Run locally

1. Install Python and Jupyter Notebook, then install the notebook dependencies:

   ```bash
   python -m pip install pandas numpy jupyter
   ```

2. Start Jupyter from the project directory:

   ```bash
   jupyter notebook
   ```

3. Open `Pandas_Task_2.ipynb`. Before running it locally, update the CSV path in the notebook from `/content/Pandas_Dataset.csv` to `Pandas_Dataset.csv` (or to the appropriate local path).

## Project structure

```text
.
├── .gitignore
├── From Raw Data to Business Insights.png
├── Pandas_Dataset.csv
├── Pandas_Task_2.ipynb
├── README.md
└── cleaned_sales_data.csv
```

## Author

Shaik Nabi Rasool

## Repository

[Pandas_Project2 on GitHub](https://github.com/shaiknabirasool9/Pandas_Project2)
