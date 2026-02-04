Let $\sum_{k=1}^{\infty} a_{k}$ be a series, we call it absolute convergent if $\sum_{k=1}^{\infty} |a_{k}|$ is convergent
## Example
$\sum_{k=1}^{\infty} \frac{(-1)^{k+1}}{k}$, for absolute convergence is $\sum_{k=1}^{\infty} \frac{1}{k}$ which is the [[Harmonic Series|harmonic series]] which is not convergent, so this series is not absolute convergent
$\sum_{k=1}^{\infty} \frac{(-1)^{k+1}}{k^{2}}$ is absolutely convergent, as $\sum_{k=1}^{\infty} \frac{1}{k^{2}}$ is convergent
## Theorem
Let $\sum_{k=1}^{\infty} a_{k}$ be absolutely convergent, then the series is convergent
### Proof 
We have $\sum_{k=1}^{\infty} |a_{k}|$ is convergent. By [[Calculus of Limits Theorem|CoLT]], $\sum_{k=1}^{\infty} 2|a_{k}|$ is convergent. We have $-|a_{k}|\leq a_{k}\leq|a_{k}|$ so $0\leq |a_{k}|+a_{k}\leq 2|a_{k}|$, which gives us a convergent series using the comparison test, $\sum_{k=1}^{\infty} (a_{k}+|a_{k}|)$ is convergent, so by CoLT, $\sum_{k=1}^{\infty} a_{k}=\sum_{k=1}^{\infty} (a_{k}+|a_{k}|)-|a_{k}|)$ is convergent
Addendum: $\sum_{k=1}^{\infty} a_{k}\leq \sum_{k=1}^{\infty} |a_{k}|$, as the LHS is the limit of the partial sums of $a_{k}$, and the same for the RHS, but also each term in the RHS is greater than or equal to that of the LHS, so yeah 

#Mathematics #Analysis #Definition #Theorem