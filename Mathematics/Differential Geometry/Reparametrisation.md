## Definition
Let $\underline{\alpha}:I\to \mathbb{R}^{n}$ be a [[Smooth Functions|smooth]], regular [[curves|curve]]. A parameter change for $\underline{\alpha}$ is a [[Functions|map]] $h:J\to I$, where $J\subset \mathbb{R}$ is an [[Open Sets|open]] [[Intervals|interval]], such that
- $h$ is smooth
- $h'(t)\neq 0$ for all $t\in J$
- $h(J)=I$
Moreover, we call $\underline{\tilde{\alpha}}=\underline{\alpha} \circ h:J\to \mathbb{R}^{n}$ a reparametrisation of $\underline{\alpha}$
Obviously, $\underline{\alpha}$ and the reparametrisation $\underline{\tilde{\alpha}}$ have the same trace. The reparametriation is orientation preserving if $h'>0$ and orientation reversing if $h'<0$
Our next aim is to show that every smooth regular curve has a unit speed reparametrisation
## Proposition
Let $\underline{\alpha}:I\to \mathbb{R}^{n}$ be a smooth regular curve, $u_{0}\in I$, and $\ell:I\to \mathbb{R}$ be defined by
$$
\ell(u)=\int_{u_{0}}^{u} \lvert \lvert \alpha u \rvert \rvert  \, dx 
$$