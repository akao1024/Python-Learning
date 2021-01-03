
# Adding a third variable with hue

- Tips Dataset

import pandas as pd
import seaborn as sns

sns.load_dataset("tips")
tips.head()

- A basic scatter plot

import matplotlib.pyplot as plt
import seaborn as sns

sns.scatterplot(x="total_bill", y="tip", data=tips)
plt.show()

- A scatter plot with hue

import matplotlib.pyplot as plt
import seaborn as sns

sns.scatterplot(x="total_bill", y="tip", data=tips, hue="smoker")
plt.show()

---> This plot will show the scatter plot of smokers and non-smokers by different colors, also a legend will show up as follows

- Setting hue order

import matplotlib.pyplot as plt
import seaborn as sns

sns.scatterplot(x="total_bill", y="tip", data=tips, hue="smoker", hue_order=["Yes", "No"])
plt.show()

---> This will change the order of of hue shows up on the legend

- Specifying hue colors

import matplotlib.pyplot as plt
import seaborn as sns

hue_colors={"Yes": "black", "No": "red"}
sns.scatterplot(x="total_bill", y="tip", data=tips, hue="smoker", palette=hue_colors)
plt.show()

- Use HTML hex color codes with hue

import matplotlib.pyplot as plt
import seaborn as sns

hue_colors={"Yes": "#808080", "No": "#00FF00"}
sns.scatterplot(x="total_bill", y="tip", data=tips, hue="smoker", palette=hue_colors)
plt.show()

- Use hue with count plots

import matplotlib.pyplot as plt
import seaborn as sns

sns.countplots(x="smoker", data=tips, hue="sex")
plt.show()




