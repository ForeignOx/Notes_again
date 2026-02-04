## In $\mathbb{R}$
A subset $X\subseteq \mathbb{R}$ is open if for any $c\in X$, there exists $\varepsilon>0$ (that can depend on $c$) such that
$$
(c-\varepsilon,c+\varepsilon)=\left\{ x\in  \mathbb{R}\mid \left| x-c \right| <\varepsilon \right\} 
$$
And we call the [[Intervals|interval]] $(c-\varepsilon,c+\varepsilon)$ an open ball around $c$ with radius $\varepsilon$
## In $\mathbb{C}$
### Definition
The open ball $B_{r}(z_{0})$ of radius $r$ centred at $z_{0}$ is
$$
B_{r}:= \left\{ z\in \mathbb{C}\mid \left| z-z_{0} \right| <r \right\}
$$
The closed ball $\overline{B}_{r}(z_{0})$ of radius $r$ centred at $z_{0}$:
$$
\overline{B}_{r}:=\left\{ z\in \mathbb{C}\mid \left| z-z_{0} \right| \leq r \right\}
$$
### Definition
- A subset $U\subseteq \mathbb{C}$ is open (in $\mathbb{C}$) if for every point $z_{0}\in U$, there exists $\varepsilon>0$ such that $B_{\varepsilon}(z_{0})\subset U$
- A subset $U\subseteq \mathbb{C}$ is closed in $\mathbb{C}$ if its [[Set Complement|complement]] $U^{c}:= \mathbb{C}\setminus U$ is open
### Lemma
Open balls are open
For any $z_{0}\in\mathbb{C}$ and any $r>0$, the open ball $B_{r}(z_{0})$ is an open set
![[Pasted image 20260120114251.png]]
#### Proof
Let $z\in B_{r}(z_{0})$, motivated by the fact that the distance from $z$ to the big radius is $r-\left| z-z_{0} \right|$, we define
$$
\varepsilon= \frac{r-\left| z-z_{0} \right| }{2}>0
$$
As $r>\left| z-z_{0} \right|$, so claim $B_{\varepsilon}(z)\subset B_{r}(z_{0})$
Indeed if $w\in B_{\varepsilon}(z)$
$$
\left| w-z_{0} \right| =\left| w-z+z-z_{0} \right| \leq \left|  w-z \right| +\left| z-z_{0} \right| <\varepsilon+\left| z-z_{0} \right| 
$$
$$
=  \frac{r-\left| z-z_{0} \right| }{2}+\left| z-z_{0} \right|  = \frac{r+\left| z-z_{0} \right| }{2}<r
$$
### Remark
It can also be shown that for any $z_{0}\in\mathbb{C}$ and any $r>0$, the closed ball $\overline{B}_{r}(z_{0})$ is closed in $\mathbb{C}$
### Examples
The following sets are open:
$$
\mathbb{H}_{+}=\left\{ z\in \mathbb{C}\mid \mathfrak{I}(z)>0 \right\}
$$
$$
 \mathbb{H}_{-}=\left\{ z\in \mathbb{C}\mid \mathfrak{I}(z)<0 \right\}
$$
$$
\mathbb{H}_{L}=\left\{ z\in \mathbb{C}\mid \mathfrak{R}(z)<0 \right\}
$$
$$
\mathbb{H}_{R}=\left\{ z\in \mathbb{C}\mid \mathfrak{I}(z)>0 \right\}
$$
$$
\mathbb{D}=\left\{ z\in \mathbb{C}\mid \left| z \right| <1 \right\}
$$
These are fairly clear to show, for example if we want to show
$$
\Omega_{1}=\left\{ z\in \mathbb{C}\mid \mathfrak{R}(z)>0,\mathfrak{I}(z)>0 \right\}
$$
For some point $z_{0}\in\Omega_{1}$, we care about the closest axis to define the radius of our ball, so we define
$$
\varepsilon= \frac{\min\left\{ \mathfrak{R}(z_{0}),\mathfrak{I}(z_{0}) \right\}}{2}
$$
We claim that $B_{\varepsilon}(z)\subset \Omega_{1}$, indeed, if $\omega \in B_{\varepsilon}(z_{0})$, then 
$$
\mathfrak{R}(\omega)=\mathfrak{R}(\omega-z_{0}+z_{0})=\mathfrak{R}(\omega-z_{0})+\mathfrak{R}(z_{0})
$$
$$
 \geq -\left| \omega-z_{0} \right| +\mathfrak{R}(z)>-\varepsilon+\mathfrak{R}(z)
$$
$$
=- \frac{\min\left\{ \mathfrak{R}(z_{0}),\mathfrak{I}(z_{0}) \right\}}{2}+\mathfrak{R}(z) \geq \frac{\mathfrak{R}(z_{0})}{2}>0
$$
___
## Remark
Careful!! Not all sets are open or closed:
$$
A= \left\{ z\in \mathbb{C}\mid \mathfrak{R}(z)>0,\mathfrak{I}(z)\geq 0 \right\}
$$
Indeed, $1\in A$, yet for any $\varepsilon>0$, we have $1-i\varepsilon \in B_{\varepsilon}(1)$, but $1-i\varepsilon \not\in A$
Consequenctly $B_{\varepsilon}(1)\not\subset A$ for any $\varepsilon>0$, which implies that $A$ can't be open. To show that $A$ is not closed, we notice that
$$
A^{c}=\left\{ z\in \mathbb{C}\mid \mathfrak{R}(z)\leq 0,\mathfrak{I}(z)\geq 0 \right\}\cup \left\{ z\in \mathbb{C}\mid \mathfrak{I}( z)<0 \right\}
$$
Using the same idea as above, we see that $i \in A^{c}$, but $B_{\varepsilon}(i)\not\subset A^{c}$ for any $\varepsilon>0$. This implies $A^{c}$ is not open and as such $A$ is not closed
### Lemma
Unions and intersections of open sets:
- Arbitrary unions of open sets are open; that is $\bigcup_{i\in I}U_{i}$ is open for any possibly infinite cossection of open sets $U_{i}$
- Finite intersections of open sets are open; that is $\bigcap_{i=1}^{n} U_{i}$ is open for any finite collection of open sets $U_{i}$
#### Proof
Denote $U=\bigcup_{i\in I}U_{i}$ and consider $z_{0}\in U$, there exists $i_{0}\in I$ such that $z_{0}\in U_{i_{0}}$. Since $U_{i_{0}}$ is open, there exists $\varepsilon>0$ such that $B_{\varepsilon}(z_{0})\subseteq U_{i_{0}}$. Consequently, $B_{\varepsilon}(z_{0})\subseteq U$. As $z_{0}$ was arbitrary we conclude the result
Similarly, denoting $U=\bigcap_{i=1}^{n}U_{i}$, we see that if $z_{0}\in U$, then $z_{0}\in U_{i}$ for all $i=1,\dots,n$. Since $\left\{ U_{i} \right\}_{i\in \overline{n}}$ are open, we can find $\varepsilon_{i}>0$ such that $B_{\varepsilon_{i}}(z_{0})\subseteq U_{i}$
Denote $\varepsilon=\min\left\{ \varepsilon_{1},\dots,\varepsilon_{n} \right\}>0$, we have for any $i\in\overline{n}$:
$$
B_{\varepsilon}(z_{0})\subseteq B_{\varepsilon_{i}}(z_{0})\subseteq U_{i}
$$
Which implies that $B_{\varepsilon}(z_{0})\subseteq \bigcap_{i=1}^{n}U_{i}=U$
As $z_{0}$ was arbitrary, we conclude the result
### Corollary
Unions and intersections of closed sets
- Finite unions of closed sets are closed
- Arbitrary interesections of close sets are closed
#### Proof
This follows from [[Law of De Morgan|De Morgan's laws]]:
$$
\left( \bigcup_{i\in  I}U_{i} \right)^{c}=\bigcap_{i\in  I} U_{i}^{c}
$$
$$
 \left( \bigcap_{i\in  I}U_{i} \right)^{c}=\bigcup_{i\in I}U_{i}^{c}
$$
And the previous lemma
### Remark
An infinite intersection of open sets is not necessarily open. Similarly, an infinite union of closed sets is not necessarily closed e.g. the union of closed intervals in $\mathbb{R}$.
$$
\bigcup_{n=1}^{\infty}\overline{B}_{1-\frac{1}{n}}(0)=B_{1}(0)
$$
Interestingly, there is a more natural way to associate open and closed to any given set
### Definition
- The interior $A^{0}$ of $A$ is defined by
$$
A^{0}:= \left\{ x\in  A\mid \exists \text{ open set }U\subseteq A:x\in  U \right\}
$$
- The closure $\overline{A}$ of $A$ is the complement of the interior of the complement:
$$
\overline{A}=((A^{c})^{0})^{c}=\left\{ x\in  X\mid U\cap A\neq \emptyset,~ \forall \text{ open sets } U:x\in  U \right\}
$$
- The boundary $\partial A$ of $A$ is the closure without the interior
$$
\partial A:=\overline{A}\setminus A^{0}=(A^{0})^{c}\cap((A^{c})^{0})^{c}=(A^{0}\cup (A^{c})^{0})^{c}
$$

