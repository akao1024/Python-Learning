
# Creating DataFrame

- Dictionaries

my_dict = { "key1": value1, "key2": value2, "key3": value3 }

my_dict["key1"] ---> value1

- Creating DataFrames

1. From a list of dictionaries
Constructed row by row

2. From a dictionary of lists
Constructed column by column

- List of dictionaries - by row

name    breed       height(cm)    weight(kg)    date of birth
Ginger  Dachsund    22            10            2019-03-14
Scout   Dalmaian    59            25            2019-05-19

list_of_dicts = [
{"name": "Ginger", "breed":"Dachsund", "height(cm)":22, "weight(kg)":10, "date of birth":"2019-03-14"},
{"name": "Scout", "breed":"Dalmaian", "height(cm)":59, "weight(kg)":25, "date of birth":"2019-05-19"}
]

new_dogs = pd.DataFrame(list_of_dicts)
print(new_dogs)

- Dictionary of lists - by column
name    breed       height(cm)    weight(kg)    date of birth
Ginger  Dachsund    22            10            2019-03-14
Scout   Dalmaian    59            25            2019-05-19

Key = column name
Value = list of column values

dict_of_lists = {
"name": ["Ginger", "Scout"],
"breed":["Dachsund", "Dalmaian"],
"height(cm)":[22, 59],
"weight(kg)":[10, 25],
"date of birth":["2019-03-14", "2019-05-19"]
}

new_dogs = pd.DataFrame(dict_of_lists)
print(new_dogs)





