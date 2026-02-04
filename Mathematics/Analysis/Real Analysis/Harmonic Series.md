This is the [[Series|Series]]:
$$
\sum_{k=1}^{\infty} \frac{1}{k}
$$
Note $\frac{1}{k}\to0$, but as we shall see, $s_{n}$ is unbounded
Look at the summands:
$$
s_{1}=1
$$
$$
 s_{2}=1+\frac{1}{2}=\frac{3}{2}
$$
$$
 s_{4}=1+\frac{1}{2}+\frac{1}{3}+\frac{1}{4}\geq 1+\frac{1}{2}+\left( \frac{1}{4}+\frac{1}{4} \right)=1+\frac{1}{2}+\frac{1}{2}=1+2\times \frac{1}{2}
$$
$$
s_{8}=1+\frac{1}{2}+\underbrace{ \frac{1}{3}+\frac{1}{4} }_{ \geq \frac{1}{2} }+\underbrace{ \frac{1}{5}+\frac{1}{6}+\frac{1}{7}+\frac{1}{8} }_{ \geq \frac{1}{2} }\geq 1+3\times \frac{1}{2}
$$
So
$$
s_{2^{n}}\geq 1+n\times \frac{1}{2}
$$
So there is a [[Subsequences|subsequence]] of partial sums which diverges, so the sequence of partial sums is divergent, so the harmonic series is divergent

#Mathematics #Analysis 