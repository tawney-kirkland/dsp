[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

**Code**
```
low = dist.cdf(177.8)
high = dist.cdf(185.4)
print('Lower end:', low)
print('Higher end:', high)
print('Qualifying:', high-low)
```

**Results**

Lower end: 0.48963902786483265
Higher end: 0.8317337108107857
Qualifying: 0.3420946829459531

**Explanation / Interpretation **

Approximately 34% of US men qualify for BMG based on height