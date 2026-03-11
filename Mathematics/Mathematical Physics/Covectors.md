## Use in Special Relativity
Vectors $W^{\mu}$ are objects with an "up" index, we can also define covectors $W_{\mu}$ with a down index
There is a [[Bijective Functions|bijective]] map between vectors and covectors:
$$
W_{\mu}=\eta_{\mu \nu}W^{\nu}
$$
Which is the [[Dual Space|dual]] vector
By lowering the index $\mu$
We multiply by $\eta ^{-1}$ gives us the inverse map:
$$
W^{\nu}=\eta^{\nu \mu}W_{\mu}
$$
So if 
$$
V^{\mu}\to \begin{pmatrix}
a \\
b \\
c \\
d 
\end{pmatrix},~V_{\mu}\to\begin{pmatrix}
-a \\
b \\
c \\
d
\end{pmatrix}
$$
How do covectors transform?
We know its dual vector transforms as:
$$
W_{\mu'}=\eta_{\mu \nu}W^{\nu'}=\eta_{\mu \nu}\Lambda^{\nu}_{~ ~\rho}W^{\rho}=\eta_{\mu \nu}\Lambda^{\nu}_{~ ~\rho}\delta^{\rho}_{\sigma}W^{\sigma} 
$$
$$
= \underbrace{ \eta_{\mu \nu}\Lambda^{\nu}_{~ ~\rho}\eta^{\rho\lambda} }_{ \Lambda_{\mu}^{~ ~\lambda} }\underbrace{ \eta_{\lambda\sigma}W^{\sigma}  }_{ W_{\lambda} }
$$
$$
= \Lambda_{\mu}^{~ ~\lambda}W_{\lambda}
$$
Sooo
$$
W_{\mu'}=\Lambda_{\mu}^{~ ~\nu}W_{\lambda}
$$
So covectors transform with the inverse of the Lorentz transformation. In fact, thi equation can also serve as the [[determinants|determinant]] for covectors
## Notation
We call "up" indices vector indices, and we call "down" indices co-vector indices
