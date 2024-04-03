# ETL in Python and SQL

`1. Exploring your data with pandas (Python) and SQL
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