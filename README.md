# for Loop

- for var in seq:
  expression
  
---> for each var in seq execute expression

Ex. fam = [1.73, 1.68, 1.71, 1.89]
for height in fam:
  print(height)
---> 1.73
---> 1.68
---> 1.71
---> 1.89

- enumerate
If you also want to access the index information, so where the list element you're iterating over is located, you can use enumerate().
Ex.
fam = [1.73, 1.68, 1.71, 1.89]
for index, height in enumerate(fam):
  print("index " + str(index) + ":" + str(height))

index 0: 1.73
index 1: 1.68
index 2: 1.71
index 3: 1.89

- Loop over string

for c in "family":
  print(c.capitalize())
  
F
A
M
I
L
Y
