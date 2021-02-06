---
title: Explore your dataset
weight: 3
---

Start by creating a folder dedicated to our module. On your computer go to My Documents and create a new folder entitled POLXXXX (XXXX indicates the code of our module). Go back to SurreyLearn and download the dataset in the folder. Go back to RStudio, create a new script file, name it `Lab1.R`. 

The first two lines of your script file should include the following three lines. 

```
rm(list = ls()) # This command will clean your workspace
setwd("~/POLXXXX") # This command will tell RStudio to read and save files at the folder POLXXXX
load("EVS_UK.RData")
```

We can now start exploring our data. We can look the names of our variables with the `names()` function.

```{r}
names(EVS_UK)
```

To see how our dataset looks like we can use the `head()` function

```{r}
head(EVS_UK)
```

Let's explore what people think about democracy

```{r}
boxplot(EVS_UK$v137, main= "Attitudes towards democracy",
ylab= "Agree/Disagree")
```


