# 🧹 Data Cleaning with Pandas – Customer Dataset

This project demonstrates **data cleaning and preprocessing using Python (Pandas)**.The raw dataset contained issues like:

- Inconsistent phone number formats
- Duplicate records
- Missing values
- Extra/unnecessary columns
- Inconsistent labels ("Yes"/"Y"/"N"/"No")
- Combined address fields that needed splitting

After cleaning, the dataset is standardized, structured, and ready for analysis.

---

## 🔹 Dataset

### Raw Data (Sample)

| CustomerID | First_Name | Last_Name | Phone_Number | Address               | Paying Customer | Do_Not_Contact | Not_Useful_Column |
| ---------- | ---------- | --------- | ------------ | --------------------- | --------------- | -------------- | ----------------- |
| 1001       | Frodo      | Baggins   | 123-545-5421 | 123 Shire Lane, Shire | Yes             | No             | TRUE              |
| 1002       | Abed       | Nadir     | 123/643/9775 | 93 West Main Street   | No              | Yes            | FALSE             |
| 1003       | Walter     | /White    | 7066950392   | 298 Drugs Driveway    | N               |                | TRUE              |
| ...        | ...        | ...       | ...          | ...                   | ...             | ...            | ...               |

### Cleaned Data (Sample)

| CustomerID | First_Name | Last_Name | Phone_Number | Address                    | Paying Customer | Do_Not_Contact | Street_Address      | State    | Zip_Code |
| ---------- | ---------- | --------- | ------------ | -------------------------- | --------------- | -------------- | ------------------- | -------- | -------- |
| 1001       | Frodo      | Baggins   | 123-545-5421 | 123 Shire Lane, Shire      | Y               | No             | 123 Shire Lane      | Shire    | NaN      |
| 1002       | Abed       | Nadir     | 123-643-9775 | 93 West Main Street        | N               | Yes            | 93 West Main Street | NaN      | NaN      |
| 1010       | Peter      | Parker    | 123-545-5421 | 25th Main Street, New York | Y               | No             | 25th Main Street    | New York | NaN      |

---

## 🔹 Cleaning Steps

1. Removed unnecessary columns (`Not_Useful_Column`).
2. Standardized phone numbers (unified format with dashes).
3. Fixed inconsistent labels in categorical fields (`Yes/No/Y/N`).
4. Handled missing values in `Phone_Number`, `Do_Not_Contact`.
5. Split `Address` into `Street_Address`, `State`, and `Zip_Code`.
6. Removed duplicates (CustomerID 1020 was duplicated).
7. Cleaned extra spaces and symbols from names.

---

## 🔹 Skills Demonstrated

- Python (Pandas) data manipulation.
- Handling duplicates and missing values.
- String cleaning and formatting.
- Feature engineering (splitting address into multiple columns).
- Data quality improvement for downstream analytics.

---

## 🔹 How to Use

1. Open the Jupyter Notebook: `Data Cleaning in Pandas.ipynb`
2. Run the cells step by step to reproduce the cleaning process.
3. Compare the **raw dataset** vs. the **clean dataset**.
