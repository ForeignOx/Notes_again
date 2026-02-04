Also known as SET, states that:
Suppose that $V$ is a [[Vectorspaces|vectorspace]] and $S=\{ \underline{v}_{1},\dots,\underline{v}_{k} \}\subseteq V$ is a [[Linear Span|spanninng]] [[Sets|set]] for $V$, $L=\{ \underline{u}_{1},\dots,\underline{u}_{l} \}$ is a [[Linear Independence|linearly independent]] set. Then there exists distinct [[Vectors|vectors]]:
$$
\underline{v}_{i_{1}},\underline{v}_{i_{2}},\dots,\underline{v}_{i_{l}}\in S
$$
Such that for each $0\leq j\leq l$ we have:
$$
(S\setminus \{ \underline{v}_{i_{1}},\dots,\underline{v}_{i_{j}} \})\cup \{ \underline{u}_{1},\dots,\underline{u}_{j} \}
$$
Is a spanning set
## Proof
[[Proof by Mathematical Induction!!!!!|Induction]] on $j$. Base case, $j=0$ is clear. So suppose we have distinct $\underline{v}_{i_{1}},\dots,\underline{v}_{i_{J}}$ such that:
$$
(S\setminus \{ \underline{v}_{i_{1}},\dots,\underline{v}_{i_{J}} \})\cup \{ \underline{u}_{1},\dots,\underline{u}_{J} \}
$$
Is spanning, since this is spanning, we have:
$$
\underline{u}_{J+1}=\sum_{\underline{w}\in S\setminus \{ \underline{v}_{i_{1}},\dots,\underline{v}_{i_{j}} \}}\lambda_{\underline{w}}\underline{w}+\sum_{k=1}^{j}\mu_{k}\underline{u}_{k}
$$
Not every $\lambda_{\underline{w}}$ can be zero, since suppose it were, then the first sum would be zero, and then since the second sum is linearly independent, then we would have a linear dependence between the $\underline{u}_{1},\dots,\underline{u}_{J+1}$. So pick a non-zero $\lambda_{\underline{v}_{i_{J+1}}}\neq 0$ to pick $i_{J+1}$, so
$$
V=\text{span}<(S\setminus \{ \underline{v}_{i_{1}},\dots,\underline{v}_{i_{J}} \})\cup \{ \underline{u}_{1},\dots,\underline{u}_{J} \}  > 
$$
$$
= \text{span}< (S\setminus \{ \underline{v}_{i_{1}},\dots,\underline{v}_{i_{J}} \})\cup \{ \underline{u}_{1},\dots,\underline{u}_{J+1} \} >  
$$
Because adding an element doesn't reduce the span, so won't affect it,
$$
=\text{span}< (S\setminus \{ \underline{v}_{i_{1}},\dots,\underline{v}_{i_{J+1}} \})\cup \{ \underline{u}_{1},\dots,\underline{u}_{J+1} \} > 
$$
We can remove $\underline{v}_{i_{J+1}}$, as
$$
\underline{v}_{i_{J+1}}\in \text{span}< (S\setminus \{ \underline{v}_{i_{1}},\dots,\underline{v}_{i_{J+1}} \})\cup \{ \underline{u}_{1},\dots,\underline{u}_{J+1} \}  > 
$$
Which we know because of the non-zero $\lambda_{\underline{v}_{i_{J+1}}}$, so we can remove it
So verified for $J+1$
## Corollary
$k\geq l$, so any linearly independent set has as many or fewer vectors than a spanning set
## Corollary
In a finite dimensional vectorspace, every [[Basis|basis]] has the same [[Cardinality of Sets|cardinality]]
### Proof
If $A=\{ \underline{a}_{1},\dots,\underline{a}_{r} \}$ and $B=\{ \underline{b}_{1},\dots,\underline{b}_{s} \}$ are two bases for $V$, then $r\geq s$ since $A$ is spanning and $B$ is linearly independent, also $s\geq r$, since $B$ is spanning and $A$ is linearly independent, so $r=s$

#Mathematics #LinAlg #Theorem 