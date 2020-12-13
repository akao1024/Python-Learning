
# Introduction to Data Manipulation with Matplotlib

Introducing Pyplot Interface

import matplotlib.pyplot as plt
fig, ax = plt.subplots()
plt.show()

- Adding data to axes
ax.plot(seattle_weather['Month], seattle_weather['MLY-TVG-NORMAL']
plt.show()

- Adding more data

fig, ax = plt.subplots()
ax.plot(seattle_weather['Month], seattle_weather['MLY-TVG-NORMAL'])
ax.plot(austin_weather['Month], austin_weather['MLY-TVG-NORMAL'])
plt.show()

