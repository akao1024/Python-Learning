# Python Learning

1. Variable
- Assignment
A variable allows you to refer to a value with a name. Use "=" to create a variable as follows:
x = 5

Remember, "=" in Python means assignment, it doesn't test equality!
- Specific, case-sensitive name
- Call up value through variable name

2. Types of Variable
- int, or integer: a number without a fractional part. savings, with the value 100, is an example of an integer.
- float, or floating point: a number that has both an integer and fractional part, separated by a point.
1.1 is an example of float
- str, or string: a type to represent text. You can use single or double quotes to build a string.
"Hello, world !"
- bool, or boolean: a type to represent logical values. Can only be True or False (the capitalization is important!).
True

Type Function for you to check what type of the value or the variable is, use it as follows:
print(type(1)) --> int

3. Operations with other types
- As mentioned within the class, different types behave differently in Python

print(1+1) --> 2
print("i am allen" + "i am allen") --> i am alleni am allen
print(True+True) --> 2

4. Typel Conversion
str() --> helps you to change the value into string 
int() --> helps you to change the value into integer
float() --> helps you to change the value into float
bool() --> helps you to change the value into boolean
Examples:
x = 100

print("I made $" + str(x) + " from stocks yesterday") --> I made $100 from stocks yesterday
