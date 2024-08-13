# Titanic Data Analysis

This project explores the Titanic dataset to understand the factors affecting passenger survival. The analysis is conducted using Python with libraries like `pandas`, `numpy`, `matplotlib`, and `seaborn`.

## Steps Involved

1. **Import Libraries:**
   - The necessary libraries (`pandas`, `numpy`, `matplotlib`, `seaborn`) are imported for data manipulation and visualization.

2. **Load and Inspect Data:**
   - The dataset is loaded using `pandas.read_csv()` and initial exploration is done with `data.head()` and `data.info()` to understand the structure and identify missing values.

3. **Visualize Data:**
   - **Missing Values:** Visualized using a heatmap (`sns.heatmap()`) to identify where data cleaning is needed.
   - **Survival Analysis:** Plotted survival counts and analyzed survival based on gender (`sns.countplot()` with `hue='Sex'`) and passenger class (`hue='Pclass'`).
   - **Age Distribution:** Visualized with a histogram to understand the age distribution of passengers.
   - **Sibling/Spouse Count:** Plotted to examine the distribution of passengers traveling with family.
   - **Fare Distribution:** Analyzed fare distribution across passengers using histograms.

4. **Data Cleaning:**
   - **Impute Missing Ages:** A custom function `impute_age()` is used to fill missing `Age` values based on passenger class (`Pclass`).
   - **Drop Cabin Column:** The `Cabin` column is dropped due to excessive missing values, and the remaining rows with null values are removed.
   - **Final Check:** The cleaned dataset is re-examined with `data.info()` to ensure no missing values remain.

## Dataset Features

- **PassengerId:** Unique ID for each passenger.
- **Survived:** Survival indicator (0 = No, 1 = Yes).
- **Pclass:** Passenger class (1st, 2nd, 3rd).
- **Name:** Passenger name.
- **Sex:** Gender of the passenger.
- **Age:** Passenger age.
- **SibSp:** Number of siblings/spouses aboard.
- **Parch:** Number of parents/children aboard.
- **Ticket:** Ticket number.
- **Fare:** Passenger fare.
- **Embarked:** Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton).

