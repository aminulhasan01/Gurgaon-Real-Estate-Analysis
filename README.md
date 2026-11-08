# Real Estate Market Exploratory Data Analysis (EDA)

## Project Overview
This data analytics project performs Exploratory Data Analysis (EDA) on a real estate dataset to uncover pricing trends, property valuations, and market dynamics. The analysis is built with Python and Pandas, focusing on answering core business questions regarding locality premiums, RERA approval impacts, and builder pricing strategies.

## Tech Stack
* **Language:** Python
* **Data Manipulation:** Pandas
* **Data Visualization:** Matplotlib, Seaborn

## Data Cleaning Pipeline
Raw real estate data requires significant standardization before analysis. The script executes a robust cleaning pipeline:
* **Header Standardization:** Stripped whitespace, converted to lowercase, and replaced spaces with underscores for programmatic access.
* **Type Casting & String Formatting:** Cleaned numeric columns (`price`, `area`, `rate_per_sqft`) by removing comma separators and casting them from strings to integer/float types for mathematical aggregation.
* **Boolean Mapping:** Converted text-based `rera_approval` statuses into explicit `True/False` boolean values.
* **Categorical Normalization:** Stripped and lowercased categorical features (`status`, `flat_type`) to prevent duplicate groupings.
* **Deduplication:** Removed duplicate records to ensure statistical accuracy.

## Key Insights & Business Questions Answered
The analysis aggregates and groups the data to answer 10 specific market questions:

1. **Maximum Valuation:** Identifies the single costliest flat in the dataset, detailing its BHK configuration, locality, and society.
2. **Premium Localities:** Determines which locality commands the highest average property price.
3. **Price Per Square Foot:** Identifies the locality with the highest average rate per square foot.
4. **Construction Status Premium:** Compares the average pricing of ready-to-move properties versus under-construction properties.
5. **Regulatory Impact (RERA):** Analyzes whether RERA-approved properties command a price premium over non-approved properties.
6. **Area vs. Price Correlation:** Maps the relationship between total property area and final price.
7. **Configuration Valuation:** Determines which BHK configuration is the most expensive on a per-square-foot basis.
8. **Property Type Valuation:** Identifies the costliest flat type in the market.
9. **Builder Pricing Strategy:** Extracts the top 5 real estate companies/builders commanding the highest rates per square foot.
10. **Size Efficiency:** Uses Seaborn scatter plots to visualize if larger homes are more or less expensive per square foot.

## How to Run the Project
1. Clone the repository to your local machine.
2. Ensure you have the required libraries installed:
   ```bash
   pip install pandas matplotlib seaborn