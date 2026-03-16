## Definition
Suppose we have two [[Random Variables|random variables]] $X:\Omega_{1}\to \mathbb{R}$ and $Y:\Omega_{2}\to \mathbb{R}$, a coupling of $X$ and $Y$ is a pair of random variables $\tilde{X}:\tilde{\Omega}\to \mathbb{R}$ and $\tilde{Y}:\tilde{\Omega}\to \mathbb{R}$ on the same probability space $\tilde{\Omega}$ such that $\tilde{X}=X$ in distribution and $\tilde{Y}=Y$ in distribution
## Example
Suppose we have a fair dice $D$ (taking values in $\left\{ 1,2,\dots,6 \right\}$) and a fair coin $C$ (taking values in $\left\{ H,T \right\}$), then we can couple them so that the dixce is equal to $1,2,3$ if and only if the coin is equal to $H$, so do this, take $\tilde{D}=D$ and
$$
\tilde{C}=\begin{cases}
H & \tilde{D}=1,2,3 \\
T & \tilde{D}=4,5,6
\end{cases}
$$
Then clearly $\tilde{D}=D$ in distribution, and $\tilde{C}=C$ in ditribution
___
Suppose that
$$
(X_{1},X_{2},X_{3})=\begin{cases}
(1,1,2) & \text{with probability }\frac{1}{3} \\
(1,1,3) & \text{with probability } \frac{1}{6} \\
(1,3,3) & \text{with probability } \frac{1}{2}
\end{cases}
$$
$$
 (Y_{1},Y_{2},Y_{3})=\begin{cases}
(1,1,3) & \text{with probability }\frac{1}{2} \\
(1,3,5) & \text{with probability } \frac{1}{2}
\end{cases}
$$
Then define $(\tilde{X}_{1},\tilde{X}_{2},\tilde{X}_{3})=(X_{1},X_{2},X_{3})$ and 
$$
(\tilde{Y}_{1},\tilde{Y}_{2},\tilde{Y}_{3})=\begin{cases}
(1,1,3) & \text{ if }(X_{1},X_{2},X_{3})=(1,1,2)\text{ or }(1,1,3) \\
(1,3,5) & \text{if }(X_{1},X_{2},X_{3})=(1,3,5)
\end{cases}
$$
We see that this is a coupling of $X$ and $Y$
Observe that under this coupling $\tilde{X}_{n}\leq \tilde{Y}_{n}$. We will use couplings of Markov chains to establish relationships between them