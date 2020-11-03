# 2D Numpy Arrays

1. Type of Numpy Arrays
import numpy as np
np_height = np.array([1.73, 1.68, 1.71, 1.89, 1.79])
np_weight = np.array([65.4, 59.2, 63.6, 88.4, 68.7])
print(type(np_height)) ---> numpy.ndarray

The "n" within ndarray refers to the dimensional of the array, like the above we have 1 dimensional array
But, numpy arrays can allow more than one dimensional data import. We will use a list to combines two dimensional lists together 

2. 2D Numpy Arrays
np_2d = numpy.array([[1.73, 1.68, 1.71, 1.89, 1.79],
                     [65.4, 59.2, 63.6, 88.4, 68.7]])
print(np_2d) ---> array([[1.73, 1.68, 1.71, 1.89, 1.79],
                         [65.4, 59.2, 63.6, 88.4, 68.7]])
print(np.2d.shape) ---> (2,5)

3. Subsetting
Will upload images to understand the conception
