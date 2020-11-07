# Loop Data Structures Part 2

- DataFrame

import pandas as pd
brics = pd.read_csv("path/to/brics.csv", index_col=0)
brics 
    country       Capital    area   population
BR  Brazil        Brasilia   8.516  200.40
RU  Russia        Moscos     17.100 143.50
IN  India         New Dehli  3.286  1252.00
CH  China         Beijing    9.597  1357.00
SA  South Africa  Pretoria   1.221  52.98

for, first try

for value in brics:
  print(value)

---> country, capital, area, population
We can find the loop only print out the column value of the dataframe, so we should the adjustment as follows:

- Iterrows
import pandas as pd
brics = pd.read_csv("brics.csv", index_col=0)

for lab, val in brics.iterrows():
  print(lab)
  print(val)
  
BR
country: Brazil
capital: brasilia
area:8.516
population:200.4
Name: BR, dtype: object

- Selective Prints

import pandas as pd
brics = pd.read_csv("brics.csv", index_col=0)

for lab, row in brics.iterrows():
  print(lab+":"+row["capital"])
---> BR: Brasilia
---> RU: Moscow
....

- Add Column
import pandas as pd
brics = pd.read_csv("brics.csv", index_col=0)

for lab, row in brics.iterrows():
  brics.loc[lab, "name_length"] = len(row["country"])
print(brics)

- apply
import pandas as pd
brics = pd.read_csv("brics.csv", index_col=0)
brics["name_length"] = brics["country"].apply(len)
print(brics)





