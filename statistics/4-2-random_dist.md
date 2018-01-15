[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

    Code:
    
    from __future__ import print_function, division

    %matplotlib inline

    import numpy as np

    import nsfg
    import first
    import thinkstats2
    import thinkplot

    r = np.random.random(1000)

    pmf = thinkstats2.Pmf(r)
    thinkplot.Pmf(pmf)
    thinkplot.Config(xlabel='Random variate', ylabel='PMF', xlim=[0.0,1.0], legend=False)

    cdf = thinkstats2.Cdf(r)
    thinkplot.Cdf(cdf)
    thinkplot.Config(xlabel='Random variate', ylabel='CDF', xlim=[0.0,1.0], ylim=[0.0,1.0], legend=False)
    
    
    Explanation:
    Yes the distribution is uniform. First of all, the pmf shows that each of the outcomes 
    between 0 and 1 occurs about equally often in the sample. 
    Additionally, the diagonal CDF shows that the sample's 
    percentile ranks were distributed uniformly among the population, 
    making the CDF of the percentile ranks a diagonal line.
