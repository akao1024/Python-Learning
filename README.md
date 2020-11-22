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
Schnauzer   Grey       Cooper       49            17
Labrador    Black      Max          59            29
Chihuahua   Tan        Stella       18            2
St.Bernard  White      Bernie       77            74

- Slicing the outer index level

dogs_srt.loc["Labradour":"Chow Chow"]
                      name     height_cm     weight_kg
breed       color    
Labradour   Brown      Bella        56            25
Poodle      Black      Charlie      43            23
Chow Chow   Bown       Lucy         46            22

*** We need to know that in pandas when we slice the rows, it will include the final value

- Slicing the inner index levels badly

dogs_srt.loc["Tan":"Grey"]
it will come back with "Empty DataFrame"

- Slicing the inner index level correctly

dogs_srt.loc[("Labradour", "Brown"):("Schnauzer":"Grey")]

                      name     height_cm     weight_kg
breed       color    
Labradour   Brown      Bella        56            25
Poodle      Black      Charlie      43            23
Chow Chow   Bown       Lucy         46            22
Schnauzer   Grey       Cooper       49            17

- Slicing columns

dogs_srt.loc[:,"name":"height_cm"]

                      name     height_cm     
breed       color    
Labradour   Brown      Bella        56           
Poodle      Black      Charlie      43           
Chow Chow   Bown       Lucy         46           
Schnauzer   Grey       Cooper       49           


- Slice twice

dogs_srt.loc[("Labradour", "Brown"):("Schnauzer":"Grey"),"name":"height_cm"]

                      name     height_cm     
breed       color    
Labradour   Brown      Bella        56           
Poodle      Black      Charlie      43           
Chow Chow   Bown       Lucy         46           
Schnauzer   Grey       Cooper       49  

- Dog days

dogs = dogs.set_index("date_of_birth").sort_index()
print(dogs)

                        name      breed       color     height_cm     weight_kg
date_of_birth    
2011-12-11              Bella     Labradour   Brown     56            25
2013-07-01              Charlie   Poodle      Black     43            23
2014-08-25              Lucy      Chow Chow   Bown      46            22
2015-04-20              Cooper    Schnauzer   Gray      49            17
2016-09-16              Max       Labrador    Black     59            29
2017-01-20              Stella    Chihuahua   Tan       18            2
2018-02-27              Bernie    St.Bernard  White     77            744


- Slicing by dates

dogs.loc["2014-08-25":"2016-09-16"]

                        name      breed       color     height_cm     weight_kg
date_of_birth    
2014-08-25              Lucy      Chow Chow   Bown      46            22
2015-04-20              Cooper    Schnauzer   Gray      49            17
2016-09-16              Max       Labrador    Black     59            29

- Slicing by partial dates
dogs.loc["2014":"2016"]

                        name      breed       color     height_cm     weight_kg
date_of_birth    
2014-08-25              Lucy      Chow Chow   Bown      46            22
2015-04-20              Cooper    Schnauzer   Gray      49            17
2016-09-16              Max       Labrador    Black     59            29

- Subsetting by row/column number
print(dogs.iloc[2:5, 1:4])

    breed       color     height_cm     
    
2   Chow Chow   Bown      46            
3   Schnauzer   Gray      49            
4   Labrador    Black     59            
