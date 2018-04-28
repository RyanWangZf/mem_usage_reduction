# mem_usage_reduction
Tool used to reduce memory usage of dataframe object through transforming dtype of each column.

# User Guidance  
import pandas as pd  
import reduce_mem_usage  
df = pd.read_csv('example.csv')  
props,nalist = reduce_mem_usage.reduce_mem_usage(df) 

# Attention  
It fills NaN with the minimum-1 under the column, nalist indicates the columns which have NaN and props is the compressed dataframe.  

# Environment  
Python 3.6.2 AMD64  
pandas (0.20.3)  
numpy (1.13.3+mkl)  

# Addtional  
Get it from Internet so that if any copyright is violated, contact me and I will delete it soon.  
