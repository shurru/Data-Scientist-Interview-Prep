It's crucial to have an understanding of the basics of statistics for you to succeed at any data science interview. A great deal of parametric statistical testing makes some basic assumptions, most importantly that the variables are normally distributed. This is based on the Central limit theorem (CLT) which states that with a large enough sample size, the distribution of sample means are approximately normally distributed. 

1. <b> Descriptive Statistics </b>
 
Explains the basics of a distribution including: 
* Central Tendency 
  - Mean 
  - Median 
  - Mode 
* Dispersion 
  - Range (min and max of distribution) 
  - Variance or Standard Deviation (sqrt (Variance))

2. <b> p-value </b>
- Confidence that two distributions are actually different 
- Probability of rejecting the null hypothesis 
- p= 0.05 means that 5% of the time you run an experiment you get a false positive. 
- p-values don't give us an understanding of HOW different the two treatments are 
  - Does NOT give us an understanding of the effect size 
- Calculation of the p-values are the sum of 3 parts: 
	1. The probability that random chance results in the observation 
	2. The proabbility of observing something equally as rare 
	3. The probabibility of observing something even more extreme 

3. <b> Error Bars: </b>  <i> Standard deviation, Standard error, Confidence Intervals </i> 
* Standard deviation: quantifies the spread of the distribution of measurements 
	- 1 S.D on both sides covers 68% of all measurements in Gaussian 
	- 2 S.D. covers 95% of all measurements 
	- 3 S.D covers 99.7% of all measurements: Using 3 S.D. is used as a common threshold to remove outliers from the datasets

* Standard error: 
	- Quantifies the spread of the means of different measurement sets 
	- Calculate the standard deviation of the means 
	- Can be calculated from the SD -> S.E = SD/ sqrt (N) 
	- Can bootstrap to get the standard errors!! 
	- Calculate the standard error of the means or standard deviations or modes 

* Confidence Intervals: 
	- 95% CI says that it covers 95% of the means 
	- Stat tests which allow visual inspection : significant differences become easier 
	- If you have no overlap between the CI of two distributions, there is a significant difference!! 
	- Width of an interval:
		- Calculate Standard error: (SD/ sqrt (N) )
		- CI width can be 1.96* standard errors : this is our <b> margin of error </b> 
		- This will include the true proportion 95% of the time 
		- The width of your CI changes with several factors 
			- Decreases as you increase N 
			- Increases as you increase the SD 
			- Increases as your confidence level increases 
			- Increases as your significance level decreases 
