# Python Lists

1. Lists
- A list is a compound of data, in which you can group different values together
Ex. values = [1, "values", True, [1,2]]

- List of lists
Instead of creating a flast list containing strings and floats, we can create a list of lists.
Ex. House = [["hallway", 11.25],["kitchen", 11.23],["restroom",10.25],["balcony",9.20]]

2. Subsetting Lists
- Each element in the list has its own index, which we can use it to retrieve the element from the list
Ex. x = ["a", "b", "c", "d"]
print(x[1]) ---> b
- If you would like to retrieve the last element within the list, you can use the negative index to select the element
print(x[-1]) ---> d
- Subset and Calculate
After you've extracted values from a list, you can use them to perform additional calculations.
- Slicing and Dicing
Slicing your list means to select multiple elements from your list.
my_list[start:end] ---> The start index will be included, while the end index is not.
Ex. x = ["a", "b", "c", "d"]
print(x[1:3]) ---> b, c
- Slicing and Dicing(2)
Slice the list without specifying the indexes. If you don't specify the begin index, Python figures out that you want to start your slice at the beginning of your list. If you don't specify the end index, the slice will go all the way to the last element of your list.
Ex. x = ["a", "b", "c", "d"]
print(x[:3]) ---> a, b, c
print(x[-2:]) ---> c, d
- Subsetting lists of lists
To subset lists of lists, you can use the same technique as before: square brackets.
x = [["a", "b", "c"],
     ["d", "e", "f"],
     ["g", "h", "i"]]
print(x[2][0]) ---> g
