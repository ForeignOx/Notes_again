Suppose [[Vectors|Vectors]] $\underline{u}_{1},\underline{u}_{2},\dots,\underline{u}_{k}\in\mathbb{R}^{n}$, then we say $\underline{u}_{1},\underline{u}_{2},\dots,\underline{u}_{k}$ are linearly independent iff the only solution to:
$$
\lambda_{1}\underline{u}_{1}+\dots+\lambda_{k}\underline{u}_{k}=\underline{0}
$$
Is $\lambda_{1}=\lambda_{2}=\dots=\lambda_{k}=0$ 
Another way of thinking of this is if we have a [[Matrices|matrix]] $A$:
$$
A=\begin{pmatrix}
\underline{u}_{1}&\dots&\underline{u}_{k}
\end{pmatrix}\in M_{n\times k}(\mathbb{R})
$$
Then $\underline{u}_{1},\underline{u}_{2},\dots,\underline{u}_{k}$ are linearly indepedent iff $A\underline{\lambda}=\underline{0}$, only if $\underline{\lambda}=\underline{0}$
## Linear Dependence
$\underline{u}_{1},\underline{u}_{2},\dots,\underline{u}_{k}\in\mathbb{R}^{n}$ are called linearly dependent iff they are not linearly independent
### Example
Suppse $\underline{u},\underline{v}\in\mathbb{R}^{n}$, $\underline{u}\neq  \underline{0}\neq \underline{v}$, then $\{ \underline{u},\underline{v} \}$ is linearly dependent iff $\underline{u},\underline{v}$ are multiples of each other (they are collinear)
#### Proof
$\underline{u},\underline{v}$ are linearly dependent iff $\exists\lambda,\mu \in\mathbb{R}$, where neither are $\hspace{0pt}0$ such that $\lambda \underline{u}+\mu \underline{v}= \underline{0}$
Say $\lambda \neq 0$ without loss of generality, then $\underline{u}=\left( -\frac{\mu}{\lambda} \right)\underline{v}$, also given $\underline{u}\neq 0$
## Extending Linearly Independent Sets
Suppose $\underline{u}_{1},\dots,\underline{u}_{r}\in V$ are linearly independent, and suppose $\underline{u}\in V$, [[Linear Span|$\underline{u} \not\in \text{span}< \underline{u}_{1},\dots,\underline{u}_{r} >$]], then $\{\underline{u}, \underline{u}_{1},\dots,\underline{u}_{r} \}$ is also linearly independent
This can be used to find [[Basis|bases]], but may not terminate, so is potentially not as useful as [[Linear Span#Lemma 2|this method]]  
### Proof
Suppose $\underline{u},\underline{u}_{1},\dots,\underline{u}_{r}$ are not linearly independent, then there exists not all $\lambda,\lambda_{i}\in\mathbb{R},1\leq i\leq r$ such that:
$$
\lambda \underline{u}+\lambda_{1}\underline{u}_{1}+\dots+\lambda_{r}\underline{u}_{r}=\underline{0}
$$
Then there are two possibilities
$\lambda=0$ which implies:
$$
\lambda_{1}\underline{u}_{1}+\dots+\lambda_{r}\underline{u}_{r}=\underline{0}
$$
So $\lambda_{1}=\lambda_{2}=\dots=\lambda _{r}=0$ by linear independence of $\underline{u}_{1},\dots,\underline{u}_{r}$ which is a contradiction
Or $\lambda \neq 0$ which implies:
$$
\underline{u}=\left( -\frac{\lambda_{1}}{\lambda} \right)\underline{u}_{1}+\dots+\left( -\frac{\lambda_{r}}{\lambda} \right)\underline{u}_{r}\in \text{span}< \underline{u}_{1},\dots,\underline{u}_{r} > 
$$
Which is also a contradiction
## Example
Consider vectors:
$$
\underline{u}_{1}=\begin{pmatrix}
1\\5\\-2
\end{pmatrix},\underline{u}_{2}=\begin{pmatrix}
1\\1\\2
\end{pmatrix},\underline{u}_{3}=\begin{pmatrix}
1\\-2\\5
\end{pmatrix}\in \mathbb{R}^{3}
$$
Are these linearly indipendent?
We want to solve:
$$
\lambda_{1}\underline{u}_{1}+\lambda_{2}\underline{u}_{2}+\lambda_{3}\underline{u}_{3}=\underline{0}\iff A\underline{\lambda}=\begin{pmatrix}
\underline{u}_{1}&\underline{u}_{2}&\underline{u}_{3}
\end{pmatrix}\begin{pmatrix}
\lambda_{1}\\\lambda_{2}\\\lambda_{3}
\end{pmatrix}=\underline{0}
$$
![[Linear Independence 2024-11-19 11.25.53.excalidraw]]
Since there is a row of zeros, there will be infinitely many solutions, and, in partiular, there must then be a non-zero solution, we can pick one e.g. $\lambda_{3}=4,\lambda_{2}=-7,\lambda_{1}=3$, so
$$
3\underline{u}_{1}-7\underline{u}_{2}+4\underline{u}_{3}=\underline{0}
$$
So they are not linearly independent
___
$$
\underline{v}_{1}=\begin{pmatrix}
1\\3\\1\\2
\end{pmatrix},\underline{v}_{2}=\begin{pmatrix}
2\\-1\\-5\\3
\end{pmatrix},\underline{v}_{3}=\begin{pmatrix}
1\\0\\-2\\-1
\end{pmatrix}\in \mathbb{R}^{4}
$$
Are these linearly independent?
Same process:
![[Linear Independence 2024-11-19 11.34.55.excalidraw]]
There are no free variables, so unique solution to $\lambda_{1}\underline{v}_{1}+\lambda_{2}\underline{v}_{2}+\lambda_{3}\underline{v}_{3}=\underline{0}$ hence $\underline{v}_{1},\underline{v}_{2},\underline{v}_{3}$ are linearly independent

#Mathematics #LinAlg #Definition