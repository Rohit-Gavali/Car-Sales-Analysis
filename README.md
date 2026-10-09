# Car Sales Data Analysis – Python EDA

## Overview
This project explores a car sales dataset using Python and Jupyter Notebook. It performs exploratory data analysis (EDA), checks data quality, examines sales-related fields, and uses visualizations to better understand the dataset.

## Dataset
The notebook loads the Excel file `JExiCarSales.xlsx`.

The dataset contains **457 rows and 21 columns** in the notebook's initial inspection. Fields include:

- **Sales and costs:** `SalePrice`, `CostPrice`, `TotalDiscount`, `DeliveryCharge`, `SpareParts`, `LaborCost`
- **Vehicle details:** `Make`, `Model`, `Color`, `VehicleType`, `Registration_Date`
- **Invoice and reporting:** `InvoiceDate`, `InvoiceNumber`, `ReportingYear`, `ReportingMonth`
- **Geography and customer:** `ClientName`, `CountryName`, `CountryISOCode`, `OuterPostode`, `Region`
- **Additional field:** `IsDealer` (the notebook reports this column as entirely missing and drops it during cleaning)

> Ensure `JExiCarSales.xlsx` is available in the notebook's working directory before running the notebook.

## Tools and Libraries
- Python
- Jupyter Notebook
- pandas
- NumPy
- Matplotlib
- Seaborn

## Project Workflow
1. **Load the data** from the Excel workbook into a pandas DataFrame.
2. **Inspect the dataset** using the row/column count, data types, and DataFrame information.
3. **Check data quality** by reviewing missing values and duplicate records.
4. **Handle missing values** by dropping the fully empty `IsDealer` column and replacing missing `Region` and `OuterPostode` values with placeholder labels.
5. **Explore the data** with summary statistics and analysis of sales, vehicle, date, and location fields.
6. **Visualize patterns** using Matplotlib and Seaborn charts included in the notebook.

## Data Quality Notes
The initial notebook output reports:
- `IsDealer`: 457 missing values
- `OuterPostode`: 86 missing values
- `Region`: 248 missing values
- No fully duplicated rows detected by the notebook's duplicate check

The notebook drops `IsDealer`, fills missing `Region` values with `Unknown`, and fills missing `OuterPostode` values with `not_define`. These choices are documented here to reflect the notebook's current implementation; confirm that placeholder values suit your reporting requirements before using the data for business decisions.

## How to Run
1. Install Python 3.10 or later and Jupyter Notebook, or use JupyterLab.
2. Install the required libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn openpyxl
   ```

3. Place `JExiCarSales.xlsx` in the same directory as `Car_Sales_operation.ipynb`.
4. Open the notebook:

   ```bash
   jupyter notebook Car_Sales_operation.ipynb
   ```

5. Run the cells from top to bottom.

## Project Structure
```text
Car-Sales-Analysis/
├── Car_Sales_operation.ipynb
├── JExiCarSales.xlsx
└── README.md
```

## Results
The notebook establishes a baseline understanding of the car sales data, identifies missing-data issues, performs initial cleaning, and explores the dataset with Python analysis and visualizations. Use the charts and outputs in the notebook to review patterns in vehicle makes and models, sales and cost values, reporting dates, and geographic fields.

## Future Improvements
- Add a clear business KPI summary, such as total sales value, average sale price, total discounts, and estimated gross margin.
- Validate date fields and business rules before analysis.
- Document assumptions for missing values and outlier handling.
- Export key findings and charts into a concise report.


