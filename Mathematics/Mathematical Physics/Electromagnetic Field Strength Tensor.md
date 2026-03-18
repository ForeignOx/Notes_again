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
Since $\chi$ is a scalar function, it must be a ${0 \choose 0 }$ tensor, $\partial_{\mu}$