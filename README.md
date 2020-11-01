# Numpy

## Alternative to Python List
## Different from lists, we can't use list to do the calculation with a collection of data, but we can do it through Numpy Arrays

Ex. We would like to calculate a group of people's BMI
weight = [60.2, 61.2, 60.4, 64.6]
height = [1.71, 1.73, 1.75, 1.76]
If we use the list to do the calculation as follows, then it will returm TypeError: unsupported operand type(s) for **: 'list' and 'int'
weight / height ** 2 

Therefore, we need a more supportive program to help us do the calculation over a collection of data
import numpy as np
weight_array = np.array(weight)
height_array = np.array(height)
weight / height ** 2 ---> It will return the end results as requested

However, numpy array can only contain one type of element
np.array([1.0, "is", True])
--->array["1.0", "is", "True"]
This is a place which is different from list

- Different types: different behavior
python_list = [1, 2, 3]
numpy_array = np.array([1, 2, 3])
python_list + python_list ---> [1, 2, 3, 1, 2, 3]

numpy_array + numpy_array ---> array([2, 4, 6])

Numpy Subsetting
weight_array = np.array([60.2, 61.2, 60.4, 64.6]) ---> array([60.2, 61.2, 60.4, 64.6])

weight_array[1] ---> 61.2
weight_array > 61 ---> array([False, True, False, True])
weight_array[weight_array > 61] ---> array([61.2, 64.6])


