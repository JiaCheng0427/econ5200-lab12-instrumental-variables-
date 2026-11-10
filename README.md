Instrumental Variables: Weak Instruments, Compliers and the Exclusion Restriction

Objective

In this lab, I studied how instrument strength and the exclusion restriction affect IV estimates, and why IV results may differ from OLS.

Methodology

I simulated data with different instrument strengths and compared OLS and 2SLS estimates.

I repeated the simulation 500 times for each instrument strength to see how the results changed.

I used Card (1995) data to estimate the return to education with college proximity as an instrument.

I tested how a direct effect of the instrument on wages changes the 2SLS estimate.

I wrote my own 2SLS function using two OLS regressions and compared the results with the linearmodels package.

Key Findings

When the instrument was very weak, the median first-stage F was 0.5, and the median 2SLS estimate was 2.038, compared with the true value of 1.0 and the median OLS estimate of 1.998.

At this instrument strength, 21.0% of the estimates were statistically significant, but 98.1% of those significant estimates were more than 0.5 away from the true value.

In Card's data, the first-stage F was 16.7. The OLS estimate was 0.0740, while the 2SLS estimate was 0.1323.

When the instrument had a direct effect of 0.02 on wages, the 2SLS estimate dropped from 0.1323 to 0.0730.

My two-stage OLS function matched the linearmodels results, giving a 2SLS estimate of 0.1323 and a first-stage F of 16.7.

Overall, I learned that a significant IV estimate is not always reliable. It is important to check the first-stage results, think about who the estimate applies to, and consider whether the exclusion restriction is reasonable.
