A useful tool for finding stationary measures and [[Invariant Distributions|distributions]] is the following
## Definition
$\lambda$ and $P$ are in detailed balance if
$$
\lambda_{i}P_{ij}=\lambda_{j}P_{ji}~\forall i,j\in  I
$$
## Lemma
If $\lambda$ is in detailed balance with $P$, then $\lambda$ is invariant for $P$
### Proof
We have
$$
\lambda_{i}P_{ij}=\lambda_{j}P_{ji}
$$
Now taking the sum of both sides over $j$,
$$
\lambda_{i}\underbrace{ \sum_{j\in  I}P_{ij} }_{ =1 }=\sum_{j\in  I}\lambda_{j}P_{ji} 
$$
$$
\implies \lambda_{i}=\sum_{j\in  I}\lambda_{j}P_{ji}
$$
## Example
We suppose we have a random walk on $\left\{ 1,2,3,4,5 \right\}$ wherein at each time step we jump to one of the adjoining vertices chosed independently and uniformly at random a depicted below:
![[Pasted image 20260323161252.png]]
We now solve the detailed balance equations:
$$
\lambda _\text{corner}\times \frac{1}{3} = \lambda _\text{corner}\times \frac{1}{3} 
$$
$$
 \lambda _\text{corner }\times \frac{1}{3}=\lambda _\text{centre}\times \frac{1}{4}
$$
this means that $\lambda_{1}=\lambda_{2}=\lambda_{3}=\lambda_{4}$, while $\lambda_{5}=\frac{4}{3}\lambda_{1}$, soo
$$
\lambda=\begin{pmatrix}
\frac{3}{16} & \frac{3}{16} & \frac{3}{16} & \frac{3}{16} & \frac{1}{4}
\end{pmatrix}
$$
Therefore this is the unique stationary distribution, and the mean return times are given by
$$
\begin{pmatrix}
m_{1} & m_{2} & m_{3} & m_{4} & m_{5}
\end{pmatrix}=\begin{pmatrix}
\frac{16}{3} & \frac{16}{3} & \frac{16}{3} & \frac{16}{3} & 4
\end{pmatrix}
$$
___
## On General Graphs
This is in fact a big class of examples