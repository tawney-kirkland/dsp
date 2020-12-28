[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

**Code**

# Compare pregnancy length (weeks) for first borns versus others
firsts = live[live.birthord == 1]
others = live[live.birthord != 1]

firsts.prglngth.mean(), others.prglngth.mean()

cohen_effect_prglngth = thinkstats2.CohenEffectSize(firsts.prglngth,others.prglngth)

# Compare weight (lbs) of first borns vs others

firsts.totalwgt_lb.mean(), others.totalwgt_lb.mean()

cohen_effect_totalwgt = thinkstats2.CohenEffectSize(firsts.totalwgt_lb,others.totalwgt.lb)

# Compare parity of highest income versus other hhs
totincr14 = resp[resp.totincr==14]
others_totincr = resp[resp.totincr!=14]

totincr14.parity.mean(), others_totincr.parity.mean()

cohen_effect_totincr_parity = thinkstats2.CohenEffectSize(totincr14.parity,others_totincr.parity)

**Results**

(38.60095173351461, 38.52291446673706)
0.028879044654449883

(7.201094430437772, 7.325855614973262)
-0.088672927072602

(1.0758620689655172, 1.2495758136665125)
-0.1251185531466061

**Explanation / Interpretation**

General commentary: Further testing would be helpful to determine the statistical signficance of the observed differences in means. To reasonably interpret these results, it would also be helpful to further interrogate the design of the study.

Pregnancy length: ~0.08 week observed difference in means for first born babies in comparison to others, with a small Cohen's D of ~0.03. 

Birth weight: ~ -0.12 lbs difference in weight of first borns (mean 7.2 lb) versus others (mean 7.3 lb), indicating that first borns may tend to weigh less than others (further testing necessary to confirm). Slightly larger (albeit still small) Cohen's D of ~ -0.09. 

Parity and hh income: ~ -0.17 difference in number of children for those in highest income group (category 14, mean of 1.1 children) versus hh in lower income groups (below category 14, mean of 1.2 children), indicating higher income households may have fewer children. Cohen's D is approximately 10 times stronger than the difference in pregnancy length (above), although still relatively small at ~ -0.13.







