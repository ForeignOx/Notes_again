## Definition
A [[Sequences|sequence]] $A_{n}$ $n\geq 1$ of [[Events|events]] is increasing if $A_{n}\subseteq A_{n+1}$ for all $n$
A sequence $B_{n}$, $n\geq 1$ of events is decreasing if $B_{n}\supseteq B_{n+1}$ for all $n$
## Theorem
Let $A_{n}$ be an increasing sequence of events, set
$$
A_{\infty}=\bigcup_{n=1}^{\infty}A_{n}
$$
Which we can think of as $\lim_{ n \to \infty }A_{n}$, then
$$
\mathbb{P}(A_{\infty})=\lim_{ n \to \infty } \mathbb{P}(A_{n})
$$
Suppose $B_{n}$ are decreasing events, set
$$
B_{\infty}=\bigcap_{n=1}^{\infty}B_{n}
$$
Which we can think of as $\lim_{ n \to \infty }B_{n}$, then
$$
\mathbb{P}(B_{\infty})=\lim_{ n \to \infty } \mathbb{P}(B_{n})
$$
### Proof
Define $C_{1} = A_{1},C_{2}=A_{2}\setminus A_{1},\dots,C_{n}=A_{n}\setminus A_{n-1}$, so the $C_{n}$'s are pairwise [[Disjoint Families of Sets|disjoint]] since the $A_{n}$'s are increasing. We see that
$$
A_{n}=\bigcup_{k=1}^{n} C_{k}
$$
We claim
$$
A_{\infty}=\bigcup_{n=1}^{\infty}C_{n}
$$
And 
$$
\bigcup_{n=1}^{\infty}C_{n}\leq A_{\infty}
$$
Which is true since
$$
C_{n}\subseteq A_{n}\implies \bigcup_{n=1}^{\infty}C_{n}\subseteq \bigcup_{n=1}^{\infty}A_{n}=A_{\infty}
$$
Suppose that $\omega \in A_{\infty}$, then $\omega \in A_{n}$ for some $n$. Let $k$ be the first index such that $\omega \in A_{k}$, then $\omega \not\in A_{1},A_{2},\dots,A_{k-1}$, then
$$
\omega \in  A_{k}\setminus A_{k-1}=C_{k}
$$
Then
$$
\omega \in  \bigcup_{n=1}^{\infty}\implies A_{\infty}\subseteq C_{k}
$$
Hence $A_{\infty}=\bigcup_{n=1}^{\infty}C_{n}$
Thus
$$
\mathbb{P}(A_{\infty})=\mathbb{P}\left( \bigcup_{n=1}^{\infty}C_{n} \right)=\sum_{n=1}^{\infty} \mathbb{P}((C_{n}))
$$
$$
= \lim_{ n \to \infty } \sum_{k=1}^{n}\mathbb{P}(C_{k})
$$
$$
= \lim_{ n \to \infty } \mathbb{P}\left( \bigcup_{k=1}^{n} C_{k} \right)
$$
___
## Remark
Attempting to extend this to uncountable limits can easily lead to contradictions. Indeed, the event $(0,1]$ has probability $\hspace{0pt}1$ in $[0,1]$, while it is still an uncountable union of zero-probability events $\left\{ x \right\}$ with $x\in(0,1]$
In probability theory we only work with countable monotone limits of events. If several approximations of an event of interest are available, we will always choose one of those for which the theorem can be applied
## Example
Let $(A_{n})_{n\geq 1}$ be an arbitrary sequence of events, the union of these events can be written as a monotone increasing limit of their finite unions $B_{n}$,
$$
\bigcup_{n\geq 1}A_{n}=\bigcup_{n\geq 1}B_{n}, ~B_{n}:= \bigcup_{m=1}^{n}A_{m}
$$
Similarly, the intersection of these events can be written a a monotone decreasing limit of their finite intersections
$$
\bigcap_{n\geq 1}A_{n}=\bigcap_{n\geq 1}C_{n},~C_{n}:= \bigcap_{m=1}^{n}A_{m}
$$
In particular, $\mathbb{P}\left( \bigcup_{n\geq 1}A_{n} \right)$ and $\mathbb{P}\left( \bigcap_{n\geq 1}A_{n} \right)$ are well defined
