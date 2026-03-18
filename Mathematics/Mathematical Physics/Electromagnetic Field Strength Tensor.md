## Build Up
We want to rewrite our electromagnetic objects into spacetime tensors
This is not obvious as we need to package $\underline{E}$ and $\underline{B}$, which in total gives us $\hspace{0pt}6$ components
We start by remembering that we can always write
$$
\underline{E}=-\underline{\nabla } \varphi-\partial_{t} \underline{A}
$$
$$
 \underline{B}=\underline{\nabla} \times \underline{ A} 
$$
And gauge invariance leaves $\underline{E}$ and $\underline{B}$ invariant:
$$
\varphi\to \varphi-\partial_{t}\chi 
$$
$$
 \underline{A}\to \underline{A}+\underline{\nabla } \chi
$$
It is natural to combine $\varphi$ and $\underline{A}$ into a spacetime vector:
$$
A^{\mu}=\begin{pmatrix}
\frac{\varphi}{c} \\
\underline{A}
\end{pmatrix}
$$
But the key thing is that we need to show this preserves gauge symmetry
So we need to choose $A_{\mu}$ so that our gauge transformations are tensorial operations, more precisely, the dual covector is the Gauge field:
$$
A_{\mu}=\eta_{\mu \nu}A^{\mu}=\begin{pmatrix}
-\frac{\varphi}{c} \\
\underline{A}
\end{pmatrix}
$$
How does $A_{\mu}$ transform under a gauge transformation?
$$
A_{0}=-\frac{\varphi}{c},A_{i}=(\underline{A})_{i},~i \in \left\{ 1,2,3 \right\}
$$
So
$$
A_{0}'=-\frac{1}{c}(\varphi-\partial_{t}\chi)=-\frac{1}{c}\varphi+\frac{1}{c} \frac{ \partial \chi }{ \partial t } =A_{0}+\frac{ \partial \chi }{ \partial x^{0} } =A_{0}+\partial_{0}\chi
$$
Now for the spatial component:
$$
A_{i}'=(\underline{A}+\underline{\nabla } \chi)_{i}=(\underline{A})_{i}+\partial_{i}\chi=A_{i}+\partial_{i}\chi
$$
Sooo as a spacetime covector,
$$
A_{\mu}\to A_{\mu}+\partial_{\mu}\chi
$$
Since $\chi$ is a scalar function, it must be a ${0 \choose 0 }$ tensor, $\partial_{\mu}\chi$ is thus a ${0 \choose 1 }$ tensor, so this specific choice of $A_{\mu}$ combines witha  covectros $\partial_{\mu}\chi$
Now this looks nice and all, but what about $\underline{E}$ and $\underline{B}$?
Well hold your horses, first we want to construct something gauge invariant out of $A^{\mu}$, which we tart by asking what the gauge invariant quantities are? It must be a ${0 \choose 2 }$ tensor
$$
F_{\mu \nu}=\partial_{\mu}A_{\nu}-\partial_{\nu}A_{\mu}
$$
And we call $F_{\mu \nu}$ the field strength tensor. To check this being gauge invariant,
$$
A_{\mu}'=A_{\mu}+\partial_{\mu}\chi
$$
Which gives the field strength tensor:
$$
F'_{\mu \nu}=\partial_{\mu}A'_{\nu}-\partial_{\nu}A'_{\mu}=\partial_{\mu}(A_{\nu}+\partial_{\nu}\chi)-\partial_{\nu}(A_{\mu}+\partial_{\mu}\chi) 
$$
$$
= \partial_{\mu}A_{\nu}+\partial_{\mu}\partial_{\nu}\chi-\partial_{\nu}A_{\mu}-\partial_{\nu }\partial_{\mu}\chi 
$$
$$
= \partial_{\mu}A_{\nu}-\partial_{\nu}A_{\mu}+\cancelto{ 0 }{ \partial_{\mu}\partial_{\nu}\chi-\partial_{\nu}\partial_{\mu}\chi }=F_{\mu \nu}
$$
Yay
The field strength tensor is antiymmetric in its indices:
$$
F_{\mu \nu}=\partial_{\mu}A_{\nu}-\partial_{\nu}A_{\mu}=-(\partial_{\nu}A_{\mu}-\partial_{\mu}A_{\nu})=-F_{\nu \mu}
$$
This must take the form:
$$
\begin{pmatrix}
0 & a_{12} & a_{13} & a_{14} \\
-a_{12} & 0 & a_{23} & a_{24} \\
-a_{13} & a_{23} & 0 & a_{34} \\ 
-a_{14} & -a_{24} & -a_{34} & 0
\end{pmatrix}
$$
So it has $\hspace{0pt}6$ independent terms which means it carries the same amount of information with $\underline{E}$ and $\underline{B}$
Let's write out the components of $F_{\mu \nu}$, 
$$
F_{0i}=\partial_{0}A_{i}-\partial_{i}A_{0}=\frac{1}{c}\partial_{t}A_{i}+\frac{1}{c}\partial_{i}\varphi=\frac{1}{c}(\partial_{i} \varphi+\partial_{t}A_{i})=-\frac{1}{c} E_{i}
$$
Thus
$$
F_{0i}=-\frac{1}{c}E_{i}, F_{i0}=\frac{1}{c}E_{i}
$$
Next, 
$$
F_{ij}=\partial_{i}A_{j}-\partial_{j}A_{i}
$$
We know from the definition of the curl,
$$
B_{k}=\epsilon_{kmn}\partial_{m}A_{n}
$$
$$
\implies  \epsilon_{ijk}B_{k}=\epsilon_{ijk}\epsilon_{kmn}\partial_{m}A_{n} =(\delta_{im}\delta_{jn}-\delta_{in}\delta_{jm})\partial_{m}A_{n} 
$$
$$
\implies \epsilon_{ijk}B_{k}=\delta_{im}\delta_{jn}\partial_{m}A_{n}-\delta_{in}\delta_{jm}\partial_{m}A_{n} 
$$
$$
\implies \epsilon_{ijk}B_{k}=\partial_{i}A_{j}-\partial_{j}A_{i}
$$
Thus
$$
F_{ij}=\epsilon_{ijk}B_{k} 
$$
$$
\implies F_{12}=-F_{21}=B_{3}
$$
$$
F_{13}=-F_{31}=-B_{2}
$$
$$
F_{23}=-F_{32}=B_{1}
$$
So we can write this in matrix form:
$$
F_{\mu \nu}=\begin{pmatrix}
0 & -\frac{1}{c}E_{1} & -\frac{1}{c}E_{2} & -\frac{1}{c}E_{3} \\
\frac{1}{c}E_{1} & 0 & B_{3} & -B_{2} \\
\frac{1}{c}E_{2} & -B_{3} & 0 & B_{1} \\
\frac{1}{c}E_{3} & B_{2} & -B_{1} & 0
\end{pmatrix}
$$
It is also useful to compute
$$
F^{\mu \nu}=\eta^{\mu \rho}\eta^{\nu\sigma}F_{\rho\sigma}=\begin{pmatrix}
0 & \frac{1}{c}E_{1} & \frac{1}{c}E_{2} & \frac{1}{c}E_{3} \\
-\frac{1}{c}E_{1} & 0 & B_{3} & -B_{2} \\
-\frac{1}{c}E_{2} & -B_{3} & 0 & B_{1} \\
-\frac{1}{c}E_{3} & B_{2} & -B_{1} & 0
\end{pmatrix}
$$
Note this doesn't change the antisymmetry property of $F$
How do $\underline{E}$ and $\underline{B}$ transform under a Lorentz transformation?
We know how $F_{\mu \nu}$ transforms, as it is a ${0 \choose 2 }$ tensors, it must transform as such, similarly for $F^{\mu \nu }$ being a ${2 \choose 0 }$ tensor
Reading off $\underline{E}'$ and $\underline{B}'$ from the transformed strength tensor $F^{\mu'\nu'}$
Let's try a boost in the $x$-direction:
$$
\Lambda^{\alpha}~_{\beta}=\begin{pmatrix}
\gamma & -\frac{v_{x}}{c}\gamma  & 0 & 0 \\
-\frac{v_{x}}{c}\gamma & \gamma & 0 & 0 \\
0 & 0 & 1 & 0  \\
0 & 0 & 0 & 1
\end{pmatrix}
$$
So
$$
F^{\mu'\nu'}=\Lambda^{\mu}~_{\alpha}\Lambda^{\nu}~_{\beta}F^{\alpha\beta} 
$$
$$
\implies F^{\mu'\nu'}=\begin{pmatrix}
0 & \frac{E_{x}}{c} & \frac{\gamma}{c}(E_{y}-v_{x}B_{z}) & \frac{\gamma}{c}(E_{z}+v_{x}B_{y}) \\ & 0 & \gamma\left( B_{z}-\frac{v_{x}}{c^{2}}E_{y} \right) & -\gamma\left( B_{y}+\frac{v_{x}}{c^{2}}E_{z} \right) \\
 &  & 0 & B_{x}
\end{pmatrix}
$$
This tells us 
$$
E_{x}'=E_{x}
$$
$$
E_{y}'=\gamma(E_{y}-v_{x}B_{z})
$$
$$
E_{z}'=\gamma(E_{z}+v_{x}B_{y})
$$
$$
 B'_{x}=B_{x}
$$
$$
 B_{y}'=\gamma\left( B_{y}+\frac{v_{x}}{c^{2}}E_{z} \right)
$$
$$
 B_{z}'=\gamma\left( B_{z}-\frac{v_{x}}{c^{2}}E_{y} \right)
$$
So components parallel to the boost remain unchanged, and purely electric fields can appear as partly magnetic in another frame and vice versa
For a general velocity $\underline{v}$,
$$
\underline{E}_{||}'=\underline{E}_{| |}
$$
$$
\underline{E}_{\bot}'=\gamma(\underline{E}_{\bot}+\underline{v}\times \underline{B})
$$
$$
\underline{B}_{| |}'=\underline{B}_{| |}
$$
$$
 \underline{B}_{\bot}'=\gamma\left( \underline{B}_{\bot}-\frac{\underline{v}}{c^{2}}\times \underline{E} \right)
$$
