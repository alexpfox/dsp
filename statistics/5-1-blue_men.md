[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

## Outline:

This is a classic example of hypothesis testing using the normal distribution. The effect size used here is the Z-statistic.

## Problem:

In the BRFSS (see Section 5.4), the distribution of heights is roughly normal with parameters μ = 178 cm and σ = 7.7 cm for men, and μ = 163 cm and σ = 7.3 cm for women.
In order to join Blue Man Group, you have to be male between 5’10” and 6’1” (see http://bluemancasting.com). What percentage of the U.S. male population is in this range? Hint: use scipy.stats.norm.cdf.

## Solution:

```python
from scipy import stats

mu = 178
sigma = 7.7

norm = stats.norm(loc=mu, scale=sigma) #normal distribution with scipy

lower = 177.8 # SI unit convert
higher = 185.4

per_lower = norm.cdf(lower) # % of men under 5'10
print('% men under 5ft10',per_lower)

per_higher = norm.cdf(higher) # % of men under 6'1
print('% of men under 6ft1:',per_higher)

print('% of men between 5ft10 and 6ft1:',per_higher-per_lower) # % of men between 5'10 and 6'1
```
## Results/meaning:

Roughly one third of men in the US are eligible to join Blue Man Group based on height, drumming ability notwithstanding.