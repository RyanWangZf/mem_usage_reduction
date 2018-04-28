# mem_usage_reduction
Tool used to reduce memory usage of dataframe object through transforming dtype of each column.

# User Guidance  
import pandas as pd  
import reduce_mem_usage  
df = pd.read_csv('example.csv')  
props,nalist,dtype_dict = reduce_mem_usage.get(df)  

# Attention  
It fills NaN with the minimum-1 under a column.  
nalist indicates the columns which have NaN and props is the compressed dataframe.  
props is compressed df.  
dtype_dict contains the dtype of each column of compressed, that will assist pd.read_csv('example.csv',dtype=dtype_dict) process.  

You can also save dtype_dict and load it as follows:  

%save
import json  
f = open('dict.json','w',encoding='utf_8_sig')  
json.dump(dtype_dict,f)  
f.close()  

%load  
f = open('dict.json','r')  
dtype_dict = f.read()  
dtype_dict = eval(dtype_dict)  

# Environment  
Python 3.6.2 AMD64  
pandas (0.20.3)  
numpy (1.13.3+mkl)  

# Addtional  
Get it from Internet so that if any copyright is violated, contact me and I will delete it soon.  
