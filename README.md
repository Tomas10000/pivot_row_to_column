# pivot_row_to_column

import pandas as pd
import numpy as np
import pyodbc
pd.set_option('max_columns', None)
df = pd.DataFrame({'Event':['a','b','c','d','c','a','a'],'ID':['001','002','003','004','004','004','001']})
df = df.reset_index()


df.pivot_table(index='ID',columns='Event',values='index',aggfunc='count',fill_value=0)
