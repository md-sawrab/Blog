---
title: Statistics for Data Science - Measure of Central Tendency
date: 2026-03-15 01:10
categories: [Data Science]
tags: [Statistics, Data Science, Mean, Median, Mode]
---

Welcome back to the Statistics for Data Science series.

In this article, we focus on one of the most important ideas in descriptive statistics: **measure of central tendency**. These measures help us summarize a dataset with a single representative value.

## What Is Central Tendency?

A measure of central tendency is a value that represents the center or typical value of a dataset.

The three main measures are:

- Mean
- Median
- Mode

## Mean

The **mean** is the average of all values.

Formula:

$$
\text{Mean} = \frac{\sum x_i}{n}
$$

Where:

- $x_i$ is each data point
- $n$ is the number of data points

### Example

For values: 10, 20, 30, 40, 50

$$
\text{Mean} = \frac{10 + 20 + 30 + 40 + 50}{5} = 30
$$

### Python Example

```python
import pandas as pd

data = {'A': [10, 20, 30, 40, 50], 'B': [5, 15, 25, 35, 45]}
df = pd.DataFrame(data)

print("Mean of each column:\n", df.mean())
print("Mean of column A:", df['A'].mean())
```

## Median

The **median** is the middle value after sorting data.

- If the number of observations is odd, median is the center value.
- If the number of observations is even, median is the average of the two center values.

### Example

- Data: 2, 4, 6, 8, 10 -> Median = 6
- Data: 2, 4, 6, 8 -> Median = $(4 + 6)/2 = 5$

### Python Example

```python
import pandas as pd

data = pd.DataFrame({
    'A': [1, 3, 5, 7, 9],
    'B': [2, 4, 6, 8, 10]
})

print("Median of each column:\n", data.median())
```

## Mode

The **mode** is the value that appears most frequently.

Mode is especially useful for categorical data, but it can also be used for numerical data.

### Example

For values: 1, 2, 2, 3, 4 -> Mode = 2

### Python Example

```python
import pandas as pd

data = pd.DataFrame({
    'A': [1, 2, 2, 3, 4],
    'B': [2, 2, 3, 4, 4]
})

print("Mode of each column:\n", data.mode())
```

## Distributions and Central Tendency

### Normal Distribution

In a symmetric (normal) distribution:

- Mean = Median = Mode

### Skewed Distribution

In skewed data, these values separate.

- Right-skewed: Mode < Median < Mean
- Left-skewed: Mean < Median < Mode

This happens because outliers pull the mean toward the tail.

## Choosing the Right Measure

- Use **mean** for continuous, approximately normal data without strong outliers.
- Use **median** for skewed data or when outliers are present.
- Use **mode** for categorical data or when the most frequent value is important.

## Final Thoughts

There is no single best measure for every dataset. The best choice depends on your data distribution and the kind of insight you need.

In many practical data science tasks:

- Start with all three
- Inspect distribution and outliers
- Choose the measure that best reflects the real center

Thanks for reading.

Original Medium article:
[Statistics for Data Science - Measure of Central Tendency](https://medium.com/@md-sawrab/statistics-for-data-science-measure-of-central-tendency-0e0400863f72)

Connect on LinkedIn: [md-sawrab](https://www.linkedin.com/in/md-sawrab/)

GitHub: [md-sawrab](https://github.com/md-sawrab)
