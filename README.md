# Slicing and Subsetting with .loc and .iloc

print(dogs) 

    name      breed       color     height_cm     weight_kg
    
0   Bella     Labradour   Brown     56            25
1   Charlie   Poodle      Black     43            23
2   Lucy      Chow Chow   Bown      46            22
3   Cooper    Schnauzer   Gray      49            17
4   Max       Labrador    Black     59            29
5   Stella    Chihuahua   Tan       18            2
6   Bernie    St.Bernard  White     77            74

- Sort the index befor you slice

dogs_srt = dogs.set_index(["breed", "color"]).sort_index()
print(dogs_srt)

                      name     height_cm     weight_kg
breed       color    
Labradour   Brown      Bella        56            25
Poodle      Black      Charlie      43            23
Chow Chow   Bown       Lucy         46            22
Schnauzer   Gray       Cooper       49            17
Labrador    Black      Max          59            29
Chihuahua   Tan        Stella       18            2
St.Bernard  White      Bernie       77            74






