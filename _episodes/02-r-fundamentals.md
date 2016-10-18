---
title: "R fundamentals"
teaching: 20
exercises: 15
questions:
- "How do I use R?"
objectives:
- "Familiarize participants with R syntax"
- "Understand the concepts of objects and assignment"
- "Get exposed to a few functions"
keypoints:
- "R's capabilities are provided by functions."
- "R users call functions and get results"
---



## Working with R 

In this workshop we'll use R in the extremely useful RStudio package. For the most part we'll work interactively, meaning we'll type stuff straight into the R console in RStudio and get our results there too. R's most basic job is as a calculator:


~~~
 3 + 5
~~~
{: .r}



~~~
[1] 8
~~~
{: .output}

~~~
 12 * 2
~~~
{: .r}



~~~
[1] 24
~~~
{: .output}

~~~
 1 / 3
~~~
{: .r}



~~~
[1] 0.3333333
~~~
{: .output}

~~~
 12 * 2
~~~
{: .r}



~~~
[1] 24
~~~
{: .output}

~~~
  3 / 0
~~~
{: .r}



~~~
[1] Inf
~~~
{: .output}


Fairly straightforward, except for the `[1]` in the output, this tells us how far through the output we are. Often R will return long lists of numbers and it can be helpful to have this extra information

###  Variables

We can save the output of operations for later use by giving it a name using the assignment symbol `<-`. Read this symbol as 'gets', so `x <- 5` reads as 'x gets 5'. These names are called variables, because the value they are associated with can change.

Let's give five a name, `x` then refer to the value 5 by it's name. We can then use the name in place of the value. In the jargon of computing we say we are assigning a value to a variable. 


~~~
 x <- 5
 x
~~~
{: .r}



~~~
[1] 5
~~~
{: .output}

 
 ~~~
 x * 2
 ~~~
 {: .r}
 
 
 
 ~~~
 [1] 10
 ~~~
 {: .output}


~~~
y <- 3
x * y
~~~
{: .r}



~~~
[1] 15
~~~
{: .output}


This is of course of limited value with just numbers but is of great value when we have large datasets, as the whole thing can be referred to by the variable.


### Using objects and functions

At the top level, R is a simple language with two types of thing: functions and objects. As a user you will use functions to do stuff, and get back objects as an answer. Functions are easy to spot, they are a name followed by a pair of brackets
 like `mean()` is the function for calculating a mean. The options (or arguments) for the function go inside the brackets: 


~~~
 sqrt(16)
~~~
{: .r}



~~~
[1] 4
~~~
{: .output}


Often the result from a function will be more complicated than a simple number object, often it will be a vector (simple list), like from the `rnorm()` function that returns lists of random numbers


~~~
 rnorm(100)
~~~
{: .r}



~~~
  [1] -0.217774885 -0.837338362  0.640327328 -1.829062507  0.887646632
  [6]  0.502427932 -0.393778563 -2.902732117 -0.550144943 -0.639290541
 [11]  0.458872694 -0.694946096 -1.642791545  0.563632298  0.632353024
 [16]  0.002856642  0.441372967  0.272062688  1.822451371 -0.355026926
 [21] -0.111678970  0.629495813 -0.086642329  1.055039922 -0.431759633
 [26] -0.960530574  0.486153631  1.927589092 -0.221497470  0.163232894
 [31] -0.994099153 -1.279442610  1.069171951 -0.648520287 -0.819790865
 [36]  0.549188856 -0.729408038  0.124942348 -0.319209476  0.406765678
 [41]  0.397305436  0.381116140  1.405136131 -0.523007526 -0.617613440
 [46]  0.056601223  0.169643980  0.190575558 -0.506207759 -1.308758266
 [51] -0.255504805 -0.201064948 -0.520856972  0.038320956  0.011311717
 [56]  0.758941031 -1.139688081 -1.393127788 -1.715928886 -0.117497625
 [61] -0.177001651 -2.305386120 -0.765365904  0.217364685  0.150986372
 [66] -3.134291691 -0.060525547  0.934294972  0.425746839  1.215664673
 [71] -1.158967312  0.438146193  0.139550420  0.385219447 -0.330600739
 [76] -2.985417010  0.392499613  1.640023172 -0.543948039  0.905981602
 [81] -0.656128735  1.032691115  0.771247992  0.333225466 -0.409560282
 [86] -0.119867115 -0.157471259  0.267083518 -0.431189725  0.462176851
 [91] -0.215997060 -0.871354420  0.203404956 -1.379139174 -0.851167783
 [96]  0.075820291 -0.964390184 -0.509216981 -1.996919985 -0.036882921
~~~
{: .output}

We can combine objects, variables and functions to do more complex stuff in R, here's how we get the mean of 100 random numbers.


~~~
numbers <- rnorm(100)
mean(numbers)
~~~
{: .r}



~~~
[1] -0.02620636
~~~
{: .output}

Here we created a vector object with `rnorm(100)` and assigned it to the variable `numbers`. We than used the `mean()` function, passing it the variable `numbers`. The `mean()` function returned the mean of the hundred random numbers.

>## Bracket notation in this document
> I'm going to use the following descriptions for the symbols `()`, `[]` and `{}`: 
>
> `()` are brackets,
> `[]` are square brackets
> `{}` are curly brackets
{: .callout}

> ## Quiz
> 1. Create two variables, `a` and `b`: Add them. What happens if we change a and then re-add a and b?
> 2. We can also assign `a + b` to a new variable, `c`. How would you do this?
> 3. Try some R functions: `round()`, `c()`, `range()`, `plot()` hint: Get help on a function by typing `?function_name` e.g `?c()`. Use the `mean()` function to calculate the average age of everyone in your house (Invent a housemate if you have to).
{: .challenge}
