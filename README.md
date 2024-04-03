# ETL in Python and SQL

## *E*TL EXTRACTING DATA
1. Exploring your data with pandas (Python) and SQL
2. Understanding your data
    - df.head()
    - df.tail()
    - df.shape
    - df.info()
    - df.duplicated()
3. Reading from File
    - sample_data = pd.read_csv('sample_data.csv')
    - sample_data.shape
    - sample_data.duplicated()
    - duplicate_rows = sample_data[sample_data.duplicated()]
4. Loading data from different sources
    - sample_csv = pd.read_csv('sample_data_csv.csv', header=None)
    - sample_exel = pd.read_excel('sample_data_excel.xlsx')
5. Extracting your data
    - import pandas as pd
    - orders = pd.read_excel("H+ Sport Orders.xlsx")
    - orders_execel = orders.head()
    - orders_execel

## E*T*L TRANSFORMIN DATA
1. Cleaning Data
    - Standardization: Transformed by removing duplicates
        - customers = pd.read_excel("H+ Sport Customers.xlsx", sheet_name="data") = Get the file and read it's data
        - customers.head() = Show first 5 records
        - customers.columns = Show column names
        - columns_to_check = ['Email', 'Phone', 'FirstName', 'LastName'] = Create a list of columns to check against
        - duplicates = customers[customers.duplicated(columns_to_check)] = Extract the duplicate data from source
        - duplicates = Display duplicates
        - duplicates.shape = Show how many rows are duplicates (e.g. (29, 9): *29 rows* and 9 columns)
        
2. Preprocessing Data
    - 
3. Formatting Data
    - 
