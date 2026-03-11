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
= \eta_{\mu \nu}\Lambda^{\nu}
$$