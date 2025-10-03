📱 Smartphone Price and Specification Data Cleaning Project
This repository contains the complete data cleaning, preprocessing, and feature engineering workflow performed on a comprehensive dataset of over 1,000 smartphone models and specifications.

The goal of this project was to transform complex, multi-type raw data (including messy string columns containing specifications like RAM, battery, and camera) into a clean, normalized, and model-ready numerical format suitable for Machine Learning analysis or exploratory data analysis (EDA).

🚀 Project Highlights
# Initial Assessment: Used the skimpy library for rapid initial data overview, identifying non-numeric data types and missing values across key feature columns.

# Missing Value Imputation: Handled missing values in the rating column using the mean, confirmed by visual inspection (boxplot analysis) showing no significant outliers. Categorical missing values (os, card) were imputed using the mode.

# Advanced String Manipulation: Employed Python's regex and Pandas string methods (.str.extract(), .str.replace()) to isolate and convert critical numerical information embedded in lengthy text fields:

# Price: Removed currency symbols (₹) and commas (,) and converted to integer type.

# RAM/ROM: Extracted numerical gigabyte (GB) values from descriptive text strings (e.g., extracting "12" from "12 GB RAM, 256 GB inbuilt").

# Technical Specs: Extracted numerical values for battery_clean (mAh), display_clean (inches), and processor_speed_GHz from their respective text columns.

# Camera: Extracted the primary camera megapixel (MP) value.

# Outlier Management & Scaling: Applied the Interquartile Range (IQR) method to cap outliers in numerical features, ensuring data integrity without skewing the distribution. The final dataset was scaled using StandardScaler from scikit-learn to prepare it for machine learning model training.

# Final Data Structure: The process resulted in a clean DataFrame of over 1,000 entries with 10 features, ready for correlation analysis or predictive modeling.

🛠️ Technologies Used

# Python

# Jupyter Notebook / Google Colab

# Pandas: Data manipulation, cleaning, and transformation.

# NumPy: Numerical operations.

# Matplotlib / Seaborn: Exploratory data visualization (used for boxplot outlier checks).

# skimpy: Quick data summary and profiling tool.

# scikit-learn (StandardScaler): Data normalization for model readiness.

📁 Repository Contents
# Smartphone.ipynb: The main Jupyter Notebook file containing all the data loading, cleaning, manipulation, and scaling steps.

# smartphones.csv: The original dataset used for the analysis (or a clean version if included).
