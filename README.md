# Task-1-
Data Cleaning and preprocessing

As part of preparing the Superstore Sales dataset for analysis, I performed a series of data cleaning and preprocessing steps to ensure the data was clean, consistent, and ready for meaningful insights.
1. Handled Missing Values
   I started by identifying missing values using `.isnull()` and filters in Excel. For critical fields like `Order Date` and `Sales`, I removed rows with null values. In non-critical fields like `Postal Code`, I filled missing values with suitable defaults (like `0`).
2. Removed Duplicate Records
   To maintain data accuracy, I removed duplicate rows using `.drop_duplicates()` in Python and the “Remove Duplicates” feature in Excel, ensuring each transaction appeared only once.
3. Standardized Text Fields
   I cleaned and standardized text values in fields such as `Segment` and `Country` by stripping extra spaces and applying consistent capitalization (e.g., converting `" united states "` to `"United States"`).
4. Converted Date Formats
   I converted string-formatted dates in the `Order Date` and `Ship Date` columns into consistent `datetime` objects using `pd.to_datetime()`. This helped in time-based analysis like monthly sales trends.
5. Renamed Column Headers
   To simplify column references and improve readability in code, I renamed the column headers by making them lowercase and replacing spaces with underscores (e.g., `Customer Name` became `customer_name`).
6. Verified and Corrected Data Types
   I reviewed and fixed data types to ensure numerical fields like `Sales` and `Quantity` were correctly treated as numbers, and date fields were recognized as `datetime`. This avoided errors in calculations and date filtering.
