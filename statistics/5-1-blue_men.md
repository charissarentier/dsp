[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

    from __future__ import print_function, division

    import scipy.stats

    mu = 178
    sigma = 7.7
    heights = scipy.stats.norm(loc=mu, scale=sigma)
    heights.cdf(mu-sigma)
    low = heights.cdf(177.8)
    high = heights.cdf(185.4)
    print(round(((high-low)*100),1),"%")

    --> 34.2 %
