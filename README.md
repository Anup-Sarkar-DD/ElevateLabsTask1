<div style="text-align: center; margin-bottom: 20px;">
  <h1>Data Cleaning & Preprocessing</h1>
</div>

<ol>
  <li><strong>Step 1:</strong> Loaded dataset from Kaggle using API token and opendatasets</li>

  <li><strong>Step 2:</strong> Checked for missing values
    <ul>
      <li><strong>Step 2a:</strong> Column <code>Age</code> fixed using group median</li>
      <li><strong>Step 2b:</strong> Column <code>Embarked</code> fixed with mode</li>
      <li><strong>Step 2c:</strong> Column <code>Cabin</code> converted to <code>Deck</code> and null values set to 'unknown'<br>
      (Extracted first letter from <code>Cabin</code>, replaced null with 'U' for unknown, dropped original <code>Cabin</code> column)</li>
    </ul>
  </li>

  <li><strong>Step 3:</strong> Converted categorical features into numerical using encoding
    <ul>
      <li><strong>Step 3a:</strong> Column <code>Sex</code> encoded using <code>map</code></li>
      <li><strong>Step 3b:</strong> Columns <code>Embarked</code> and <code>Deck</code> encoded using <code>get_dummies</code></li>
    </ul>
  </li>

  <li><strong>Step 4:</strong> Created visual boxplots for continuous data types (Age and Fare)</li>

  <li><strong>Step 5:</strong> Used IQR method to remove outliers from Age and Fare</li>

  <li><strong>Step 6:</strong> Normalized continuous numerical features</li>

  <li><strong>Step 7:</strong> Saved the cleaned data into a CSV file</li>
</ol>

