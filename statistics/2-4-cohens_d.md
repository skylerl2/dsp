[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> from __future__ import print_function, division
>> %matplotlib inline
>> import numpy as np
>> import nsfg
>> import first
>> preg=nsfg.ReadFemPreg()
>> live=preg[preg.outcome==1]
>> firsts=live[live.birthord==1]
>> others=live[live.birthord!=1]
>> def CohenEffectSize(group1,group2):
       diff=group1.mean()-group2.mean()
       var1=group1.var()
       var2=group2.var()
       n1,n2=len(group1),len(group2)
       pooled_var=(n1 * var1 + n2 * var2)/(n1 + n2)
       d=diff/np.sqrt(pooled_var)
       return d
>> firsts.totalwgt_lb.mean(),others.totalwgt_lb.mean()
>> CohenEffectSize(firsts.totalweight_lb,others.totalweight_lb)
