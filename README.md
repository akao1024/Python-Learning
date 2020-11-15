# Grouped Summary Statistics

1. Grouped Summaries

If we want to learn differnet color dogs mean weight, we can use follows

dogs[dogs["color"] == "Black"].["weight_kg"].mean()
dogs[dogs["color"] == "Brown"].["weight_kg"].mean()
dogs[dogs["color"] == "White"].["weight_kg"].mean()
dogs[dogs["color"] == "Gray"].["weight_kg"].mean()
dogs[dogs["color"] == "Tan"].["weight_kg"].mean()

However, if we use above, it's kind of outdated, so we can use follows instead

dogs.groupby("color")["weight_kg"].mean()

2. Multiple Grouped Summaries

dogs.groupby("color")["weight_kg"].agg([min, max, sum])

3. Group by Multiple variables

dogs.groupby(["color", "breed"])["weight_kg"].mean()

4. Many Groups, many summaries

dogs.groupby(["color", "breed"])[["weight_kg", "height_cm"]].mean()
