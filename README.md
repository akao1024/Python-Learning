# Pivot Tables

1. Group by to pivot table

dogs.groupby("color")["weight_kg"].mean() = dogs.pivot_table(values="weight_kg", index="color")

2. Different Statistics

import numpy as np

dogs.pivot_table(values="weight_kg", index="color", aggfunc=np.median)

3. Multiple Statistics

dogs.pivot_table(values="weight_kg", index="color", aggfunc=[np.mean, np.median])

4. Pivot on Two Variable

dogs.groupby(["color", "breed"])["weight_kg"].mean() = dogs.pivot_table(values="weight_kg", index="color", columns="breed")

5. Filling Missing Values with 0 

dogs.pivot_table(values="weight_kg", index="color", columns="breed", fill_value=0)

6. Summarizing with Pivot Tables

dogs.pivot_table(values="weight_kg", index="color", columns="breed", fill_value=0, margins=True)
