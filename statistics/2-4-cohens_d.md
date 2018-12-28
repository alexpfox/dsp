[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

Outline:

Cohen's D is an example of effect size. Other examples of effect size are: correlation between two variables, mean difference, regression coefficients and standardized test statistics such as: t, Z, F, etc. In this example, you will compute Cohen's D to quantify (or measure) the difference between two groups of data.

You will see effect size again and again in results of algorithms that are run in data science. For instance, in the bootcamp, when you run a regression analysis, you will recognize the t-statistic as an example of effect size.


Problem: 

Compute the Cohen effect size for the difference in pregnancy length for first babies and others.


Solution:

```python
# import libraries
import first
import nsfg
from math import sqrt

# Load Pregnancy Data & Create Dataframes
live = preg[preg.outcome == 1]
firsts = live[live.birthord == 1]
others = live[live.birthord != 1]

# mean
mean_live = live['totalwgt_lb'].mean()
mean_firsts = firsts['totalwgt_lb'].mean()
mean_others = others['totalwgt_lb'].mean()

# variance
var_live = live['totalwgt_lb'].var()
var_firsts = firsts['totalwgt_lb'].var()
var_others = others['totalwgt_lb'].var()

# diff
diff_lb = mean_firsts - mean_others

# diff relative to mean
diff_rel = diff_lb / mean_live

# Cohen's d
cohens_d = (diff_lb) / sqrt(var_live)
```

overall mean: 7.265628457623368  
firsts mean: 7.201094430437772  
others mean: 7.325855614973262  
overall var: 1.9832904288326532  
firsts var: 2.0180273009157768  
others var: 1.9437810258964572  
diff in weight: -0.12476118453549034  
diff relative to mean: -0.017171423678372415  
Cohen's d: -0.0885903324538168


Results/meaning:

The difference in mean weights between groups of firsts and others was -0.125lb, or ~ 2oz. This amounts to a bit less than 2% change (~ 1.7%), which is not very significant in the context of birth weight. The number of standard deviations from the mean is ~ 0.09. This is slightly off from what the author calculated, for some reason. 

