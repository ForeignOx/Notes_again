Pearson's product-moment correlation coefficient is a measure of the linear [[Correlation]] between two variables. The coefficient, when applied to a sample, is represented by the letter $r$. When applied to a population, it is represented by the letter $\rho$. The value of the coefficient lies in the range $-1\leq r\leq 1$, where 1 represents perfect positive correlation, and -1 represents perfect negative correlation. 0 represents no correlation
## Derivation
We want to find a way to quantify correlation. It must be:
- independent of scaling/units
- it must follow the range $-1\leq r\leq 1$ where the numbers take the values as described above
- points further away from the [[Line of Best Fit]] should have a higher impact
- it must be independent of gradient
To get the moment, we find the perpendicular distance $x-\bar{x}$ and $y-\bar{y}$, to make it a product moment, we multiply these. We then sum these values and divide by the number of them and then the [[Standard Deviation]] of $x$ and $y$:
$$
r=\frac{\sum(x-\bar{x})(y-\bar{y})}{n\sigma_{x}\sigma_{y}}
$$
Since
$$
S_{xx}=\sum(x-\bar{x})^{2}
$$
and
$$
S_{xy}=\sum(x-\bar{x})(y-\bar{y})
$$
So:
$$
r=\frac{\frac{Sxy}{n}}{\sqrt{ \frac{S_{x x}}{n} }\sqrt{ \frac{S_{yy}}{n} }}
$$
$$
\implies r=\frac{S_{xy}}{\sqrt{ S_{xx}S_{yy} }}
$$
## Hypothesis Testing
### Assumptions
- The data is random on random
- The data is drawn from an (approximately) bivariate normal distribution
    - The scatter diagram is roughly elliptical
    - Data points are more concentrated at the centre
    - Data points are roughly symmetrical within the ellipse
    - Neither variable is bimodal or skewed
- The data is not non-linear
    - This can be determined visually using a scatter diagram
- There are no outliers
    - This can be determined visually using a scatter diagram
### Hypotheses
Null hypothesis:
$H_{0}: \rho=0$
The alternative hypothesis will depend on what you are testing for:
Testing for any correlation - $H_{1}:\rho\neq 0$, this will be a two-tailed test
Testing for positive correlation - $H_{1}:\rho>0$
Testing for negative correlation - $H_{1}:\rho<0$, these are both one-tailed tests
You must then write that $\rho$ is the population correlation coefficient between the two variables
### Critical Region
Anything more extreme than the critical value:
$$
|r|>\text{critical value}
$$
## Using PMCC as an Effect Size
Often it is more useful to consider the size of the correlation rather than testing whether the population correlation is non-zero. The phrase effect size is sometimes used in this context for the value of the PMCC
### Cohen's Guideline
In social sciences, Cohen's guidline is often used:
- 0.1 is a small effect size
- 0.3 is a medium effect size
- 0.5 is a large effect size

#Mathematics #Statistics