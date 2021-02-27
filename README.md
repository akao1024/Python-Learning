
# Regression plots in seaborn

- Introduction to regplot
a. The regplot function generates a scatter plot with a regression line
b. Usage is similar to distplot
c. The data and x and y variables must be defined
i.e. sns.regplot(x='alcohol', y='pH', data=df)

- Implot() builds on top of the base regplot()

- Implot faceting
a. Organize data by color
i.e. sns.Implot(x='quality', y='alcohol', data=df, hue='type')
b. Organize data by columns
i.e. sns.Implot(x='quality', y='alcohol', data=df, col='type')





