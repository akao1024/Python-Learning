
# Missing Values

In pandas, we use "NaN" to inform you the data is missing

- Detecting Missing Values
dogs.isna()

- Detecting any missing values
dogs.isna().any()

- Counting missing values

dog.isna().sum()

- Plotting missing values

import matplotlib.pyplot as plt
dog.isna().sum.plot(kind="bar")
plt.show()

- Removing missing values

dogs.dropna()

- Replacing missing values
dogs.fillna(0)






