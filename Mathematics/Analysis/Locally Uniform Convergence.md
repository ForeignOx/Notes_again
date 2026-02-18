While [[uniform convergence|uniform convergence]] seems attractive, it is fairly restrictive and is usually more than we need to pass topological notions from a [[sequences of functions|sequence of functions]] to the [[limit|limit]]
## Example
We have seen that the sequence of functions $f_{n}(z)=z^{n}$ converges pointwise on $\mathbb{D}$ to the function $f(z)=0$. While the limit function is [[Continuity|continuous]], the convergence to it is not uniform
To show this we can simply approach the "problematic point" $z=1$ in our domain. Indeed, by considering the sequence $z_{n}=\left( \frac{1}{2} \right)^{\frac{1}{n}}\in \mathbb{D}$, we find that
$$
\left| f_{n}(z_{n})-f(z_{n}) \right| =\frac{1}{2}
$$
Which implies, according to the [[Weierstrass M-test|Weierstrass M-test]] that $f$ doesn't converge uniformly to $f$ on $\mathbb{D}$
The main reason the uniform convergence fails here is that uniform convergence on a domain $D$ automatically takes the boundary of $D$ into account. This is shown in the above example by the fact that we approach the problematic boundary point $z=1$, from within
If we are interested in passing local properties, such as continuity, to limit functions, we need to refine our notion of uniform convergence to be one that is measured locally and not globally
## Definition
Let $D\subseteq \mathbb{C}$ be a given set and let $\left\{ f_{n} \right\}_{n\in\mathbb{N}}:D\to \mathbb{C}$ be a  sequence of functions. We say that $\left\{ f_{n} \right\}_{n\in\mathbb{N}}$ converges locally uniformly to the limit function $f$ on $D$, if for every $z_{0}\in D$ there exists an [[Open Sets|open set]] $U_{z_{0}}\subset \mathbb{C}$ (that can depend on $z_{0}$) which contains $z_{0}$ such that $\left\{ f_{n} \right\}_{n\in\mathbb{N}}$ converges uniformly to $f$ on $U_{z_{0}}\cap D$
## Remark
We need to deal with $U_{z_{0}}\cap D$ to make sure we take into account all the different types of points in $D$ (interior and boundary)
___
A simplified version of local uniform convergence for open sets:
In the case where $D\subseteq \mathbb{C}$ is an open set, the sequence $\left\{ f_{n} \right\}_{n\in\mathbb{N}}:D\to \mathbb{C}$ will converge locally uniformly on $D$ to $f$ if and only if for every $z_{0}\in D$ there exists an open set $U_{z_{0}}\subset \mathbb{C}$ (that can depend on $z_{0}$) which contains $z_{0}$ such that $\left\{ f_{n} \right\}_{n\in\mathbb{N}}$ converges uniformly on $U_{z_{0}}$ to $f$
## Example
Show that the sequence of functions $f_{n}(z)=z^{n}$ converges locally uniformly to $f(z)=0$ on $\mathbb{D}$
We claim that it is enough to show that $f_{n}(z)$ converges to $f(z)$ uniformly on $B_{r}(0)$, where $0<r<1$ which is a family of open sets in $\mathbb{D}$ such that any $z_{0}\in \mathbb{D}$ belongs to one of these sets
Indeed, given $z_{0}\in \mathbb{D}$, $z_{0}\in B_{\frac{\left| z_{0} \right|+1}{2}}(0)\subset \mathbb{D}$
On $B_{r}(0)$,
$$
\left| f_{n}(z)-f(z) \right| =\left| z \right| ^{n}\leq r^{n}=s_{n}
$$
So $s_{n}>0$, and $s_{n}$ goes to zero independently of $z$
By our theorem, $f_{n}(z)$ converges to $f(z)$ uniformly on $B_{r}(0)$, $0<r<1$
Note that the open set we chose for $z_{0}$ depended on $z_{0}$, indeed, the closer $z_{0}$ is to the boundary, the closer $r$ gets to $\hspace{0pt}1$, and consequently, the slower $\sup_{z\in B_{r}(0)}\left| f_{n}(z)-0 \right|$ converges to 0
The notion of local uniform convergence is enough to preserve continuity
## Theorem
Let $\left\{ f_{n} \right\}_{n\in\mathbb{N}}:D\to \mathbb{C}$ be a sequence of continuous functions that converges locally uniformly to a limit function $f$ on $D$. Then $f:D\to \mathbb{C}$ is continuous on $D$
### Proof
Let $z_{0}\in D$ be given, then there exists an open set $U_{z_{0}}\subseteq D$ such that $z_{0}\in U_{z_{0}}$ and $\left\{ f_{n} \right\}_{n\in\mathbb{N}}$ converges uniformly to $f$ on $U_{z_{0}}\cap D$
This implies that $f$ is continuous on $U_{z_{0}}\cap D$ and in particular, it is continuous at $z_{0}$
Since $z_{0}$ was arbitrary, we conclude the continuity of $f$ on $D$
___
We can recast all our uniform convergence criteria to local uniform convergence:
## Lemma: Criteria for Local Uniform Convergence and Lack Thereof for Sequences
Let $\left\{ f_{n} \right\}_{n\in\mathbb{N}}:D\to \mathbb{C}$ be a sequence of functions converging pointwise toa  limit function $f$ on $D$
- If for any $z_{0}\in D$, there exist an open set $U_{z_{0}}\subset D$ which contains $z_{0}$, a non-negative sequence of real numbers $\left\{ s_{n}(U_{z_{0}}) \right\}_{n\in\mathbb{N}}$ that converges to zero and $n_{0}(U_{z_{0}})\in \mathbb{N}$ that may depend on $U_{z_{0}}$ (but not on $z\in U_{z_{0}}$) such that for all $n\geq n_{0}(U_{z_{0}})$,
$$
\left| f_{n}(z)-f(z) \right| \leq s_{n}(U_{z_{0}})~\forall z\in  U_{z_{0}}\cap D
$$
    Then the sequence of functions $\left\{ f_{n} \right\}_{n\in\mathbb{N}}$ converges locally uniformly to $f$ on $D$
- If there exist a non-negative sequence of real numbers $\left\{ s_{n} \right\}_{n\in\mathbb{N}}$ that converge to $c>0$, $n_{0}\in \mathbb{N}$ (independent of $z$), and a sequence $\left\{ z_{n} \right\}_{n\in\mathbb{N}}\subset D$ that converges to $z_{0}\in D^{0}$ such that for all $n\geq n_{0}$,
$$
\left| f_{n}(z_{n})-f(z_{n}) \right|\geq s_{n} 
$$
    Then the sequence of functions $\left\{ f_{n} \right\}_{n\in\mathbb{N}}$ does not converge locally uniformly to $f$ on $D$
## Remark
Note the difference in the second statemtnt and that for uniform convergence. Here we want $\left\{ z_{n} \right\}_{n\in\mathbb{N}}$ to not only be in $D$, but to converge to a point $z_{0}$ in the interior of $D$
This guarantees that we can find $\varepsilon>0$ and $n_{1}\in \mathbb{N}$ such that the open ball $B_{\varepsilon}(z_{0})$ contains $z_{0}$ and is contained in $D$, will also contain $z_{n}$ for every $n\geq n_{1}$. Consequently we see that for any $n>\max(n_{0},n_{1})$,
$$
\left| f_{n}(z_{n})-f(z_{n}) \right| \geq s_{n}~\forall z\in  B_{\varepsilon}(z_{0})
$$
which is enough to show the lack of uniform convergence in $B_{\varepsilon}(z_{0})=B_{\varepsilon}(z_{0})\cap D$
We conclude that the convergence on $D$ can't be locally uniform
