In this distribution, each of a finite number of values has an equal probability. The standard discrete uniform distribution is defined as follows:
$$
X\sim \text{Uniform}(n) \iff P(x=r)=\begin{cases}
\frac{1}{n} && r \in \{ 1,2,\dots,n \}\\
0 && \text{otherwise}
\end{cases}
$$
___
## [[Expectation]]
$$
E(X)=\sum_{ r=1} ^{ n}  rP(X=r)=\sum_{ r=1} ^{ n}  \frac{r}{n}=\frac{1}{n}\sum_{ r=1} ^{ n}  r=\frac{1}{n}\times\frac{1}{2}n(n+1)=\frac{1}{2}(n+1)
$$
___
## [[Variance]]
$$
E(X^{2})=\sum_{ r=1} ^{ n}  r^{2}P(X=r)=\sum_{ r=1} ^{ n}  \frac{r^{2}}{n}=\frac{1}{n}\sum_{ r=1} ^{ n}  r^{2}=\frac{1}{n}\times \frac{1}{6}n(n+1)(2n+1)=\frac{1}{6}(n+1)(2n+1)
$$
$$
\therefore Var(X)=E(X^{2})-(E(X))^{2}=\frac{1}{6}(n+1)(2n+1)-\frac{1}{4}(n+1)^{2}=\frac{(n+1)(4n+2-3n-3)}{12}
$$
$$
\implies Var(X)=\frac{1}{12}(n+1)(n-1)=\frac{1}{12}(n^{2}-1)
$$

#Mathematics #Statistics #Distribution