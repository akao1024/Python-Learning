# Methods

1. Built-in Functions
2. Back 2 basics

sister = "Liz"
height = 1.73
fam = ["liz", 1.73, "emma", 1.68, "mom", 1.71, "dad", 1.89]

All above are obejects with different type, and methods are functions belonging to objects.
We have string methods, list methods, integer methods, etc.

ConclusionL:
- Everything = object
- Object have method associated, depending on type

3. Methods as follows
- String Methods
Upper() ---> Use it to change all letter to upper class
Count() ---> Use it to count the numbers of the argument within the string
areas = "Allen"/ print(areas.upper()) ---> ALLEN/ print(areas.count("l")) ---> 2
- List Methods
index(), to get the index of the first element of a list that matches its input and
count(), to get the number of times an element appears in a list.
areas = [11.25, 18.0, 20.0, 10.75, 9.50]
# Print out the index of the element 20.0
print(areas.index(20.0))
# Print out how often 9.50 appears in areas
print(areas.count(9.50))
append(), that adds an element to the list it is called on,
remove(), that removes the first element of a list that matches the input, and
reverse(), that reverses the order of the elements in the list it is called on.
# Use append twice to add poolhouse and garage size
areas.append(24.5)
areas.append(15.45)
# Reverse the orders of the elements in areas
areas.reverse()
