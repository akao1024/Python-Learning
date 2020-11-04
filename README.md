# Pandas

import pandas as pd
brics = pd.read_csv("path/to/brics.csv", index_col = 0)
brics

- index & select data
1. Square Brackets
2. Advanced Methods
a. loc
b. iloc

we should know the difference when extract the data through one bracket or two brackets
1. brics["RU"] ---> 1D labeled array series
2. brics[["RU"]} ---> DataFrame

- Column Access
1. brics[["country"]]
2. brics[["country", "capital"]]

- Row Access
1. brics[1:4]

- Discussion
1. Square Brackets: Limited Functionality
2. Ideally:
a. 2D Numpy Array
b. my_array[rows, columns]
3. pandas
a. loc(label-based)
b. iloc(integer position-based)


Rows Loc
brics.loc["RU"] ---> Row as pandas series
brics.loc[["RU"]] ---> DataFrame

Row&Column Loc
brics.loc[["RU","IN"],["country","capital"]]
brics.loc[:,["country","capital"]]

- Recap
1. Square Bracket
a. Column Access// brics[["country","capital"]]
b. Row Access// brics[1:4]
2. loc(label-based)
a. Row Access// brics.loc[["RU","IN]]
b. Column Access// brics.loc[[:,["country","capital"]]
c. Row&Column Access// brics.loc[[["RU","IN],["country","capital"]]

- Iloc 
Actually iloc is pretty similar to loc, but we use the integer to extract the value instead of the strings
brics.loc[["RU]] ---> brics.iloc[[1]]

Upload the file from datacamp















