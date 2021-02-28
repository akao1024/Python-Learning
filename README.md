
# Customizing with matplotlib

- Matplotlib axes
a. most customization available through matplotlib axes objects
b. axes can be passed to seaborn functions
i.e.
fig, ax = plt.subplots()
sns.distplot(df['Tuition'], ax=ax)
ax.set(xlabel='Tuition 2013-14')

- Further customizations
a. the axes object supports many common customizations
ie
fig, ax = plt.subplots()
sns.distplot(df['Tuition'], ax=ax)
ax.set(xlabel='Tuition 2013-14', ylabel='Distribution', xlim=(0, 50000), title='2013-14 Tuition and fees distribution')

- Combining plots
a. It is possible to combine and configure multiple plots
ie.
fig, (ax0, ax1) = plt.subplots(nrows=1, ncols=2, sharey=True, figsize=(7, 4))
sns.distplot(df['Tuition'], ax=ax0)
sns.distplot(df.query('Staete = "MN"')['Tuition'], ax=ax1)

ax1.set(xlabel='Tuition (MN)', xlim=(0, 70000))
ax1.axvline(x=20000, label='My Budget', linestyle='--')
ax1.legend()






