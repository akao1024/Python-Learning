# Random Walk

Known in Science
1. Path of molecules
2. Gambler's financial status

- Heads or Tails
import numpy as np
np.random.seed(123)
outcomes=[]
for x in range(10):
  coin = np.random.randint(0,2)
  if coin == 0:
    outcomes.append("heads")
  else:
    outcomes.append("tails")
print(outcomes)

["heads", "tails","heads", "tails","heads", "tails","heads", "tails","heads", "tails"]

- Heads or Tails: Random Walk
import numpy as np
np.randon.seed(123)
tails=[0]
for x in range(10):
  coin = np.random.randint(0,2)
  if coin == 0:
    tails.append(tails[x]+coin)
print(tails)

[0, 0, 1, 1, 1, 1, 2, 2, 3, 3]










