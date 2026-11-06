# E-Commerce Order Data Cleaning

## Project Overview

Cleaned and validated a messy e-commerce order dataset using Python and Pandas.

The dataset contained duplicate records, inconsistent formatting, mixed date formats,
inconsistent units, corrupted text, and other data-quality issues.

## Objective

Transform the raw e-commerce data into a clean and consistent dataset suitable for
further analysis.

## Tools Used

- Python
- Pandas
- Jupyter Notebook
- CSV

## Data Cleaning Performed

- Removed duplicate records
- Standardized country names
- Standardized date formats
- Converted prices to numeric values
- Standardized weight units to grams
- Corrected corrupted product text
- Investigated negative quantities and inconsistent statuses
- Validated order totals against quantities, prices, and discounts
- Retained multiple currencies where no exchange rate was provided

## Results

- Original records: 3,047
- Final records: 3,000
- Columns: 13
- Duplicate rows after cleaning: 0
- Duplicate order IDs after cleaning: 0
- Missing values after cleaning: 0

## Key Data-Quality Finding

88 orders contained negative quantities while being marked as `completed`.
These records were flagged rather than modified because changing business data
without confirmation from the client could introduce incorrect assumptions.

## Files

- `raw/01-ecommerce-orders.csv` — Original dataset
- `analysis.ipynb` — Cleaning and validation process
- `output/cleaned_ecommerce_orders.csv` — Final cleaned dataset