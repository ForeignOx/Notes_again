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
___
The new random variables don't have to be built out of the old ones at all, for instace, taking $(X_{1},X_{2},X_{3})$ and $(Y_{1},Y_{2},Y_{3})$ from above, then define $\tilde{\Omega}=\left\{ \tilde{\omega}_{1},\tilde{\omega}_{2},\tilde{\omega}_{3},\tilde{\omega}_{4},\tilde{\omega}_{5} \right\}$ and $\mathbb{P}=\left\{ \frac{1}{4},\frac{1}{12},\frac{1}{6},\frac{1}{2} \right\}$, we define
$$
(\tilde{X}_{1},\tilde{X}_{2},\tilde{X}_{3})(\tilde{\omega})=\begin{cases}
(1,1,2) & \tilde{\omega}\in \left\{ \omega_{1},\omega_{2} \right\}  \\
(1,1,3) & \tilde{\omega}=\omega_{3}  \\
(1,3,3) & \tilde{\omega}=\omega_{4}
\end{cases}
$$
$$
 (\tilde{Y}_{1},\tilde{Y}_{2},\tilde{Y}_{3})(\tilde{\omega})=\begin{cases}
(1,1,3) & \tilde{\omega}=\omega_{1} &  \\
(1,3,5) & \tilde{\omega}\in  \left\{ \omega_{2},\omega_{3},\omega_{4} \right\}
\end{cases}
$$
We have written the couplings of $X$ and $Y$ as $\tilde{X}$ and $\tilde{Y}$ to emphasise that they are in fact new random variables on a new probability space, but one often abuses the notation by simply writng them as $X$ and $Y$
___
Consider the random walk on $I=\mathbb{Z}$ with transition states:
$$
P_{ij}=\begin{cases}
\frac{2}{3}+\frac{1}{3(i+2)^{2}} & j=i+1  \\
\frac{1}{3}- \frac{2}{3(i+2)^{2}} & j=i-1 \\
0 & \text{otherwise}
\end{cases}
$$
Clearly, this is irreducible. We will use coupling to show that the corresponding [[Markov chains|Markov chain]] is [[Recurrence and Transience|transient]]
By irreducibility, we may suppose without loss of generality that the initial condition is $\hspace{0pt}0$, i.e. $\lambda(\left\{ 0 \right\})=1$
We inductively construct on the same probability space, the Markov chain $(X_{n})_{n\geq 0}$ with rate matrix $P$ and the biased random walk $(Y_{n})_{n\geq 0}$ with stochastic matrix
$$
Q_{ij}=\begin{cases}
\frac{2}{3} & j=i+1  \\
\frac{1}{3} & j=i-1 \\
0 & \text{otherwise}
\end{cases}
$$
We set $X_{0}=Y_{0}=0$, we now suppose that we have constructed $X_{0},\dots,X_{n}$ and $Y_{0},\dots,Y_{n}$
We generate independently at random the uniform random variable $U_{n}$ and set
$$
X_{n+1}=\begin{cases}
X_{n}+1 & U_{n}\leq \frac{2}{3}+ \frac{1}{3(i+2)^{2}} \\
X_{n}-1 &  \frac{2}{3}+\frac{1}{3(i+2)^{2}}<U_{n}\leq 1
\end{cases}
$$
$$
Y_{n+1}=\begin{cases}
Y_{n}+1 & U_{n}\leq \frac{2}{3} \\
Y_{n}-1 & \frac{2}{3}<U_{n}\leq 1
\end{cases}

$$
We see that this provides a coupling of $(X_{n})_{n\geq 0}$ and $(Y_{n})_{n\geq 0}$
We now want to argue that $X_{n}$geq $Y_{n}$ for all $n\geq 0$, which we will accomplish by showing that $X_{n+1}-X_{n}\geq Y_{n+1}-Y_{n}$ for all $n\geq 0$ and using that $X_{0}=Y_{0}$
Oberve that if $Y_{n+1}=Y_{n}-1$, then $X_{n+1}-X_{n}\geq -1=Y_{n+1}-Y_{n}$
If $Y_{n+1}=Y_{n}+1$, then $U_{n}\leq \frac{2}{3}\leq \frac{2}{3}+ \frac{1}{3(i+2)^{2}}$, hence $X_{n+1}=X_{n}+1$
In either case, we have $X_{n+1}-X_{n}\geq Y_{n+1}-Y_{n}$ for all $n\geq 0$ so that $X_{n}\geq Y_{n}$ for all $n$
On the other hand, we know from the strong law of large numbers that
$$
\mathbb{P}\left( \frac{Y_{n}}{n}\to \frac{1}{3}\text{ as }n\to\infty \right)=1
$$
Therefore
$$
\mathbb{P}\left( Y_{n}\geq \frac{n}{4} \text{ eventually} \right)=1
$$
Since $X_{n}\geq Y_{n}$, we must have
$$
\mathbb{P}\left( X_{n}\geq \frac{n}{4}\text{ eventually} \right)=1
$$
This implies $X_{n}$ is transient
