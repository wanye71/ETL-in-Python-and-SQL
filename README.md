# ETL in Python and SQL

## *E*TL EXTRACTING DATA
1. Exploring your data with pandas (Python) and SQL
    ```python
     import pandas as pd
    ```
2. Understanding your data
    + df.head()
    + df.tail()
    + df.shape
    + df.info()
    + df.duplicated()
3. Reading from File
    + sample_data = pd.read_csv('sample_data.csv')
    + sample_data.shape
    + sample_data.duplicated()
    + duplicate_rows = sample_data[sample_data.duplicated()]
4. Loading data from different sources
    + sample_csv = pd.read_csv('sample_data_csv.csv', header=None)
    + sample_exel = pd.read_excel('sample_data_excel.xlsx')
5. Extracting your data
    + import pandas as pd
    + orders = pd.read_excel("H+ Sport Orders.xlsx")
    + orders_execel = orders.head()
    + orders_execel

## E*T*L TRANSFORMIN DATA
1. Cleaning Data
    + Standardization: Transformed by removing duplicates
        + customers = pd.read_excel("H+ Sport Customers.xlsx", sheet_name="data") = Get the file and read it's data
        + customers.head() = Show first 5 records
        + customers.columns = Show column names
        + columns_to_check = ['Email', 'Phone', 'FirstName', 'LastName'] = Create a list of columns to check against
        + duplicates = customers[customers.duplicated(columns_to_check)] = Extract the duplicate data from source
        + duplicates = Display duplicates
        + duplicates.shape = Show how many rows are duplicates (e.g. (29, 9): *29 rows* and 9 columns)
## Extract and transform data

> Remove Job rating, New Salary, Tax Rate and 2.91%

- Read data from data set
    + employees = pd.read_excel("H+ Sport Employees.xlsx", sheet_name='Employees+Table')
- Show number of columns and rows in data sheet
    + employees.shape
- Show column names
    + employess.columns
    Index(['Employee Name', 'Building', 'Department', 'Status', 'Hire Date',
       'Month', 'Years', 'Benefits', 'Salary', 'Job Rating', 'New Salary',
       'Tax Rate', '2.91%'],
      dtype='object')
- Remove columns
    + columns_to_remove = ['Job Rating', 'New Salary',
       'Tax Rate', '2.91%']
- Drop columns
    + employees = employees.drop(columns=columns_to_remove)
- Show colums
    + employess.columns
    Index(['Employee Name', 'Building', 'Department', 'Status', 'Hire Date',
       'Month', 'Years', 'Benefits', 'Salary'],
      dtype='object')

# Data Warehousing and Data Lakes
## Loading data into relational databases
### Imports
```python
import pandas as pd
import sqlalchemy as db
```
### Read data set from file
```python
customers = pd.read_excel("H+ Sport Customers.xlsx", sheet_name="data")
```
### Drop duplicate records
```python
customers.drop_duplicates()
```
### Drop column from data set
```python
customers = customers.drop(columns="Zipcode")
```
### Connect to database
```python
engine = db.create_engine('postgresql://tifwqjsh:mB2WRPrTia0MwJdWH2RQiZujAheiCfzU@salt.db.elephantsql.com/tifwqjsh')
```
### Insert data from Excel file into database
```python
customers.to_sql("customers", engine, if_exists='replace', index=False)
```