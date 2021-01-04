[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

**Code**

```
resp = nsfg.ReadFemResp()

import thinkplot
numkdhh_pmf = thinkstats2.Pmf(hist_numkdhh, label='numkdhh')

thinkplot.Pmf(numkdhh_pmf)
thinkplot.Config(xlabel='Number of children', ylabel='PMF')

biased_numkdhh_pmf = BiasPmf(numkdhh_pmf,label='biased')
thinkplot.PrePlot(2)
thinkplot.Pmfs([numkdhh_pmf, biased_numkdhh_pmf])
thinkplot.Config(xlabel='Number children in hh', ylabel='PMF')

print('Actual mean:', numkdhh_pmf.Mean())
print('Biased mean:', biased_numkdhh_pmf.Mean())
```

**Results**
![PMF of number of kids in household](https://github.com/tawney-kirkland/dsp/blob/master/img/3.1.1.png?raw=true)
![PMF of actual and biased number of kids in household](https://github.com/tawney-kirkland/dsp/blob/master/img/3.1.2.png?raw=true)

**Explanation / Interpretation**
Surveying a sample of children from the study results in a higher average number of children in the household, as households with no children would be excluded from the sample.

