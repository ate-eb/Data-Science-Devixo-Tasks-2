# Devixo Solutions – Task 02
## Data Cleaning & Feature Engineering

### Project Overview

This project focuses on cleaning and preprocessing a real-world dataset using Python, Pandas, NumPy and Scikit-learn.

The objective is to transform raw data into a clean, structured and analysis-ready dataset while creating meaningful new features.

### Dataset

**Name:** Hotel Booking Demand Dataset

**Source:** Kaggle

**Dataset Link:** https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand

**Original Records:** Approximately 119,390

**Original Columns:** 32

The dataset contains hotel booking information, including customer details, reservation dates, booking prices, room types and cancellation status.

### Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Joblib
- SciPy

### Installation

Install the required libraries using:

```bash
pip install pandas numpy scikit-learn scipy joblib
```

### Dataset Setup

1. Download the Hotel Booking Demand dataset from Kaggle.
2. Extract the downloaded file.
3. Locate `hotel_bookings.csv`.
4. Place the CSV file in the same directory as `task2.py`.

### How to Run

1. Open the project folder in PyCharm or VS Code.
2. Make sure all required libraries are installed.
3. Ensure `hotel_bookings.csv` is in the project directory.
4. Run the following command:

```bash
python task2.py
```

### Tasks Performed

**1. Missing Value Handling**

- Identified missing values.
- Removed the Company column due to excessive missing data.
- Filled missing Agent values with 0.
- Filled missing Country values with Unknown.
- Replaced missing Children values with the median.

**2. Duplicate Removal**

- Identified duplicate records.
- Removed duplicate rows using Pandas.

**3. Outlier Detection**

- Applied the Interquartile Range (IQR) method.
- Detected outliers in ADR and Lead Time.
- Handled extreme values using clipping.

**4. Data Type Conversion**

- Converted reservation dates into datetime format.
- Corrected numerical and categorical data types.

**5. Categorical Encoding**

- Applied One-Hot Encoding using Scikit-learn.

**6. Numerical Standardization**

- Applied StandardScaler to numerical features.

**7. Feature Engineering**

Created eleven new features:

1. Total Nights
2. Total Guests
3. Is Family
4. Is Weekend Stay
5. Previous Booking Total
6. Has Previous Cancellations
7. Has Special Requests
8. Booking Value Estimate
9. Arrival Season
10. Lead Time Category
11. Stay Type

**8. Descriptive Statistics**

Generated descriptive statistics before and after preprocessing using Pandas.

**9. Automated Preprocessing Pipeline**

Implemented an automated Scikit-learn pipeline using:

- SimpleImputer
- StandardScaler
- OneHotEncoder
- ColumnTransformer
- Pipeline

The dataset was split into 80% training data and 20% testing data.

### Generated Files

After successfully running the program, the following files are generated:

| File | Description |
|---|---|
| `hotel_bookings_cleaned.csv` | Cleaned dataset with engineered features |
| `hotel_train_preprocessed.npz` | Preprocessed training features |
| `hotel_test_preprocessed.npz` | Preprocessed testing features |
| `hotel_preprocessing_pipeline.pkl` | Saved preprocessing pipeline |
| `feature_names.csv` | Names of transformed features |
| `y_train.csv` | Training target values |
| `y_test.csv` | Testing target values |

### Project Structure

```text
Devixo_Task2/
│
├── task2.py
├── hotel_bookings.csv
├── hotel_bookings_cleaned.csv
├── hotel_train_preprocessed.npz
├── hotel_test_preprocessed.npz
├── hotel_preprocessing_pipeline.pkl
├── feature_names.csv
├── y_train.csv
├── y_test.csv
└── README.md
```

### Conclusion

This project demonstrates a complete data cleaning and feature engineering workflow.

The raw dataset is transformed into a clean and structured format through missing value handling, duplicate removal, outlier treatment, data type conversion, categorical encoding, numerical standardization and feature engineering.

An automated preprocessing pipeline is also implemented using Scikit-learn to make the process reusable and efficient.

---

