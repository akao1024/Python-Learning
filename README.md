# Explicit Indexes

print(dogs) 

    name      breed       color     height_cm     weight_kg
    
0   Bella     Labradour   Brown     56            25
1   Charlie   Poodle      Black     43            23
2   Lucy      Chow Chow   Bown      46            22
3   Cooper    Schnauzer   Gray      49            17
4   Max       Labrador    Black     59            29
5   Stella    Chihuahua   Tan       18            2
6   Bernie    St.Bernard  White     77            74

dogs.columns
---> Index(['name', 'breed', 'color', 'height_cm', 'weight_kg'])
dogs.index
---> RangeIndex(start=0, stop=7, step=1)

- Setting a column as the index
dogs.ind = dogs.set_index('name')
print(dogs.ind)

          breed       color     height_cm     weight_kg
name    
Bella     Labradour   Brown     56            25
Charlie   Poodle      Black     43            23
Lucy      Chow Chow   Bown      46            22
Cooper    Schnauzer   Gray      49            17
Max       Labrador    Black     59            29
Stella    Chihuahua   Tan       18            2
Bernie    St.Bernard  White     77            74

- Removing an Index
dogs_ind.reset_index()

    name      breed       color     height_cm     weight_kg   
0   Bella     Labradour   Brown     56            25
1   Charlie   Poodle      Black     43            23
2   Lucy      Chow Chow   Bown      46            22
3   Cooper    Schnauzer   Gray      49            17
4   Max       Labrador    Black     59            29
5   Stella    Chihuahua   Tan       18            2
6   Bernie    St.Bernard  White     77            74


- Drop an Index

dogs_ind.reset_index(drop=True)

          breed       color     height_cm     weight_kg    
0         Labradour   Brown     56            25
1         Poodle      Black     43            23
2         Chow Chow   Bown      46            22
3         Schnauzer   Gray      49            17
4         Labrador    Black     59            29
5         Chihuahua   Tan       18            2
6         St.Bernard  White     77            74

- Subsetting with indexes

dogs[dogs["name"]].isin(["Bella", "Stella"])

name      breed       color     height_cm     weight_kg    
Bella     Labradour   Brown     56            25
Stella    Chihuahua   Tan       18            2

dogs_ind.loc[["Bella", "Stella"]]
          breed       color     height_cm     weight_kg 
name    
Bella     Labradour   Brown     56            25
Stella    Chihuahua   Tan       18            2

- Index Values dont need to be unique

dogs_ind2 = dogs.set_index("breed")
print(dogs_ind2)
               name     color     height_cm     weight_kg
breed    
Labradour      Bella    Brown     56            25
Poodle         Charlie  Black     43            23
Chow Chow      Lucy     Bown      46            22
Schnauzer      Cooper   Gray      49            17
Labrador       Max      Black     59            29
Chihuahua      Stella   Tan       18            2
St.Bernard     Bernie   White     77            74

- Subsetting on duplicated index values

dogs_ind2.loc["Labradour"]

               name     color     height_cm     weight_kg
breed    
Labradour      Bella    Brown     56            25
Labrador       Max      Black     59            29

- Multi-level indexes

dogs_ind3 = dogs.set_index(["breed", "color"])
print(dogs_ind3)

- Subset the outer level with a list

dogs.ind3.loc[["Labradour", "Chihuahua"]]

- Subset inner levels with a list of tuples
dogs_ind3.loc[[("Labradour", "Brown"), ("Chihuahua", "Tan")]]

- Sorting by index values
dogs_ind3.sort_index()

- Cotrolling sort_index
dogs_ind3.sort_index(level=["color", "breed"], ascending=[True, False])



