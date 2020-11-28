
# Visualizing Your Data

- Histogram
import matploylib.pyplot as plt
dog_pack["height_cm"].hist()
plt.show()

- Different Bins

dog.pack["height_cm"].hist(bins=20)
plt.show()

dog_pack["height_cm"].hist(bins=5)
plt.show()

- Bar Plots
avg_weight_by_breed = dog_pack.groupby("breed)["weight"].mean()
print(avg_weight_by_breed)

- Bar Plots 2

avg_weight_by_breed.plot(kind="bar")
plt.show()

avg_weight_by_breed.plot(kind="bar", title="Mean Weight by Dog Breed")
plt.show()

- Line Plots
sully.plot(x="date", y="weight_kg", kind="line")
plt.show()

- Rotating Axis Labels

sully.plot(x="date", y="weight_kg", kind="line", rot=45)
plt.show()

- Scatter Plots

dog_pack.plot(x="height_cm", y="weight_kg", kind="scatter")
plt.show()

- Layering Plots

dog_pack[dog_pack["sex] == "F"]["height_cm"].hist()
dog_pack[dog_pack["sex] == "M"]["height_cm"].hist()
plt.show()

- Add a Legend
dog_pack[dog_pack["sex] == "F"]["height_cm"].hist()
dog_pack[dog_pack["sex] == "M"]["height_cm"].hist()
plt.legend(["F","M"])
plt.show()

- Transparency
dog_pack[dog_pack["sex] == "F"]["height_cm"].hist(alpha=0.7)
dog_pack[dog_pack["sex] == "M"]["height_cm"].hist(alpha=0.7)
plt.legend(["F","M"])
plt.show()

