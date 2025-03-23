# A/B-testing

  Below is a structured pipeline for conducting an A/B test, from experiment
  design to analysis and decision-making.  It also includes useful links and key
  statistical formulas.


## Check list

1. **Formulate Hypothesis and Choose Metrics**
    * Define the null hypothesis (H₀) and alternative hypothesis (H₁).
  
***

2. **Fix Parameters**

    * Type I Error (α): Typically set to 0.05 (5% significance level).
    * Type II Error (β): Typically set to 0.2 (80% power).
    * Minimum Detectable Effect (MDE): The smallest effect size you want to detect.
    * p-value Threshold: Usually 0.05.
*** 

3. **Determine Duration and Timing**

    * Avoid holidays or weekends to prevent skewed data.
    * Ensure the experiment runs for a sufficient number of full business cycles (e.g., weekly or monthly trends).
    * Calculate the required sample size and ensure the experiment runs long enough to collect data from the target number of users.

***

4. **A/A Test on Historical Data**

  - Objective: Validate that the system behaves as expected under the null hypothesis.
  - Check:
    * The proportion of rejected null hypotheses should be close to the chosen significance level (α).
    * p-values should be uniformly distributed.

***

5. **A/B Test on Historical Data**

  - Objective: Simulate the effect of the treatment by adding an artificial effect ([]()).
  - Check:
    * The proportion of rejected null hypotheses should be close to or greater than the chosen power (1 - β).
    * The p-value distribution should be convex (upward-sloping).

***

6. **Bootstrap Method**

 - When to Use: When the data distribution is unknown or non-parametric.
 - Decision Rule: Reject the null hypothesis if 0 is not within the confidence interval.
 - Reference: See Jupyter notebook for implementation details.


***

7. **Variance Reduction Techniques**
  - Outlier Filtering
> [!NOTE]
> Removing extreme values (outliers) that can skew the results and increase variance.


  - Stratification
> [!NOTE]
> Splitting the data into homogeneous subgroups (strata) based on specific characteristics (e.g., user demographics, behavior)


  - CUPED
> [!NOTE]
> Controlled-Experiment Using Pre-Experiment Data. A method that uses covariates to reduce variance.


***

8. **User and Ratio Metrics**

***

9. **Multiple Testing**

***

10. **Result Analysis**
