# csi_week1_assignment

# E-Commerce Data Cleaning & Feature Engineering Pipeline

## 📌 Project Overview
This project focuses on executing an end-to-end data cleaning, preprocessing, and feature engineering pipeline on a raw e-commerce product catalog using Python and Pandas.

## 🛠️ Data Pipeline Steps & Milestones

* **Step 1 & 2: Data Loading & Exploration**
  Ingested the primary product catalog containing data streams ($1,000$ initial entries across $24$ distinct features). Analyzed structural properties and integrity constraints using `.head()` and `.info()`.

* **Step 3: Missing Value Imputation**
  Identified and addressed structural null entries across critical attributes (like `discount`) using safe `.fillna()` parameters to ensure downstream analytical accuracy without dropping viable rows.

* **Step 4: Target Subset Filtering**
  Performed conditional rows isolation to filter the catalog down to high-performing product inventories boasting a user review score of **`rating > 3.0`**.

* **Step 5: Deduplication Check**
  Implemented a dynamic `if-else` verification pipeline checking row signatures via `.duplicated().sum()` to guarantee data uniqueness before feature calculation.

* **Step 6: Feature Engineering (Derived Metrics)**
  Engineered a new transactional column metric named **`total_amount`** using vectorized matrix operations to calculate actual discount values:
  $$\text{Total Amount} = \text{Initial Price} \times \left(\frac{\text{Discount}}{100}\right)$$

* **Step 7: Dataset Serialization**
  Compiled the final completely transformed, filtered dataset and exported it cleanly into a shareable storage matrix format named `Cleaned_Combined_dataset1.csv`.

## 📁 Repository Structure
* `E_Commerce_Data_Cleaning.ipynb` - The primary production notebook containing all step-by-step cleaning logic execution.
* `Cleaned_Combined_dataset1.csv` - The final filtered, completely clean production-ready catalog dataset.
