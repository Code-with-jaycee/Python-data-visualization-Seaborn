# Python-data-visualization-Seaborn
We cover everything concerning seaborn

# What is SeaBorn?

Seaborn is a Python package for visualizing data. It's useful for making engaging and explorable visualizations of data.

# imports
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline
```

Read the data into DataFrame
```
mtcars = pd.read_csv("mtcars.csv")
mtcars.head(2)
```

# Types plots to cover

<h2>Barplot</h2>
One of the most typical diagrams is a barchart, sometimes known as a barplot. It illustrates how a quantitative and a qualitative variable are connected. Individual categories are shown as bars. Bar height is proportional to the value shown.

# Example

```
# barplot
fig = plt.figure(dpi=600)
res = sns.barplot(x='cyl', y='drat', data=mtcars, palette="bright")
plt.show()
```

# Output
<img src="https://user-images.githubusercontent.com/87891857/211370468-9323faff-6b07-4f3f-bb8b-cb17e2a9400b.png" alt="Bar plot" title="Optional title" width=50% height=50%>


# Countplot

Show bar graphs of categorical bin counts. Count plots are categorical histograms. Compare counts across nested variables using the same API and settings as barplot().

# Example

```
fig = plt.figure(dpi=600)
sns.countplot(x='cyl',data=mtcars, palette="tab10")
```

# Output

<img src="https://user-images.githubusercontent.com/87891857/211373742-44abe4ed-0c85-40d3-b379-83f9ccdb31c1.png" alt="Countplot" title="Optional title" width=50% height=50%>
