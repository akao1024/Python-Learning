# Sorting and Subsetting

- Sorting

dog.sort_values("weight_kg")

---> This will sort the values by column "weight_kg" from light to heavy

If we want to sort in descending order

dog.sort_values("weight_kg", ascending=False)

---> This will sort the values by column "weight_kg" from heavy to light

If we want sort by multiple variables

dog.sort_values(["weight_kg", "height_cm"])

---> This will sort our values by orders

If we want to sort by multiple variables

dog.sort_values(["weight_kg", "height_cm"], ascending=[True, False])

---> This will sort our values by corresponding ascending orders

- Subsetting Columns

dogs["name"]

---> This will print out the whole name column in dog dataframe

If we want to subset multiple columns

dogs[["breeds", "height_cm"]]

---> This will print out the whole breed & height_cm column in dog dataframe

If we want to subset those rows whose height_cm is more than 50

dogs[dogs["height_cm"] > 50]

---> This will print all those who fit the criteria

If we want to subset based on text data

dogs[dogs["breed"] == "Labrador"]

---> This will print all those who fit the criteria

- Subset based on multiple conditions

is_lab = dogs["breed"] == "Labrador"
is_brown = dogs["color"] == "Brown"
dogs[is_lab & is_brown]

---> This will print all those who fit the criteria


*** Using .isin() to subset

is_black_or_brown = dogs["color"].isin(["Black", "Brown"])
dogs[is_black_or_brown]
