[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> import numpy as np
>> import thinkstats2
>> import thinkplot
>> pmf=thinkstats2.pmf(np.random.random(1000))
>> thinkplot.pmf(pmf,linewidth=0.1)
>> cdf=thinkstats2.cdf(np.random.random(1000))
>> thinkplot.cdf(cdf)

### The distribution does appear uniform in the CDF. The PDF went wrong because it's of a continuous variable, so no two sample points are exactly the same--each comprises 0.001 of the probability, and these are each graphed as spikes.
