
# List comprehensions

- Populate a list with for loop
nums = [12, 8, 21, 3, 16]
new_nums = []
for num in nums:
  new_nums.append(num+1)
print(new_nums)


- A list comprehension
nums = [12, 8, 21, 3, 16]
new_nums = [num + 1 for num in nums]
print(new_nums)

- For loop and list comprehension syntax
new_nums = [num + 1 for num in nums]
for num in nums:
  new_nums.append(num+1)
print(new_nums)

- List comprehension with range()
result = [num for num in range(11)]
print(result)

- List comprehensions
1. Collapse for loops for building lists into a single line
2. Components
a. Iterable
b. Iterator variable (represent members of iterable)
c. Output expression

- Nested loops (1)

pairs_1 = []
for num1 in range(0, 2):
  for num2 in range(6, 8):
    pairs_1.append(num1, num2)
print(pairs_1)

   
- Nested loops (2)

pairs_2 = [(num1, num2 for num1 in range(0,2) for num2 in range(6,8)]
print(pairs_2)
Tradeoff: readability





