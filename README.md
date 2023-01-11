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


<h2>Horizontal count plot</h2>

```
fig = plt.figure(dpi=600)
sns.countplot(y="carb", data=mtcars, palette="rocket")
```

# Output

<img src="https://user-images.githubusercontent.com/87891857/211446435-bc346414-146f-4117-8ac7-d16823ee5881.png" alt="Horizontal countplot" title="Optional title" width=50% height = 50%>


Which column in the data frame will be utilized to store the color code is specified by the hue parameter. As an illustration, we can look at the lmplot reference manual.

# Example
<img src="https://user-images.githubusercontent.com/87891857/211447634-1a40399b-1cfa-457a-80ef-5708a00925be.png" alt="Cue countplot" title="Optional title" width=50% height=50%>


# distplot

A distribution plot, or Distplot, displays how the data is spread out. The Seaborn Distplot is a graphical representation of the frequency distribution of continuous data. The distplot with its many permutations is displayed using the Seaborn and Matplotlib libraries.

# Example

```
fig = plt.figure(dpi=600)
sns.distplot(mtcars.mpg, bins=10, color='g')
```

# Output
<img src="https://user-images.githubusercontent.com/87891857/211448992-9a928bc9-4a7d-4eb8-8b10-42a0060dbce7.png" alt="dist plot" title="Optional title" width=50% height = 50%>


# Heatmap

A heatmap is a color-coded, two-dimensional representation of data in which each value in a matrix is shown separately. Annotated heatmaps can be made with the Seaborn package and then modified with Matplotlib's capabilities to suit the needs of the maker.

# Example

```
# corr shows correlation of the data
# cbar draws the color bar
fig = plt.figure(dpi=600
sns.heatmap(mtcars.corr(), cbar=True, linewidths=0.5)
```

# Output
<img src="https://user-images.githubusercontent.com/87891857/211450190-0d428825-ff2d-4c0a-984c-10cff83ea217.png" alt="Heatmap" title="Optional title" width=50% height = 50%>



# Scatter plot

Using a scatter plot, you can figure out how two numbers are related to each other. We can tell if there is a relationship between the variables based on where the data points, called markers, are placed.

# Example

```
iris = sns.load_dataset('iris')
fig = plt.figure(dpi=600)
sns.scatterplot(x='sepal_length', y = 'petal_length', data=iris, hue="species")
```

# Output
<img src="https://user-images.githubusercontent.com/87891857/211451848-d6281819-3694-493a-95a0-b8849e3ea63d.png" alt="Scatter plot" title="Optional title" width=50% height=50%>


# Pairplot

With the Seaborn Pairplot, we can show how two variables in a dataset are related to each other. This makes a nice way to see the data and helps us understand it by putting a lot of data into one figure. This is very important when we are looking at our dataset and trying to get to know it.

# Example

```
sns.pairplot(iris,hue="species", palette='Set1')
```

# Output
<img src="https://user-images.githubusercontent.com/87891857/211455462-9c411c25-61b4-48df-8953-53a0c4404995.png" alt="pairplot" title="Optional title" width=100% height=100%>

# Lineplot

One of the simplest types of charts is the lineplot (lmplot). A line is depicted on a flat, two-dimensional surface. You can choose between seaborn and matlotlib to generate plots.

# Example

```
fig = plt.figure(dpi=600)
sns.lmplot(x='petal_length', y='petal_width',hue='species', data=iris, markers=["o", "*", "^"])
```

# Output
<img src="https://user-images.githubusercontent.com/87891857/211457005-ac634f6f-197f-4892-b55d-97637ec06929.png" alt="Lmplot" title="Optional title" >


# boxplot
