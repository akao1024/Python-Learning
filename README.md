
# Categorical plot types

- Categorical data
a. Data which takes on a limited and fixed number of values
b. Normally combined with numeric data
c. Examples include:
1. geography
2. gender
3. ethnicity
4. blood type
5. eye color

- stripplot
sns.stripplot(data=df, y='DRG Definition', x='Average Covered Charges', jitter=True)

- swarmplot
sns.swarmplot(data=df, y='DRG Definition', x='Average Covered Charges')

- boxplot
sns.boxplot(data=df, y='DRG Definition', x='Average Covered Charges')

- violinplot
sns.violinplot(data=df, y='DRG Definition', x='Average Covered Charges')

- lvplot
sns.lvplot(data=df, y='DRG Definition', x='Average Covered Charges')

- barplot
sns.barplot(data=df, y='DRG Definition', x='Average Covered Charges', hue='Region')

- pointplot
sns.pointplot(data=df, y='DRG Definition', x='Average Covered Charges', hue='Region')

- countplot
sns.countplot(data=df, y='DRG_Code', hue='Region')







