
# Reading and Writing CSVs

1. CSV = comma-separated values
2. Designed for DataFrame-like data
3. Most database and spreadsheet programs can use them or create them

- CSV to DataFrame
import pandas as pd
new_dogs = pd.read_csv("new_dogs.csv")
print(new_dogs)

- DataFrame to CSV
new_dogs.to_csv("new_dogs_with_bmi.csv")





