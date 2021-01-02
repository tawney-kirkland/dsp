[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> REPLACE THIS TEXT WITH YOUR RESPONSE

**Code**
```
ex_sample = np.random.random(1000)

ex_sample_pmf = thinkstats2.Pmf(ex_sample)
thinkplot.pmf(ex_sample_pmf, linewidth=0.01)
thinkplot.Config(xlabel='Random int',ylabel='PMF')

ex_sample_cdf = thinkstats2.Cdf(ex_sample,label='random int')
thinkplot.cdf(ex_sample_cdf)
thinkplot.Config(xlabel='Random int',ylabel = 'CDF')

```

**Explanation / Interpretation**
Yes, the distribution is uniform. Noise appears in the PMF as the number of values increases because the associated probabilities become smaller. The CDF manages for this by using percentiles.