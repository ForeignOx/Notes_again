We have already seen that if $\left| G \right|=2$, then $G\cong \mathbb{Z} /2$, if $\left| G \right|=3$, then $G\cong \mathbb{Z}/3$ what else can we find?
## Lemma
- If [[Groups|$G$]] is [[Cyclic Groups|cyclic]] of order $n$, then $G\cong \mathbb{Z} /n$
- If $\left| G \right|=p$ for some prime $p$, then $G\cong \mathbb{Z} /p$
### Proof
For the first part $G=\left<  g \right>=\left\{ e,g,g^{2},\dots,g^{n-1} \right\}$, and $\mathbb{Z} /n=\left<  \overline{1} \right>=\left\{ \overline{0},\overline{1},\dots,\overline{n-1} \right\}$, then we can take the isomorphism:
$$
\varphi:G\to \mathbb{Z} /n,\varphi(g^{k})=\overline{k}
$$
For the second, we have $\left|  G \right|=p$, take any $g\in G$ with $g\not\in e$, consider $H=\left<  g \right>$, then $\left| H \right|\geq 2$, by [[Lagrange's Theorem|lagrange's theorem]], $\left| H \right| \mid \left| G \right|$ which implies $\left| H \right|=p$, which implies $H=G$
So $G$ is cyclic, so by the first part, $G\cong \mathbb{Z} /p$
___
We have seen several families of groups, such as cyclic groups $\mathbb{Z} /n$, [[Dihedral Groups|dihedral]] groups $D_{n}$ and [[Symmetric Groups|symmetric]] groups $S_{n}$
These in fact overlap, for example, $S_{2}\cong \mathbb{Z} /2$
There are many ways of showing these overlaps
How does one distinguish non-isomorphic gorups?
One way is to show that the orders of the element are different
## Example
Why is $\mathbb{Z} /4\not\cong \mathbb{Z} /2\times \mathbb{Z} /2$, in $\mathbb{Z} /4$, there exists an element of order $\hspace{0pt}4$, thi is not the case in $\mathbb{Z} /2\times \mathbb{Z} /2$
___
Is $\mathbb{Z} /3\times S_{3}\cong D_{9}$??
No.
___
## Showing $D_{3}\cong S_{3}$:
$$
D_{3}=\left\{ e,r,r^{2},s,rs,r^{2}s \right\}\text{ with orders }(1,3,3,2,2,2)
$$
$$
S_{3}=\left\{ e,\begin{pmatrix}
1 & 2
\end{pmatrix},\begin{pmatrix}
2&3\end{pmatrix},\begin{pmatrix}
1 & 3
\end{pmatrix},\begin{pmatrix}
1 & 2 & 3
\end{pmatrix},\begin{pmatrix}
3 & 2 & 1
\end{pmatrix} \right\}
$$
$$
\text{with orders }(1,2,2,2,3,3)
$$
### Proof
Define the isomorphism expicitly, it i sufficient to define on generators
$$
\varphi: D_{3}\to S_{3}
$$
$$
 \varphi(r)=\begin{pmatrix}
1 & 2 & 3
\end{pmatrix},\varphi(s)=\begin{pmatrix}
1 & 2
\end{pmatrix}
$$
And we can check that this works by checking $\varphi(r)^{3}=e,\varphi(s)^{2}=e,\varphi(s rs)=\varphi(r^{-1})$ 
___
Alternatively, 
