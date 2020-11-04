# Pandas

1. High level data manipulation tool
2. Built on Numpy
3. DataFrame

- DataFrame from Dictionary
dict = { "country":["Brazil", "Russia", "India", "China", "South Africa"],"capital":["Brasilia", "Moscow", "New Delhi", "Beijing", "Pretoria"],"area":[8.516, 17.10, 3.286, 9.597, 1.221]"population":[200.4, 143.5, 1252, 1357, 52.98] }

1. key(column labels)
2. values(data, column by column)

import pandas as pd
brics = pd.DataFrame(dict)
print(brics)

if we want to change the index of the dataframe, we will use as follows
brics.index = ["BR", "RU", "IN", "CH", "SA"]
print(brics)

- DataFrame from CSV
1. CSV = Comma-Seperated Values
2. Assume we have a csv file called brics.csv, and we want to use the data from the file, should do as follows
import pandas as pd
brics = pd.read_csv("path/to/brics.csv")
And we want the pandas show us the data from the very first column instead of the index column, we should adjust as follows
brics = pd.read_csv("path/to/brics.csv", index_col=0)
print(brics)













