
# Automating Figures from Data

- Getting unique values of a column

sports = summer_2016_medals["Sport"].unique()
print(sports)


- Bar-chart of heights for all sports

fig, ax = plt.subplots()

for sport in sports:
  sport_df = summer_2016_medals[summer_2016_medals["Sport"] == sport]
  ax.bar(sport, sport_df["Height"].mean(), yerr=sport_df["Height"].std())
ax.set_ylabel("Height(cm)")
ax.set_xticklabel(sports, rotation=90)

plt.show()

