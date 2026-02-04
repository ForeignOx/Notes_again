For a recurrence [[Sequences|sequence]] defined as so:
$$
u_{n}=a_{1}u_{n-1}+a_{2}u_{n-2}+\dots+a_{k}u_{n-k}+p(n)
$$
You must solve it in two parts, the homogeneous solution and the particular solution
## Homogeneous Solution
### Linear Algebra Derivation
Consider the homogeneous case, sart
$$
\underline{u}_{n}=\begin{pmatrix}
u_{n}\\u_{n}\\\vdots\\u_{n-k+1}
\end{pmatrix},\underline{u}_{0}=\begin{pmatrix}
u_{k-1}\\u_{k-2}\\\vdots\\u_{0}
\end{pmatrix}
$$
We construct a [[Matrices|matrix]] of coefficients to relate $\underline{u}_{n}$ to $\underline{u}_{n-1}$:
$$
\underline{u}_{n+1}=\begin{pmatrix}
a_{1}&a_{2}&\dots&a_{k-1}&a_{k}\\
1&0&\dots&0&0\\0&1&\dots&0&0\\\vdots&\vdots&\ddots&\vdots&\vdots\\0&0&\dots&1&0
\end{pmatrix}\underline{u}_{n}
$$
$$
\implies \underline{u}_{n+1}=\begin{pmatrix}
a_{1}&a_{2}&\dots&a_{k-1}&a_{k}\\
1&0&\dots&0&0\\0&1&\dots&0&0\\\vdots&\vdots&\ddots&\vdots&\vdots\\0&0&\dots&1&0
\end{pmatrix}^{n}\underline{u}_{0}
$$
$$
\underline{u}_{n+1}=A^{n}\underline{u}_{0}
$$
So we want to [[Diagonalisation|diagonalise]] our matrix $A$, we can do so by finding
$$
\det(A-tI)=\det \begin{pmatrix}
a_{1}-t&a_{2}&\dots&a_{k-1}&a_{k}\\
1&-t&\dots&0&0\\0&1&\dots&0&0\\\vdots&\vdots&\ddots&\vdots&\vdots\\0&0&\dots&1&-t
\end{pmatrix}
$$
Which gives a characteristic polynomial, which will have roots of [[Eigenvalues|eigenvalues]] $\lambda_{1},\dots,\lambda_{k}$, each with associated [[Eigenvectors|eigenvector]] $\underline{v}_{\lambda_{i}}$ so we can write
$$
A=\begin{pmatrix}
\underline{v}_{\lambda_{1}}&\underline{v}_{\lambda_{2}}&\dots&\underline{v}_{\lambda_{k}}
\end{pmatrix}\begin{pmatrix}
\lambda_{1}&0&\dots&0\\0&\lambda_{2}&\dots&0\\\vdots&\vdots&\ddots&\vdots\\0&0&\dots&\lambda_{k}
\end{pmatrix}\begin{pmatrix}
\underline{v}_{\lambda_{1}}&\underline{v}_{\lambda_{2}}&\dots&\underline{v}_{\lambda_{k}}
\end{pmatrix}^{-1}
$$



 
___
### Method
Take the homogeneous part of $u_{n}$:
$$
a_{1}u_{n-k}+a_{2}u_{n-k+1}+\dots+a_{k-1}u_{n-1}+a_{k}u_{n}=0
$$
We can convert this to an auxiliary equation:
$$
a_{1}+a_{2}m+\dots+a_{k-1}m^{k-1}+a_{k}m^{k}=0
$$
With roots $m_{1}, m_{2}, \dots, m_{k}$, then we can write the ordinal equation as:
$$
h_{n}=A_{1}m_{1}^{n}+A_{2}m_{2}^{n}+\dots+A_{k}m_{k}^{n}
$$
If there are two repeated roots, then instead of writing for example $A_{i}m_{i}^{n}+A_{j}m_{i}^{n}$, you'd write $(A_{i}+A_{j}n)m_{i}^{n}$. If there are more than two, then you'd combine them into a polynomial in terms of $n$ multiplied by $m_{i}^{n}$, where the polynomial would be of an order of one less than the number of repeated roots
If a pair of roots are complex conjugates, then instead of writing for example $A_{i}m_{i}^{n}+A_{j}(m_{i}^{*})^{n}$, we can write them in modulus argument form:
$$
A_{i}(r e^{ i\theta })^{n}+A_{j}(r e^{ -i\theta })^{n}=r^{n}(A_{i}(\cos\theta+i\sin\theta)^{n}+A_{j}(\cos\theta-i\sin\theta)^{n})
$$
$$
=r^{n}(A_{i}(\cos n\theta+i\sin n\theta)+A_{j}(\cos n\theta-i\sin n\theta))
$$
$$
=r^{n}(B_{i}\cos n\theta+B_{j}\sin n\theta)
$$
## Particular Solution
Next you consider the $f(n)$, you essentially need to find a general version of $f(n)$ and then substitute this back into the full recurrence relation by $u_{n}=f(n)$, and hence $u_{n-k}=f(n-k)$ and so on. By comparing coefficients or otherwise, the particular solution is found
Finally, sum the homogeneous and particular solutions and use the initial conditions to form a system of equations which are then used to find the solution to the recurrence relation
### $f(n)=0$
In this case no more work is needed
### $f(n)$ is a polynomial
Try a general polynomial of the same degree
### $f(n)$ is an exponential
If $f(n)=a^{n}$, try $\beta a^{n}$, unless $a$ is a root of the homogeneous part, in which case you treat it as a repeated root
### $f(n)$ is a polynomial multiplied by an exponential
Simply use a general polynomial multiplied by an exponential with the same base

#Mathematics