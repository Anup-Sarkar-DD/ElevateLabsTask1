<div style="text-align: center; margin-bottom: 20px;">
  <h1>Data Cleaning & Preprocessing</h1>
</div>

- Loaded the Titanic dataset directly from Kaggle using an API token and the `opendatasets` package, ensuring seamless and authorized data access.
- Conducted a thorough missing value analysis to identify columns with incomplete data:
  - For the `Age` column, missing values were imputed using the median age calculated within groups defined by passenger class (`Pclass`) and gender (`Sex`), improving accuracy by leveraging relevant subgroup information.
  - The `Embarked` column's missing values were filled with the mode (most frequent embarkation point), preserving the dominant category distribution.
  - Extracted the deck letter from the `Cabin` column by taking the first character; missing cabins were labeled as 'U' (Unknown). The original `Cabin` column was then dropped to simplify the dataset.
- Categorical feature transformation was performed to convert text labels into numerical values:
  - The `Sex` column was encoded using a simple label mapping where 'male' was replaced by 1 and 'female' by 0.
  - The multi-category columns `Embarked` and `Deck` were transformed using one-hot encoding via `pandas.get_dummies()`, creating binary indicator columns for each category.
- Visualized the distributions of continuous features (`Age` and `Fare`) with boxplots to detect outliers and understand the spread of data.
- Applied the Interquartile Range (IQR) method to systematically identify and remove outliers in `Age` and `Fare` that fall significantly outside the typical range, reducing noise and potential bias in modeling.
- Standardized the numerical continuous features (`Age` and `Fare`) using `StandardScaler` to rescale values to have zero mean and unit variance, which aids many machine learning algorithms in convergence and performance.
- Finally, exported the cleaned and processed dataset to a CSV file to facilitate subsequent modeling, analysis, and reproducibility.

