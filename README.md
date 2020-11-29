# Inner Join

We have two datafram which are "ward and "census"

Both dataframe have the same column which is called as "ward"

- Inner Join

ward_census = ward.merge(census, on="ward")
print(ward_census)

in the above, we successfully merge the two dataset we have

If we want to merge two different dataframe, those two dataframes should at least have one common column for us to combine

- Suffixes

ward_census = ward.merge(census, on="ward", suffix=("_ward", "_cen"))
print(ward_census.head())

