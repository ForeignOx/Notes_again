One thing we think about is that
$$
f(z)=\sum_{n=0}^{\infty}z^{n}
$$
Is holomorphic on $B_{1}(0)$, and is equal to $g(z)=\frac{1}{1-z}$
But $g(z)$ is defined on $\mathbb{C}\setminus \left\{ 1 \right\}$, so can we think of $g$ as a continuation of $f$??
## Definition
If [[Complex Functions|$f:U\to \mathbb{C}$]] is [[holomorphicity|holomorphic]] on an [[open sets|open set]] $U$, and if $V$ is an open set containing $U$, then a holomorphic function
$$
g:V\to \mathbb{C}
$$
Such that $g(z)=f(z)\forall z\in U$
Is called an analytic continuation of $f$ to $V$
## Lemma: Principle of Analytic Continuation
Let $f,g:D\to \mathbb{C}$ be holomorphic on a [[domains|domain]] $D$, if there exists a ball $B_{r}(a)\subset D$ on which $f(z)=g(z)$ for all $z\in B_{r}(a)$, then $f(z)=g(z)$ on $D$
### Proof
Recall, a domain is connected, so if we could write $D=U_{1}\cup U_{2}$ for disjoint open $U_{1}$ and $U_{2}$, then we must have that one of $U_{1},U_{2}$ is empty
Let $h(z)=f(z)-g(z)$ so that $h(z)=0$ on $B_{r}(a)$. We aim to show $h(z)=0$ on $D$
Let
$$
S=\left\{ z\in D:\middle|:h(z)=0 \right\}
$$
Be the set of zeros
We define sets of [[accumulation points|accumulation points]]
$$
U_{1}=\left\{ z\in  D:\middle|: z\text{ is an accumulation point of }S \right\}
$$
$$
 U_{2}=\left\{ z\in  D:\middle|: z\text{ is not an accumulation point of }S \right\}
$$
These are disjoint and $D=U_{1}\cup U_{2}$
Note $U_{1}$ is nonempty, namely $B_{r}(a)\subset U_{1}$, and $U_{1}\subset S$

We claim $U_{1}$ is open, 
We show this by picking $z\in U_{1}$, let $\varepsilon>0$ and consider $B_{\varepsilon}(z)$. Note that if $z$ is an accumulation point of zeros fo $h$, then $h(z)=0$ by continuity, one can show this using sequence definition of continuity
If $h(z)=0$, then by the [[Isolated Points|principle of isolated zeros]], there is a ball around $z$ containing no other zeros of $h$, this contradicts $h$ being an accumulation point of zeros

We next claim $U_{2}$ is open
Suppose $z\in U_{2}$, then by the principle of solated zeros or by the [[Continuous Functions are Locally Bounded|fact that continuous functions are locally bounded]], we have a ball around $z$ on which $h$ is non-zero
So this ball contains no zeros (apart from at $z$) so all pionts are not accumulation points of zeros

