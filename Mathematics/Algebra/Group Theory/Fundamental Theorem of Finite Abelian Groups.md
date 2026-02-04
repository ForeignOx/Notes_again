## Theorem
If $G$ is a finite [[Abelian Groups|abelian]] [[Groups|group]], then
$$
G\cong \mathbb{Z} /a_{1} \times \mathbb{Z} /a_{2}\times\dots \times \mathbb{Z} /a_{k}
$$
Moreover if one writes $a_{i}$ such that $a_{1}|a_{2}|a_{3}|\dots|a_{k}$, then this presentation is unique
## Example
Consider the abelian group $\mathbb{Z} /4\times \mathbb{Z} /6$ we presume we can in fact write this as $\mathbb{Z} /2 \times \mathbb{Z} /12$
We know $G=(x,y)$ with $x\in \mathbb{Z} /4,y\in \mathbb{Z} /6$, let $a=(x,e),b=(e,y)$, then clearly, $G=\left< a,b \right>$ and $ab=ba$
We also have $a^{4 }=e,b^{6}=e$, soo
$$
G=\left< a,b:\middle|: ab=ba,a^{4}=e,b^{6}=e \right> 
$$
We want tofind $c,d\in G$ such that $G=\left< c,d:\middle|: cd=dc,c^{2}=e,d^{12}=e \right>$
We can write $G$ as a matrix:
$$
\begin{pmatrix}
4 & 0  \\
0 & 6
\end{pmatrix}
$$
We can use [[Gauss-Jordan Elimination|row operations]] to rewrite this as:
$$
\begin{pmatrix}
2 & 0 \\
0 & -12
\end{pmatrix}
$$
We have essentially defined $d=a^{-1}b$, then  aour new generators can be $a,d$, and then $d^{-12}=e$, and $c^{2}=e$ for $c=d^{3}a$, hence since $c^{2}=e$, we can rewrite $G$:
$$
G=\left< c,d:\middle|: cd=dc,c^{2}=e,d^{12}=e \right> 
$$
