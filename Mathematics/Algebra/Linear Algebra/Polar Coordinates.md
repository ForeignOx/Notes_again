Consider [[Vectors]] in [[Vectorspace Rn|$\mathbb{R}^2$]]   
$$
v\in \mathbb{R}^2,v\neq 0
$$
![[Dot Product 2024-10-08 11.39.32.excalidraw]]
Using this diagram we can see that we can write:
$$
\underline{v}=\begin{pmatrix}
r\cos\theta\\ r\sin\theta
\end{pmatrix}
$$
Where [[Magnitude of a Vector|$r=|v|$]] and $0\leq\theta \leq 2\pi$ is the angle made by $\underline{v}$ in an anticlockwise direction with the positive real axis
If
$$
\underline{v}=\begin{pmatrix}
v_{1}\\v_{2}
\end{pmatrix}
$$
$$
r=\sqrt{ v_{1}^{2}+v_{2}^{2} }
$$
$$
\theta=\arctan\left( \frac{v_{2}}{v_{1}} \right)=\arcsin\left( \frac{v_{2}}{r} \right)
$$
But be careful with this definition of $\theta$ as the $\arctan$ function gives values between $-\pi \leq\theta \leq \pi$, and so we have to add $2\pi$ to negative values of $\theta$ given

We define $(r,\theta)\in(0,\infty)\times[0,2\pi)$ to be the unique numbers such that
$$
\underline{v}=\begin{pmatrix}
r\cos\theta\\ r\sin\theta
\end{pmatrix}
$$
We call $(r,\theta)$ the polar coordinates of $\underline{v}$
This has the problem of the angle $\theta$ being well-defined if $r=0$

#Mathematics #LinAlg 