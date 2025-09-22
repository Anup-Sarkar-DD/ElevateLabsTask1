<div style="text-align: center; margin-bottom: 20px;">
  <h1>Data Cleaning & Preprocessing</h1>
</div>

- Loaded dataset from Kaggle using API token and opendatasets
- Checked for missing values:
  - Column `Age` fixed using group median (median calculated per group of Pclass and Sex)
  - Column `Embarked` fixed with mode (most frequent value)
  - Column `Cabin` converted to `Deck` by extracting the first letter, and null values replaced with 'U' for unknown; original `Cabin` column dropped
- Converted categorical features into numerical using encoding:
  - Column `Sex` encoded using `map` (male=1, female=0)
  - Columns `Embarked` and `Deck` encoded using one-hot encoding via `get_dummies`
- Created visual boxplots for continuous data types (`Age` and `Fare`) to identify outliers
- Used Interquartile Range (IQR) method to remove outliers from `Age` and `Fare`
- Normalized continuous numerical features (`Age` and `Fare`) using StandardScaler for scaling
- Saved the cleaned data into a CSV file for further use
