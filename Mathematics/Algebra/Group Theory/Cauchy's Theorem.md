## Theorem
Let $G$ be a finite [[Groups|group]], $p$ be a prime and $p\mid \left| G \right|$, then there is a [[Subgroups|subgroup]] of $G$ of order $p$
### Proof
We need to find an element $h\in G$ such that $\text{ord}(h)=p$. Then $\left| \left< h \right> \right|=p$
Consider 
$$
G^{p}=G\times G\times G\times\dots \times G=\left\{ (x_{1},x_{2},\dots ,x_{p})\mid x_{i}\in  G \right\}
$$
Define $\Omega \subseteq G^{p}$ as
$$
\Omega=\left\{ (x_{1},x_{2},\dots,x_{p})\in G^{p}\mid x_{1}x_{2}\dots x_{p-1}x_{p}=e \right\}
$$
Then $\left| \Omega \right|=\left| G \right|^{p-1}$ as for any $x_{1},\dots,x_{p-1}$ there is a unique $x_{p}$ such that the equality holds (its inverse)
We can then consider $\mathbb{Z} /p$ [[Group Action|acting]] on $\Omega$:
$$
\overline{m}(x_{1},\dots,x_{p})=(x_{m+1},x_{m+2},\dots,x_{p},x_{1},\dots,x_{m})
$$
Why is this an action?
If $x_{1}\dots x_{p}=e$, then any of its conjugations is also $e$:
$$
x_{m+1}\dots x_{p}x_{1}\dots x_{m}=\begin{pmatrix}
x_{m+1} & x_{m+2} & \dots x_{p}
\end{pmatrix}\begin{pmatrix}
x_{1} & \dots & x_{p}
\end{pmatrix}\begin{pmatrix}
x_{p}^{-1} & \dots & x_{m+1}^{-1}
\end{pmatrix}
$$
$$
= \begin{pmatrix}
x_{m+1} & \dots  & x_{p}
\end{pmatrix}\begin{pmatrix}
x_{1} & \dots & x_{p}
\end{pmatrix}\begin{pmatrix}
x_{m+1} & \dots & x_{p}
\end{pmatrix}^{-1}=e
$$
For example
$$
x_{2}x_{3}\dots x_{p}x_{1}=\begin{pmatrix}
x_{p} & x_{1}
\end{pmatrix}
$$
Finish example?
Thus $\forall(x_{1},\dots,x_{p})\in\Omega$, we have $\overline{m}(x_{1},\dots,x_{p})\in\Omega \forall \overline{m}\in\mathbb{Z} /p$ and
$$
(\overline{n}+\overline{m})(x_{1},\dots,x_{p})=(x_{n+m+1},\dots,x_{p}x_{1},\dots,x_{n+m})
$$
$$
 \overline{0}(x_{1},x_{2},\dots,x_{p})=(x_{1},x_{2},\dots x_{p})
$$
So it is an action
By the [[Orbit-Stabiliser Theorem|orbit-stabiliser theorem]], $\mathbb{Z} /p$ actos on $\Omega$ implies 
$$
\left| \text{orb}(x) \right| = \frac{\left| \mathbb{Z} /p \right| }{\left| \text{stab}(x) \right| }\forall x\in \Omega
$$
Thus $\left| \text{orb}(x) \right|=1$ or $\left| \text{orb}(x) \right|=p$ (as $p$ is prime)
Recall $\left| \Omega \right|=\left| G \right|^{p-1},p\mid \left| G \right|\implies p\mid \left| \Omega \right|$
So we want to find an $x$ such that $\left| \text{orb}(x) \right|=1$ with $x\neq e$
Observe $\left| \text{orb}(x) \right|=1 \iff x=(h,h,h, \dots,h),h\in G$ i.e. $x_{1}=x_{2}=\dots=x_{p}$, but then, by definition of $\Omega$, $h\cdot h\dots h=h^{p}=e$
So if we find an $x$ such that $\left| \text{orb}(x) \right|=1$, then we find some $h\in G$ such that $h^{p}=e$ with $h\neq e$ so $\text{ord}(h)=p$ as we wanted :)
But $(e,e,\dots e)\in \Omega,\left| \text{orb}((e,e, \dots,e)) \right|=1$, soo
$$
\left| \Omega \right| =\text{number of orbits of size 1}+p\times \text{number of orbits of size }p
$$
Thus the number of orbits of size $\hspace{0pt}1$ is divisible by $p$, so the number of orbits of size $\hspace{0pt}1$ is greater than or equal to $p$ which is greater than or equal to $\hspace{0pt}2$, so there exists an orbit of size $\hspace{0pt}1$ different from $(e,e, \dots,e)$, thus there exists an element of order $p$ in $G$ $W^{5}$ 
## Remark
Actually a much stronger statment holds, the First Sylon Theorem:
If $\left| G \right|=p_{1}^{n_{1}}p_{2}^{n_{2}}\dots p_{k}^{n_{k}}$, then for every $i\in \overline{k}$, there exists a subgroup $H_{i}\subseteq G$ such that $\left| H_{i} \right|=p_{i}^{n_{i}}$
## Proposition
Let $G$ be a group, $\left| G \right|=2p$, then either [[Cyclic Groups|$G\cong \mathbb{Z} /2p$]] or [[Dihedral Groups|$G\cong D_{p}$]]
### Proof
By Cauchy's theorem, there is $a\in G:\text{ord}(a)=2(a)=2,b\in G:\text{ord}(b)=p$
$$
\left| \left< b \right>  \right| =p,\left< b \right> \cong \mathbb{Z} /p,a\not\in  \left< b \right> =B
$$
But we know if [[Index of Groups|$[G:H]=2$]], then $H\lhd G$, so $aba\in B$, so $aba=b^{k}$ for some $k$
Then if $k=1$, then 
$$
aba=b \iff ab =ba\implies \text{ord}(ab)=\text{lcm}(\text{ord}(a),\text{ord}(b))=\text{lcm}(2,p)=2p
$$
If $k\neq 1$, then 
$$
aba=b^{k}\implies b=ab^{k}a=(aba)^{k}=(b^{k})^{k}=b^{k^{2}}
$$
$$
\implies b^{k^{2}-1}=e
$$
We know $\text{ord}(b)=p$, so $p|k^{2}-1$, so $p|(k+1)(k-1)$, so $p|k+1$ or $p|k-1$, only the latter is possible, thus
$$
G=\left< a,b\mid a^{2}=e,b^{p}=e,aba=b^{p-1} \right> 
$$
Thus $G\cong D_{p}$