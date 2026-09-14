# MSBA 265 Module 1: Foundational Exploratory Data Analysis

## Project Overview

This project performs a reproducible Exploratory Data Analysis (EDA) on the French Motor Third Party Liability Claims dataset from OpenML.

The workflow includes:

- Programmatic data download
- Structural data quality audit
- Business Data Dictionary creation
- Skewness analysis
- Pearson correlation audit
- Correlation heatmap
- Box plots and KDE distribution analysis
- Tukey IQR and Z-score outlier detection
- Production outlier filtering script

## Project Structure

```text
msba265_module1_Wendy/
├── .gitignore
├── README.md
├── requirements.txt
├── Module1_Homework_Report.pdf
├── data/
│   ├── download_data.py
│   ├── raw_business_data.csv
│   └── cleaned_business_data.csv
├── notebooks/
│   └── 01_eda_and_data_dictionary.ipynb
├── src/
│   └── clean_outliers.py
└── reports/
    ├── data_dictionary.csv
    └── figures/
        ├── feature_distributions.png
        ├── correlation_heatmap.png
        └── outlier_filtering_comparison.png
```

## How to Run the Project

### 1. Clone the Repository

```bash
git clone YOUR-NEW-REPOSITORY-URL
cd msba265_module1_Wendy
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

### 3. Activate the Virtual Environment

**Windows:**

```bash
venv\Scripts\activate
```

**macOS/Linux:**

```bash
source venv/bin/activate
```

### 4. Install Required Packages

```bash
pip install -r requirements.txt
```

### 5. Download the Raw Dataset

```bash
python data/download_data.py
```

Expected output:

```text
678013 rows x 12 columns
```

### 6. Run the Jupyter Notebook

Open:

```text
notebooks/01_eda_and_data_dictionary.ipynb
```

Select the virtual environment Python kernel and run all cells from top to bottom.

### 7. Run the Outlier Cleaning Script

```bash
python src/clean_outliers.py
```

This creates:

```text
data/cleaned_business_data.csv
```

The cleaned dataset contains **600,447 records** after applying the Tukey IQR filter to `Density`.

## Final Report

The completed homework report is available here:

[Download the final homework report](Module1_Homework_Report.pdf)

The report contains the final written interpretations, correlation heatmap, distribution analysis, and outlier filtering results.