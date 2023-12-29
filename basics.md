# Basics
Pandas is a popular Python library for data manipulation and analysis. Here are some of the basics of Pandas:

1. **Data Structures:**
   - **Series:** A one-dimensional labeled array capable of holding any data type.
     ```python
     import pandas as pd

     series = pd.Series([1, 2, 3, 4])
     ```

   - **DataFrame:** A two-dimensional table with rows and columns, similar to a spreadsheet or SQL table.
     ```python
     data = {'Name': ['Alice', 'Bob', 'Charlie'],
             'Age': [25, 30, 35]}
     df = pd.DataFrame(data)
     ```

2. **Reading and Writing Data:**
   - Pandas supports reading data from various file formats like CSV, Excel, SQL, and more.
     ```python
     # Reading from CSV
     df = pd.read_csv('data.csv')

     # Writing to CSV
     df.to_csv('output.csv', index=False)
     ```

3. **Indexing and Selection:**
   - Pandas provides various ways to index and select data, including label-based indexing and position-based indexing.
     ```python
     # Selecting a column
     age_column = df['Age']

     # Selecting rows based on a condition
     young_people = df[df['Age'] < 30]
     ```

4. **Basic Operations:**
   - Pandas supports basic operations, such as arithmetic operations, element-wise operations, and statistical functions.
     ```python
     # Arithmetic operations
     df['Age'] = df['Age'] + 5

     # Statistical summary
     summary = df.describe()
     ```

5. **Handling Missing Data:**
   - Pandas provides functions to handle missing data, including dropping or filling missing values.
     ```python
     # Dropping rows with missing values
     df_cleaned = df.dropna()

     # Filling missing values with a specific value
     df_filled = df.fillna(0)
     ```

6. **Grouping and Aggregation:**
   - Pandas allows grouping data based on one or more columns and performing aggregations on the groups.
     ```python
     # Grouping by 'Department' and calculating average age
     avg_age_by_dept = df.groupby('Department')['Age'].mean()
     ```

7. **Merging and Concatenating:**
   - Pandas supports merging and concatenating dataframes, allowing you to combine data from different sources.
     ```python
     # Concatenating two dataframes vertically
     combined_df = pd.concat([df1, df2], axis=0)
     ```

8. **Time Series Data:**
   - Pandas has robust support for working with time series data, including date-based indexing and time-based operations.
     ```python
     # Creating a time series dataframe
     time_series = pd.date_range('2023-01-01', '2023-01-10')
     ```

These are just some of the basics of Pandas. The library is extensive and provides many more functionalities for data analysis and manipulation in Python.
