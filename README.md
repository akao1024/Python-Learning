
# Concatenation Basics

- Concatenate two tables vertically

Pandas .concat() method can concatenate both vertical and horizontal. 
axis=0, vertical

- Basic Concatenation
1. 3 different tables
2. Same column names
3. Table variable names:
a. inv_jan
b. inv_feb
c. inv_mar

pd.concat([inv_jan, inv_feb, inv_mar])

- Ignoring the index
pd.concat([inv_jan, inv_feb, inv_mar], ignore_index=True)

---> The index order of the concatenation will start from 0

- Setting Labels to Original Tables
pd.concat([inv_jan, inv_feb, inv_mar], ignore_index=False, key=['jan', 'feb', 'mar'])

Those keys will be concatenated infront of the indexes

- Concatenate Table with Different Column Names

pd.concat([inv_jan, inv_feb2], sort=True)

---> We can see that even though two table with different column names, this way can still concatenate them together

However, if we set the join equals to 'inner', then it will only concatenate columns intersections

pd.concat([inv_jan, inv_feb2], join='inner')

- Using Append Method
.append()
1. simplified version of concat() method
2. Supports: ignore_index and sort
3. Does not support: key and join
4. Always join = outer

- Append The Tables
inv_jan.append([inv_feb, inv_mar], ignore_index=True, sort=True)




