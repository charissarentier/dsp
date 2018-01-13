[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

    from __future__ import print_function, division

    %matplotlib inline

    import numpy as np

    import nsfg
    import first
    import thinkstats2
    import thinkplot

    def BiasPmf(pmf, label):
        new_pmf = pmf.Copy(label=label)

        for x, p in pmf.Items():
            new_pmf.Mult(x, x)

        new_pmf.Normalize()
        return new_pmf

    resp = nsfg.ReadFemResp()

    # Pmf actual - with original data
    pmf = thinkstats2.Pmf(resp.numkdhh, label='actual')

    # Pmf biased - constructed
    biased = BiasPmf(pmf, label='biased')

    # Plot both distributions
    thinkplot.PrePlot(2)
    thinkplot.Pmfs([pmf, biased])
    thinkplot.Config(xlabel='Number of children', ylabel='PMF')

    # Compute the means
    pmf.Mean()    --> 1.024205155043831
    biased.Mean() --> 2.403679100664282
