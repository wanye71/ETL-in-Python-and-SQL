# ETL in Python and SQL

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