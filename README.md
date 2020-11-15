# Summary Statistics

- Summarizing Numerical Data

1. types :
.median(), .mode(), .min(), max(), .var(), std(), .sum(), .quatile()

dogs["height_cm"].mean()

2. The .agg() method

ex. def pct30(column):
        return column.quantile(0.3)
dogs["height_cm"].agg(pct30)

3. Summaries on multiple columns
dogs[["weight_kg", "height_cm"]].agg(pct30)

4. Multiple Summaries
def pct40(column):
    return column.quantile(0.4)

dogs["height_cm"].agg([pct30, pct40])

5. Cumulative Sum
dogs["height_cm"].cumsum()

6. Cumulative Statistics
.cummax()
.cummin()
.cumprod()
