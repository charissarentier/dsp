[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

    Code:
       
    def CohenEffectSize(group1, group2):
        """Computes Cohen's effect size for two groups.

        group1: Series or DataFrame
        group2: Series or DataFrame

        returns: float if the arguments are Series;
                 Series if the arguments are DataFrames
        """
        diff = group1.mean() - group2.mean()

        var1 = group1.var()
        var2 = group2.var()
        n1, n2 = len(group1), len(group2)

        pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
        d = diff / np.sqrt(pooled_var)
        return d

    preg = nsfg.ReadFemPreg()
    live = preg[preg.outcome == 1]

    firsts = live[live.birthord == 1]
    others = live[live.birthord != 1]

    firsts.totalwgt_lb.mean(), others.totalwgt_lb.mean()

    CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)
    
    
    Results: 
    
    mean weight (lb) of firstborns: 7.201094430437772
    mean weight (lb) of others: 7.325855614973262

    Cohen's d = -0.088672927072602006
    
    
    Explanation:
    
    The firstborns are slightly lighter than others, by ~0.12 pounds (less than two ounces), 
    which is not a huge difference, just like the difference in pregnancy length. 
    However, what is interesting, is that although the length of the pregnancies of firstborns
    is slightly longer,  their weight is less than for other newborns.
