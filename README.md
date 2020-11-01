# Manipulating Lists

1. Replace list elements
Simply subset the list and assign new values to the subset.
Ex. x = ["a", "b", "c", "d"], x[1] = "r", print(x) ---> ["a", "r", "c", "d"]

2. Extend or Delete a List
- Extend
x = ["a", "b", "c", "d"]
y = x + ["e", "f"]
print(y) ---> ["a", "b", "c", "d", "e", "f"]
- Delete
If you want to remove the elements from the list, you can use the del statement
x = ["a", "b", "c", "d"]
del(x[1])
print(x) ---> ["a", "c", "d"]

Pay attention here: as soon as you remove an element from a list, the indexes of the elements that come after the deleted element all change!

3. Inner workings of lists
- Behind the scenes (1)
x = ["a", "b", "c"]
y = x
y[1] = z
print(y) ---> ["a", "z", "c"]
print(x) ---> ["a", "z", "c"]

However, if we want to prevent changes in y from also taking effect in x, we'll have to do a more explicitlycopy of the x list. We can do this by list() or by using [:]
- Behind the scenes (2)
x = ["a", "b", "c"]
y = list(x) 
y[1] = z
print(y) ---> ["a", "z", "c"]
print(x) ---> ["a", "b", "c"]
//////
x = ["a", "b", "c"]
y = x[:] 
y[1] = z
print(y) ---> ["a", "z", "c"]
print(x) ---> ["a", "b", "c"]
