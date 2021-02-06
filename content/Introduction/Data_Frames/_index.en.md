---
title: Data Frames
weight: 8
---

In R a data frame is a kind of object. Like vectors, data frames store data. However, data frames are differ in that they store multiple vectors. It is important that you understand what a data frame is as it is the most frequently used tool in political statistical analysis. 

If you are having a hard time visualizing a dataframe simply think of what a spreadsheet looks like. Each column of the dataframe can be said to be vector, each vector represents a variable and the rows coincide with an observation. In all statistical software variables are represented by columns and observations are by rows.

You may create a data frame manually if you want but living in the age of big data this is rarely the case! There are many example datasets pre-loaded in RStudio.

Let's have a look at one of these pre-loaded data frames. The data frame is called longley (this is an pre-loaded economic dataset)

Using the `View` function let's see the variables included in the dataset

```{r datalongley, message=FALSE, warning=FALSE, paged.print=FALSE}
data("longley")
```

```{r viewlongley, message=FALSE, warning=FALSE, paged.print=FALSE}
View(longley)
```

![Data frame](Fig_24.PNG)

If we want to see individuals columns, in other words, a specific variable in the data frame, then we use the $ sign between the name of the dataset and the name of the variable (e.g name_of_dataset$name_of_variable). Let's start by observing the Unemployment column.

```{r longleyvariable, message=FALSE, warning=FALSE, paged.print=FALSE}
longley$Unemployed
```

In addition, often we want to access only certain observations (rows) or only certain variables (columns). By using the square brackets [ ] we subset the data frame. In the square brackets, we insert the coordinates for a row and a column. The row is always first followed by the column. For example, longey[7, 5] gives us the 7th row and the 5th column. If we leave the column coordinate empty then we want to see all columns longey[7, ]. If we leave the row coordinate empty then we want all columns.

```{r longleyrows, message=FALSE, warning=FALSE, paged.print=FALSE}
longley[7,5]
```

Leave the column coordinate empty to see the 7th row

```{r longleyrows2, message=FALSE, warning=FALSE, paged.print=FALSE}
longley[7, ]
```

Leave the row empty to see the 5th column

```{r longleycolumns, message=FALSE, warning=FALSE, paged.print=FALSE}
longley[ ,5]
```

We may see the first ten rows of a dataset by adding a colon in the brackets

```{r longleyrows3, message=FALSE, warning=FALSE, paged.print=FALSE}
longley[1:10, ]
```

# Plots

Let's create a plot from our dataset. Let's start by creating a scatterplot with the one axis (X) representing the Year and the other (Y) axis the Gross National Product

```{r longleyplots}
plot(longley$Year,longley$GNP)
```

to create the same plot but by using a line instead of dots we add the argument `type="l"`


```{r longleyplotsline, message=FALSE, warning=FALSE, paged.print=FALSE}
plot(longley$Year,longley$GNP,type = "l")
```


{{% notice Additional Training %}} Use the `title()` function, to give labels to the axes, and a title to your plot. 
The examples in the help are particularly informative.
{{% /notice %}}






