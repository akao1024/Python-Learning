# Loop Data Structures Part 1

- Ditcionary
Ex.

world = {"afghanistan":30.55, "albania":2.77, "algeria":39.21}
if we use the loop as follows, we will get:

for key, value in world:
  print(key+"---"+str(value))
---> ValueError

Since we get valueerror above, we should use the method instead for us looping through dictionary

for key, value in world.items():
  print(key+"---"+str(value))
---> algeria---30.55
---> afghanistan---2.77
---> algeria---39.21

for k, v in world.items():
  print(key+"---"+str(value))
---> algeria---30.55
---> afghanistan---2.77
---> algeria---39.21

Two things about dictionary:
1. Even though the order within the dictionary is as above, actually for ditcionary there is no order to store the data within it, which is why when we print the key and value out, it will not be the same order as above
2. No matter what argument we gave the loop key or k, for the first argument it will always indicate to key, and foe the second argument will always lead to key value, which is why no matter what argument we gave the loop above, the print out is the same.

- Numpy Arrays
import numpy as np
np_height = np.array([1.73, 1.68, 1.71, 1.89, 1.79])
np_weight = np.array([65.4, 59.2, 63.6, 88.4, 68.7])
bmi = np_weight / np_height ** 2
for val in bmi:
  print(val)
---> 21.852, 20.975, 21.750, 24.747, 21.441

- 2D Numpy Arrays
import numpy as np
np_height = np.array([1.73, 1.68, 1.71, 1.89, 1.79])
np_weight = np.array([65.4, 59.2, 63.6, 88.4, 68.7])
meas = np.array([np_height, np_weight])

for val in meas:
  print(val)
  
---> [1.73, 1.68, 1.71, 1.89, 1.79]
---> [65.4, 59.2, 63.6, 88.4, 68.7]
It prints the whole array above, but what we want here is the value inside of it, so we should as follows:

for val in np.nditer(meas):
  print(val)
---> 1.73, 1.68, 1.71, 1.89, 1.79, 65.4, 59.2, 63.6, 88.4, 68.7

- Recap
1. Dictionary:
for key, val in my_dic.items():
2. Numpy Array
for val in np.nditer(my_array):







