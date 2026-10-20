## Definition
For $n\in\mathbb{N}_{0}$, we define the standard open disc:
$$
B^{n}=\left\{ (x_{1},\dots,x_{n})\in \mathbb{R}^{n}:\middle|: x_{1}^{2}+\dots+x_{n}^{2}<1 \right\}
$$
And the standard closed disc
$$
D^{n}=\left\{ (x_{1},\dots,x_{n})\in \mathbb{R}^{n}:\middle|:x_{1}^{2}+\dots+x_{n}^{2}\leq 1 \right\}
$$
Note that the closed dic is $D(0; 1)$ if we use the metric $d_{2}$ on $\mathbb{R}^{n}$, so we get this set to be closed
The open disc is the pre-image of $[0,1)$ which is open in $[0,\infty)$
## Example
If we use the metric $d_{1}$ or $d_{\infty}$, the closed balls $D_{d_{2}}(0; 1)$ and $D_{d_{\infty}}(0;1)$ are not the same subset of $\mathbb{R}^{n}$ as $D^{n}$, but they are [[Homeomorphicity|homeomorphic]]
Define $f:D^{n}\to D_{d_{1}}(0;1)$ by
$$
h(x)=\begin{cases}
\frac{\lvert \lvert x \rvert \rvert_{2}}{\lvert \lvert x \rvert \rvert _{1}}x & x\neq 0 \\
0 & x=0
\end{cases}
$$
We need to check that this is continuous at $0$, but notice that $\lvert \lvert h(x) \rvert \rvert_{1}=\lvert \lvert x \rvert \rvert_{2}$ for all $x\in D^{n}$, so $h$ sends each $B_{d_{2}}(0;\varepsilon)$ to $B_{d_{2}}(0;\varepsilon)$ for any $\varepsilon>0$, which is the definition of continuity so that's pretty groovy
The inverse map is obtained by a similar formula, simply replacing the roles of $\lvert \lvert \cdot \rvert \rvert_{2}$ and $\lvert \lvert \cdot \rvert \rvert_{1}$ in the definition of $h$
We can similarly construct the homeomorphism between $D^{n}$ and $D_{d_{\infty}}(0; 1)$
