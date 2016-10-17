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
  [1]  0.45717621 -0.23526023  0.38240693  0.96762736  0.30532116
  [6]  0.37151575  0.25942869 -1.07486418  1.42308818 -1.18205124
 [11]  0.37197071  1.40417790 -0.30525488  0.80626993  0.63539401
 [16]  0.28999168  0.01770248 -0.34006678 -0.87220564  0.14525594
 [21] -0.23630212  0.30473016 -1.63208746  1.06629791 -1.68390643
 [26]  0.35063416  0.10282312  0.72366883  0.74209444 -0.91463253
 [31]  0.98131871 -0.70606362 -0.78256791  0.65905006 -0.28150025
 [36] -0.97823762 -0.72091721  1.43274281 -0.08398903 -0.26973928
 [41]  0.86011956  0.16068080  0.84861951  0.04616353 -0.58262491
 [46]  0.94025653 -0.53323720 -2.96797721 -0.71225877  0.23308377
 [51]  0.52868988  0.04926733 -1.13060568 -1.69867599  2.06375357
 [56]  1.89125870 -0.74531573  0.06469970  1.84669923  1.61094167
 [61]  0.04666530  1.18648705 -0.89378507 -1.40533520  0.68067665
 [66] -0.32872844 -0.60401204 -1.05645100  1.08632121 -0.49769442
 [71]  1.15979056  1.14621808  0.57860686 -0.09025315 -0.46228132
 [76] -0.06098335 -1.39106088 -1.73510189  0.15305101  0.85915786
 [81] -0.77036404  0.40915038 -1.12894396  0.69764436  0.12208382
 [86]  0.21610520  0.50303449  0.15625106 -0.65676346 -0.63378110
 [91] -2.54557835 -0.71084476  1.24662405 -0.79610780  1.34025103
 [96]  1.27194533  0.77436838 -0.04656522 -0.58897474  1.06898836
~~~
{: .output}

We can combine objects, variables and functions to do more complex stuff in R, here's how we get the mean of 100 random numbers.


~~~
numbers <- rnorm(100)
mean(numbers)
~~~
{: .r}



~~~
[1] -0.0138151
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
