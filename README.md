# Instrumental Variables: Weak Instruments, Compliers and the Exclusion Restriction

## Objective

In this lab, I looked at how weak instruments affect 2SLS estimates and why IV estimates can be different from OLS.

## Methodology

- I simulated data with different instrument strengths and compared OLS with 2SLS.
- I ran 500 simulations for each instrument strength to see how the estimates changed.
- I used Card (1995) data to estimate the effect of education on wages.
- I changed the direct effect of the instrument to see how it affected the 2SLS results.
- I also wrote a 2SLS function using two OLS regressions and checked my answers with the linearmodels package.

## Key Findings

When the instrument was very weak, the median first-stage F was only 0.5. The median 2SLS estimate was 2.038, which was close to the OLS estimate of 1.998 instead of the true value of 1.0.

I also found that 21.0% of the estimates were significant, but 98.1% of those significant estimates were more than 0.5 away from the true value.

For Card's data, the first-stage F was 16.7. The OLS estimate was 0.0740 and the 2SLS estimate was 0.1323.

When I allowed the instrument to have a direct effect of 0.02 on wages, the 2SLS estimate fell to 0.0730.

My own 2SLS function gave the same results as the linearmodels package.

From this lab, I learned that a significant 2SLS result does not always mean the estimate is reliable. We also need to check the instrument strength and think about whether the exclusion restriction makes sense.
