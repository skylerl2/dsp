[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> from __future__ import print_function, division
>> %matplotlib inline
>> import numpy as np
>> import nsfg
>> import first
>> import thinkstats2
>> import thinkplot
>> def BiasPmf(pmf,label):
       new_pmf=pmf.Copy(label=label)
       for x,p in pmf.Items():
           new_pmf.Mult(x,x)
       new_pmf.Normalize()
       return new_pmf
>> resp=nsfg.ReadFemResp()
>> UnbiasedPmf=thinkstats2.pmf(resp.numkdhh,label='Unbiased')
>> BiasedPmf=BiasPmf(UnbiasedPmf,label='Biased')
>> thinkplot.PrePlot(2)
>> thinkplot.Pmfs([UnbiasedPmf,BiasedPmf])
>> thinkplot.config(xlabel='# Children in Household',ylabel='PMF')
>> UnbiasedPmf.mean()
>> BiasedPmf.mean()

