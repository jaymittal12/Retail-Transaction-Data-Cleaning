# Retail Data Cleaning & Transformation Project

## Project Overview

This project demonstrates the complete cleaning and transformation of a large retail transaction dataset containing over 100,000 records.

The raw dataset contained inconsistent formats, missing values, duplicate information, merged product entries, unstructured customer details, and non-standard payment information.

The objective was to convert messy business data into a clean, analysis-ready dataset suitable for reporting, dashboarding, and business intelligence tools such as Power BI.

---

## Dataset Information

### Raw Dataset

* 100,000 transaction records
* Multiple date formats
* Customer names and phone numbers mixed together
* Multiple products stored in a single row
* Missing customer information
* Currency symbols inside numeric columns
* Unstructured payment remarks
* Inconsistent quantity and unit formats

### Clean Dataset

* 146,506 normalized transaction rows
* Standardized date format
* Structured customer information
* One product per transaction row
* Standardized item names
* Clean quantity and unit measures
* Structured payment mode and payment status
* Balance due calculation

---

## Data Cleaning Tasks Performed

### Date Standardization

Converted multiple date formats into a single standard date format.

Examples:

* 23-01-26
* 15.01.2026
* 13/02/2026
* Excel serial dates (45477)

↓

2026-01-23

---

### Customer Information Extraction

Extracted:

* Customer Name
* Customer Phone Number

from mixed text fields.

Examples:

Amit driver 9876543210

↓

Customer Name: Amit Driver

Customer Phone: 9876543210

---

### Product Normalization

Split rows containing multiple products into separate transaction records.

Example:

Maggi; Chana Daal

↓

Maggi

Chana Daal

---

### Quantity and Unit Cleaning

Standardized values such as:

* 4
* 4 kg
* 1 pc

into structured fields:

* Quantity
* Unit Measure

---

### Price Standardization

Removed currency symbols and converted values into numeric format.

Examples:

Rs 120

↓

120

---

### Payment Classification

Mapped unstructured payment remarks into:

Payment Status

* Completed
* Pending
* Partially Pending

Payment Mode

* Cash
* UPI
* Credit

---

### Balance Due Calculation

Created a Balance Due field from payment remarks.

Example:

Cash baki 47

↓

Balance Due = 47

---

## Final Schema

| Column         |
| -------------- |
| Txn_Date       |
| Customer_Name  |
| Customer_Phone |
| Item_Name      |
| Quantity       |
| Unit_Measure   |
| Unit_Rate      |
| Total_Bill     |
| Payment_Status |
| Payment_Mode   |
| Balance_Due    |

---

## Business Value

The cleaned dataset can now be used for:

* Sales Analysis
* Customer Analysis
* Inventory Insights
* Credit Tracking
* Power BI Dashboards
* Revenue Reporting

---

## Key Learning Outcomes

* Large-scale data cleaning
* Data normalization
* Data quality improvement
* Handling missing values
* Text extraction
* Retail transaction transformation
* Preparing data for analytics and visualization

---

## Author

Jay

Aspiring Data Analyst focused on SQL, Python, Excel, Power BI, and Business Analytics.
