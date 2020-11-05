# Filtering Pandas and DataFrames

Will insert related curriculum resources within the repository

we still use brics as our example on this course

import pandas as pd
brics = pd.read_csv("path/to/brics.csv", index_col=0)
brics 
    country       Capital    area   population
BR  Brazil        Brasilia   8.516  200.40
RU  Russia        Moscos     17.100 143.50
IN  India         New Dehli  3.286  1252.00
CH  China         Beijing    9.597  1357.00
SA  South Africa  Pretoria   1.221  52.98


- Goal
1. Select countries with area over 8 million km2
2. 3 steps
a. Select the area column
b. Do comparison on area column
c. Use result to select country

- Step1: Get Column
brics["area"]
BR  8.516  
RU  17.100 
IN  3.286  
CH  9.597  
SA  1.221  
Name: area, dtype: float64

- Step2: Compare
brics["area"] > 8
BR  True  
RU  True 
IN  False  
CH  True  
SA  False  
Name: area, dtype: bool

is_huge = brics["area"] > 8

- Step3: Subset DF

brics[is_huge]
    country       Capital    area   population
BR  Brazil        Brasilia   8.516  200.40
RU  Russia        Moscos     17.100 143.50
CH  China         Beijing    9.597  1357.00

- Summary:
is_huge = brics["area"] > 8
brics[is_huge] or brics[brics["area"] > 8]

- Boolean Operators
import numpy as np
np.logical_and(brics["area"] > 8, brics["area"] < 10)
brics[np.logical_and(brics["area"] > 8, brics["area"] < 10)]

    country       Capital    area   population
BR  Brazil        Brasilia   8.516  200.40
CH  China         Beijing    9.597  1357.00




