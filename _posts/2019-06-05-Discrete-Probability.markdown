---
layout: post
title:  "Data lit: Statistics and Probability (2.2) Discrete Probability"
date:   2019-06-05 12:49:44 -0800
categories:  data lit
---

In this section we studied ***Discrete Probability***.
First we start with the definition: a probability distribution which a random variable is discrete.


***Expected Value Function***
E(x)=ΣPiXi

Ex company's sales:

| Sales | Frequency | Probability(P) |
|-------|--------|---------|
| $30M | 3 | 0.2143 |
| $40M | 2 | 0.1429 |
| $50M | 4 | 0.2857 |
| $60M | 2 | 0.1429 |
| $70M | 2 | 0.1429 |
| $80M | 1 | 0.0714 |

Probability = Frequency / Frequency Total

ΣP = 1

E(x)=ΣPiXi >>> E(x) = 50.719

So, on average, you can have a ***$51M in sales each day***. It also represents the mean of the dataset.

***Variance and Standard Deviation***

***Variance*** : is one way to measure the spread in a dataset, it is defined as the sum of the squared deviations from the mean.

For discrete probability distributions: Var(x) = ΣPiXi^2 - [E(x)]^2

For our example company's variance:
Var(x) = 234.953039

***Standard Deviation*** : is simply equal to the square root of variance

σ = √Var(x)

σ = √234.953039 = 15.32817794

***Since the Standard Deviation is 15, the worst sales days can go down to $14M and the best sales days can be $95M!***

We will look at two well known discrete probability distributions:
Bernoulli and Poisson.

***Bernoulli distribution***
A ***bernoulli trial*** is any random experiment in which there are exactly two possible outcomes. (Ex.Coin flip)

A ***bernoulli distribution*** is the probability distribution for a series of bernoulli trials.

It is the simplest kind of discrete probability distribution that can only take two possible values, usually 0 and 1.(Success and Failure)

***Conditions*** :
The variable being measured must be both random & independent. This means the probability must be the same for every trial. Or else, the bernoulli distribution will not be accurate.

***Variance for Bernoulli distribution*** :
The probability of success is P. The probability of failure is 1-P.
The variance of a series of bernoulli trials is measured by how spread out the values of the dataset are.

Var = P(1-P)

For the coin flip, Var = (0.5)(1-0.5) = 0.25

***Poisson Distribution***
• It is used to calculate the probability of an event occurring over a certain interval.

•The interval can be on of time, area, volume, or distance.

•Usually, it can be applied to systems with a large number of possible events, each of which is rare.

λ^ke^-λ
| -------- |
  k!
