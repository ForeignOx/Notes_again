## Definition
Given a [[sets|set]] $S\subset \mathbb{C}$, we say $w\in S$ is an isolated point of $S$ if there exists $\rho>0$ such that
$$
B_{\rho}(w)\cap S=\left\{  w \right\}
$$
## Definition
If every point of $S$ is an isolated point of $S$, then we say $S$ is a discrete set
## Proposition: Principle of Isolated Zeros
Suppose [[Complex Functions|$f$]]  is [[Holomorphicity|holomorphic]] on some ball $B_{r}(a)$ and not identically zero. If $f(a)=0$, then there exists $\rho \in(0,r)$ such that
$$
f(z)\neq 0~\forall z\in  B_{\rho}(a)\setminus \left\{ a \right\}
$$
In other words, the zeros of holomorphic functions form a discrete set
### Proof
If $f(a)=0$, then by [[Order of a Zero#Lemma Holomorphic Functions have Zeros of Finite Order|this lemma]]  $z=a$ is a zero of finite order. By [[Order of a Zero#Lemma Characterisation Lemma for Zeros|this lemma]], there is a $g:B_{r}(a)\to \mathbb{C}$ such that
$$
f(z)=(z-a)^{k}g(z)~\forall z\in  B_{r}(a), g(a) \neq 0
$$
So there is $\rho>0$ such that $g\neq 0$ on $B_{\rho} (a)$ so on $B_{\rho}(a)\setminus \left\{ a \right\}$, $f(z)\neq 0$
