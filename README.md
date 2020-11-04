# Dictionaries

- Recap
Keys have to be immutable values
{0:"hello", True:"dear", "two":"world"}
---> {0:"hello", True:"dear", "two":"world"}

Immutavle values are like Booleans, Integers, or Stings, which are the values dont change much

{["just","to","eat"]:"value"}
---> TypeError

Since the value of list changes often, so list is not the immutable value we refer to at here.

- Dictionary
1. Add value
world = {'afghanistan': 30.55, 'albania': 2.81,'algeria': 39.21}
world['sealand'] = 0.00027
print(world) ---> {'afghanistan': 30.55, 'albania': 2.81,'algeria': 39.21, 'sealand': 0.00027}

2. Remove
del(world['sealand'])

- Dictionary of dictionaries
# Dictionary of dictionaries
europe = { 'spain': { 'capital':'madrid', 'population':46.77 },
           'france': { 'capital':'paris', 'population':66.03 },
           'germany': { 'capital':'berlin', 'population':80.62 },
           'norway': { 'capital':'oslo', 'population':5.084 } }
# Print out the capital of France
print(europe['france']['capital']) ---> paris
# Create sub-dictionary data
data = {'capital':'rome', 'population':59.83}

# Add data to europe under key 'italy'
europe['italy'] = data

# Print europe
print(europe)

{'italy': {'capital': 'rome', 'population': 59.83}, 'france': {'capital': 'paris', 'population': 66.03}, 'germany': {'capital': 'berlin', 'population': 80.62}, 'norway': {'capital': 'oslo', 'population': 5.084}, 'spain': {'capital': 'madrid', 'population': 46.77}}










