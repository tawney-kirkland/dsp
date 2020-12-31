[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> REPLACE THIS TEXT WITH YOUR RESPONSE

resp = nsfg.ReadFemResp()

import thinkplot
numkdhh18 = resp[resp.numkdhh < 18]
hist_numkdhh = thinkstats2.Hist(numkdhh18.numkdhh,label='numkdhh')
thinkplot.Hist(hist_numkdhh)
thinkplot.Config(xlabel='Number kids in hh', ylabel='Count')

numkdhh_pmf = thinkstats2.Pmf(hist_numkdhh, label='actual')
biased_numkdhh_pmf = BiasPmf(numkdhh_pmf,label='observed')
thinkplot.PrePlot(2)
thinkplot.Pmfs([numkdhh_pmf, biased_numkdhh_pmf])
thinkplot.Config(xlabel='Number kids in hh', ylabel='PMF')

print('Actual mean:', numkdhh_pmf.Mean())
print('Observed mean:', biased_numkdhh_pmf.Mean())

