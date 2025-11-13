1 – Import the Dataset and Explore Basic Information

In this step, we import all the required Python libraries (like pandas, numpy, seaborn, and matplotlib) and load the Titanic dataset.
We then check the dataset’s shape, data types, and missing values to understand its overall structure.

2 – Handle Missing Values (Mean / Median / Mode Imputation)

Here, we fill the missing values using appropriate strategies:
Numerical columns → filled using mean or median.
Categorical columns → filled using mode (most frequent value).

Note:
Missing values can cause errors or biases in analysis and model training.
Using mean/median/mode helps retain all rows in the dataset instead of dropping them, ensuring no loss of valuable data.

3 – Convert Categorical Features into Numerical (Encoding)

Categorical data (like “male/female” or “S/C/Q” for Embarked) is converted into numerical form.
We use:
Label encoding (for binary categories like Sex).
One-hot encoding (for multi-class columns like Embarked or Pclass).

4 – Normalize / Standardize Numerical Features

We standardize continuous numerical columns (Age, Fare) using StandardScaler, which transforms values so that:
Mean = 0
Standard deviation = 1

5 – Visualize and Remove Outliers (Boxplots + IQR Method)

We first visualize outliers using boxplots, then remove extreme values using the IQR (Interquartile Range) method:
Calculate Q1, Q3, and IQR = Q3 – Q1.
Remove points outside 1.5 × IQR from Q1 and Q3.

Additional Step 6 – Correlation Heatmap (Data Understanding)

We visualize the correlation between numerical columns using a heatmap.
It shows how strongly features are related to each other and to the target variable (Survived).

Why:
Understanding correlations helps in feature selection and identifying multicollinearity — situations where two features are highly correlated.
It gives quick insight into which factors most influence survival.



After all steps:

The dataset is clean, numeric, standardized, and free from missing values or outliers.
It’s ready for model building or deeper statistical analysis.
The workflow is structured and reproducible, suitable for any similar real-world dataset.
