Meowmoewomeowmeowmeowmeowmeowmeowmeowmeowmeowme


## Theorem: Closed Contour Case
Let $f:U\to \mathbb{C}$ be a continuous function on an open set $U\subset \mathbb{C}$, if $f$ has a [[Holomorphicity|holomorphic]] antiderivative $F$ on $U$
Then
$$
\int _{\gamma}f(z) \, dz=0 
$$
For all closed contours $\gamma \subset U$
## Remark
Finding antiderivatives is not a trivial thing, and this is our main restriction
## Example
For $r>0$ we have for any $a\in \mathbb{C}$,
$$
\int _{\left| z-a \right| =r}(z-a)^{n} \, dz =\begin{cases}
0 & n\neq -1 \\
2\pi i & n=-1
\end{cases} 
$$
So $f(z)=\frac{1}{z}$ is holomorphic on $\mathbb{C}\setminus \left\{  0 \right\}$ but doesn't have a holomorphic antiderivative, as that would mean its integral would have to be $\hspace{0pt}0$, contradicting Newton-Leibniz
We do know that it kinda has the antiderivative $\log$, but this has the issue that the branch cut is messing things up :/