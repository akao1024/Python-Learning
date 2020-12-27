
# Statistical Plotting

- Add error bars to bar charts
fig, ax = plt.subplots()

ax.bar("Rowing", mens_rowing["Height"], yerr=mens_rowing["Height"].std())
ax.bar("Gymnastics", mens_gymnastics["Height"], yerr=mens_gymnastics["Height"].std())

ax.set_ylabel("Height(cm)")
plt.show()

- Adding error bars to plots

fig, ax = plt.subplots()
ax.errorbar(seattle_weather["MONTH"], seattle_weather["MLY-TAVG-NORMAL"], seattle_weather["ML-TAVG-STDDEV"])
ax.errorbar(austin_weather["MONTH"], austin_weather["MLY-TAVG-NORMAL"], austin_weather["ML-TAVG-STDDEV"])

ax.set_ylabel("Temperature(Fahrenheit)")
plt.show()

- Adding boxplots

fig, ax = plt.subplots()
ax.boxplot([mens_rowing["Height"], mens_gymnastics["Height"]])
ax.set_xticklabels(["Rowing", "Gymnastics"])
ax.set_ylabel("Height(cm)")

plt.show()




