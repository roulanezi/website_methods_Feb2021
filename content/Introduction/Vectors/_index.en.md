---
title: Vectors
weight: 3
---

A vector is a collection of elements, a basic data structure. Vectors are crucial in RStudio because they can used to represent variables. The data types contained by a vector could be logical e.g (`TRUE, FALSE`), integer e.g (`1, 2, 3`), or character e.g (`"Roula", "Micheal"`). 
</br>

The `c()` function is very useful as it allows us to create a vector in R. The c stands for **c**ombine (or concatenate), because multiple elements are combined into a vector.

```{r vector, message=FALSE, warning=FALSE, paged.print=FALSE}
x <-c(1,2,3,4,5,6,7,8,9,10)
```

```{r x, message=FALSE, warning=FALSE, paged.print=FALSE}
x
```

An important property of vectors is their length. The length of a vector is the count of how many elements are within it.

```{r length, message=FALSE, warning=FALSE, paged.print=FALSE}
length(x)
```


Additionally, you may create a vector using the `seq()` function. The seq() function generates a sequence of numbers. For example, if you want to generate a sequence of numbers from 0 to 30 incremented by 3 you can do so using the following command

```{r seq, message=FALSE, warning=FALSE, paged.print=FALSE}
seq(from=0, to=30, by=3)
```
