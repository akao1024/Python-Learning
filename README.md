# Random Numbers

- Random Generators
import numpy as np
np.random.rand()
---> 0.95355

np.random.seed(123)
np.random.rand()
---> 0.69646

*** np.random.seed() 
We use this code when we want to create the same random float, but if we want to keep the same value, we should always execute the np.random.seed() first for each loop

np.random.seed(123)
np.random.rand()
---> 0.69646


np.random.seed(123)
np.random.rand()
---> 0.69646

np.random.seed(123)
np.random.rand()
---> 0.69646







