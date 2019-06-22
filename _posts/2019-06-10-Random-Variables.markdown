---
layout: post
title:  "Data lit: Statistics and Probability (2.3) Random Variables"
date:   2019-06-10 12:49:44 -0800
categories:  data lit
---
In this section of the course I learned about random variables, the difference between discrete and continous and about probability distributions.

A random variable(aka random quantity, aleatory variable or stochastic variable) is a variable whose possible values are outcomes of a random phenomenon. 

It can also be defined as a function that maps the outcomes of an upredictable process to numerical quantities. Which means it is dependent on the outcome of an underlying process  provinding the input to this function.

X = Random Variable
Possible values = {0,1}
Random Events = Heads or tails

X = {0,1} 

A random variable can either be discrete, continous or a mixture of both and has a probability distribution which specifies the probability of its values.

Discrete: taking any specified finite or countable list of values, endowed  with a probability mass function characteristic of the random variable's prob. dist.

Coninous: taking any numerical value in an interval or collection of intervals, via a probablity density that is characteristic of the random variable's prob. dist.

![discretevscontinous]({{ "/assets/discrete-vs-continous-growth.png" | absolute_url }})

Lets get a deeper look at distributions...

**The Uniform Distribution**
aka Rectangular Distribution, it is the simplest distribution.

![uniformdistribution]({{ "/assets/uniform-distribution.jpg" | absolute_url }})

The probability of any value between a & b is P.
P(b-a) = 1
P = 1/(b-a)

We can write: 

P(X=x) = 1/(b-a) for a <= x <= b
P(X=x)=0 otherwise.

Ex.
![uniformdistributionex]({{ "/assets/uniform-distribution-ex.jpg" | absolute_url }})

To find the probability between a & a+20 find the shaded area :
 Area = (1/91) * (a+20-a) = (1/91*20) = 20/91
= 0.22 

We can also have the uniform dist. as a cummulative dist.(adding up as it goes along)

![cumulativeuniform]({{ "/assets/cumulative.gif" | absolute_url }})

The probability starts at 0 and builds to 1.

Ex. 
Using past example numbers:

![cumulativeuniformex]({{ "/assets/cumulative-ex.gif" | absolute_url }})

**The Normal Distribution**
The most important continous distribution is the Standard Normal Distribution, the random variable even has its own letter - Z.

The graph for Z is a symetrical bell-shaped curve:
![normaldist]({{ "/assets/normal-dist.gif" | absolute_url }})

Usually, we want to find the probability of Z being between certain values.

Ex.
P(0 < Z < 0.45)
![normaldistex]({{ "/assets/normal-dist-ex.gif" | absolute_url }})

This is found using the Standard Normal Distribution Table. 

P(0 < Z < 0.45) = 0.1736
