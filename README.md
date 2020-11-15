# Counting

Let's say we have df named as vet_visits

1. Dropping duolicate names

vet_visits.drop_duplicates(subset="name")
---> This will use "name" column to help us drop the duplicates


2. Dropping duplicate parins

But, what if we have dogs with same name but different breeds?
we can use this instead

unique_dogs = vet_visits.drop_duplicates(subset=["name", "breed"])

3. Value counts

unique_dogs["breed"].value_counts()
---> This will count the vlaues by breeds

unique_dogs["breed"].value_counts(sort=True)
---> This will help us count but also sort

4. Proportions
unique_dogs["breed"].value_counts(normalize=True)
---> This will give us the proportion of the distribution of breed column

