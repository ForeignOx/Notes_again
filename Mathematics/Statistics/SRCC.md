A calculation we can use to establish whether there is [[Association]] between two variables is Spearman's Rank Correlation Coefficient. It is a numerical representation of the relationship beetwewen the rank order of the two variables. In fact, it is the [[PMCC]] of the rankings. A test using Spearman's rank correlation coefficient investigates for a monotonic relationship between the variables. It requires no modelling assumptions. The coefficient is represented by $r_{s}$. This is applied to a sample only. The value of the coefficient satisfies $-1\leq r_{s}\leq 1$. The formula is:
$$
r_{s}=1-\frac{6\sum d_{i}^{2}}{n(n^{2}-1)}
$$
Where $d_{i}$ is the differences between the ranks
## Hypothesis Testing
### Hypotheses
$H_{0}: \text{No association between }X\text{ and }Y$
Two-tailed test:
$H_{1}: \text{Some association between }X\text{ and }Y$
Test for positive association (one-tailed):
$H_{1}: \text{Positive association between }X\text{ and }Y$
Test for negative association (one-tailed):
$H_{1}: \text{Negative association between }X\text{ and }Y$
### Critical Region
Anything more extreme than the critical value:
$$
|r_{s}|>\text{critical value}
$$

#Mathematics #Statistics