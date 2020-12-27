
# Creating Histograms

- A bar chart again

fig, ax = plt.subplots()
ax.bar("Rowing", mens_rowing["Height"].mean())
ax.bar("Gymnastics", mens_gymnastic["Height"].mean())
ax.set_ylabel("Height(cm)")
plt.show()

- Histograms Introduction
fig, ax = plt.subplots()
ax.hist(mens_rowing["Height"])
ax.hist(mens_gymnastic["Height"])
ax.set_xlabel("Height(cm)")
ax.set_ylabel("# of observations")
plt.show()

- Labels are needed

fig, ax = plt.subplots()
ax.hist(mens_rowing["Height"], label="Rowing")
ax.hist(mens_gymnastic["Height"], label="Gymnastics")
ax.set_xlabel("Height(cm)")
ax.set_ylabel("# of observations")
ax.legend()
plt.show()

- Setting the number of bins

fig, ax = plt.subplots()
ax.hist(mens_rowing["Height"], label="Rowing", bins=5)
ax.hist(mens_gymnastic["Height"], label="Gymnastics", bins=5)
ax.set_xlabel("Height(cm)")
ax.set_ylabel("# of observations")
ax.legend()
plt.show()

- Setting bin boundaries

ax.hist(mens_rowing["Height"], label="Rowing", 
        bins=[150, 160, 170, 180, 190, 200, 210])
ax.hist(mens_gymnastic["Height"], label="Gymnastics", 
        bins=[150, 160, 170, 180, 190, 200, 210])
ax.set_xlabel("Height(cm)")
ax.set_ylabel("# of observations")
ax.legend()
plt.show()

- Transparency

ax.hist(mens_rowing["Height"], label="Rowing", 
        bins=[150, 160, 170, 180, 190, 200, 210],
        histtype="step")
ax.hist(mens_gymnastic["Height"], label="Gymnastics", 
        bins=[150, 160, 170, 180, 190, 200, 210],
        histtype="step")

ax.set_xlabel("Height(cm)")
ax.set_ylabel("# of observations")
ax.legend()
plt.show()


