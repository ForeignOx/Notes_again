## Definition
Let $\underline{\alpha}:I\to \mathbb{R}^{n}$ be a [[Smooth Functions|smooth]], regular [[curves|curve]]. A parameter change for $\underline{\alpha}$ is a [[Functions|map]] $h:J\to I$, where $J\subset \mathbb{R}$ is an [[Open Sets|open]] [[Intervals|interval]], such that
- $h$ is smooth
- $h'(t)\neq 0$ for all $t\in J$
- $h(J)=I$
Moreover, we call $\underline{\tilde{\alpha}}=\underline{\alpha} \circ h:J\to \mathbb{R}^{n}$ a reparametrisation of $\underline{\alpha}$
Obviously, $\underline{\alpha}$ and the reparametrisation $\underline{\tilde{\alpha}}$ have the same trace. The reparametriation is orientation preserving if $h'>0$ and orientation reversing if $h'<0$
Our next aim is to show that every smooth regular curve has a unit speed reparametrisation
## Proposition
Let $\underline{\alpha}:I\to \mathbb{R}^{n}$ be a smooth regular curve, $u_{0}\in I$, and $\ell:I\to \mathbb{R}$ be defined by the [[arclength|arclength]]
$$
\ell(u)=\int_{u_{0}}^{u} \lvert \lvert \underline{\alpha}'(t) \rvert \rvert  \, dt 
$$
Let $J=\ell(I)\subset \mathbb{R}$, then the curve
$$
\underline{\alpha}\circ \ell ^{-1}:J\to \mathbb{R}^{n}
$$
Is of unit speed
Note that the map $\ell$ ha the following geometric meaning:
$$
\ell(u)=\begin{cases}
L(\underline{\alpha}_{[u_{0},u]}) & \text{if }u\geq u_{0} \\
-L(\underline{\alpha}_{[u,u_{0}]}) & \text{if }u\leq u_{0}
\end{cases}
$$
Unit speed curves are also called arc length parametrised curves and constant speed curves are also called proportional to arc length curves
### Proof
Let us first show that $\ell:I\to J\subset \mathbb{R}$ is invertible. We note that
$$
\ell'(u)=\lvert \lvert \underline{\alpha}'(u) \rvert \rvert >0
$$
Since $\underline{\alpha}$ is a regular curve. Therefore $\ell$ is strictly increasing, and, therefore, bijective. Then $\ell ^{-1}:J\to I$ exists by [[fundamental theorem of calculus|fundamental theorem of calculus]]. The formula for the derivative of the inverse function together with our inequality for $\ell'$ yield the following:
$$
(\ell ^{-1})'(s)=\frac{1}{\ell'(\ell ^{-1}(s))}=\frac{1}{\lvert \lvert \underline{\alpha}'(\ell ^{-1}(s)) \rvert \rvert }
$$
Letting $\underline{\beta}=\underline{\alpha}\circ \ell ^{-1}$, then by the chain rule,
$$
\underline{\beta}'(s)=(\underline{\alpha}'\circ \ell ^{-1})(s)\cdot (\ell ^{-1})'(s)= \frac{\underline{\alpha}'(\ell ^{-1}(s))}{\lvert \lvert \underline{\alpha}'(\ell ^{-1}(s)) \rvert \rvert }

$$
Thus $\lvert \lvert \underline{\beta}'(s) \rvert \rvert=1$ and $\underline{\beta}$ is a unit speed curve
___
Note that regularity is essential in the proof since, otherwise $\underline{\alpha}'(u)=0$ for some $u\in I$, which leads to diviion by zero.