
# Introcution to relation plots and subplots

- Questions about quantitative variables
1. Height vs Weight
2. Number of school absences vs final grade
3. GDP vs percent literate

- Introducing relplot()
1. Creating "relational" plots: scatter plots or line plots
Why use relplot() instead of scatterplot() ?
2. relplot() lets you create subplots in a single figure 


- Scatterplot() vs relpot()

1. Scatterplot()

import seaborn as sns
import matplotlib.pyplot as plt

sns.scatterplot(x="total_bill", y="tip", data=tips)
plt.show()

2. Relplot()

import seaborn as sns
import matplotlib.pyplot as plt

sns.relplot(x="total_bill", y="tip", data=tips, kind="scatter")
plt.show()

- Subplots() in columns

import seaborn as sns
import matplotlib.pyplot as plt

sns.relplot(x="total_bill", y="tip", data=tips, kind="scatter", col="smoker")
plt.show()

- Subplots() in rows

import seaborn as sns
import matplotlib.pyplot as plt

sns.relplot(x="total_bill", y="tip", data=tips, kind="scatter", row="smoker")
plt.show()

- Subplots() in rows and columns

import seaborn as sns
import matplotlib.pyplot as plt

sns.relplot(x="total_bill", y="tip", data=tips, kind="scatter", col="smoker", row="time")
plt.show()

- Wrapping columns

import seaborn as sns
import matplotlib.pyplot as plt

sns.relplot(x="total_bill", y="tip", data=tips, kind="scatter", col="day", col_wrap=2)
plt.show()

- Ordering columns

import seaborn as sns
import matplotlib.pyplot as plt

sns.relplot(x="total_bill", y="tip", data=tips, kind="scatter", col="day", col_wrap=2, col_order=["Thu.", "Fri.", "Sat.", "Sun."])
plt.show()
