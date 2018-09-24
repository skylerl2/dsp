[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>> import scipy.stats
>> HeightDist=scipy.stats.norm(loc=178,scale=7.7)
>> HeightDist.cdf(185.4)-HeightDist.cdf(177.8)
