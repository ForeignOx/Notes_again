Given $\left\{ V,(,) \right\}$ being an [[Inner Product|inner product]] [[Inner Product Spaces|space]], and $U=\text{span}\left\{ \underline{v}_{1},\dots \underline{v}_{k} \right\}\subseteq V$, a [[Subspaces|subspace]] of [[Vectorspaces|$V$]], can we find an [[Orthonormal Vectors|orthonormal]] [[Basis|basis]] for $U$?
I.e. we can say $U=\text{span}\left\{ \underline{v}_{1},\dots,\underline{v}_{k} \right\}$ with $(\underline{v}_{i},\underline{v}_{j})=\delta_{ij}\forall i,j=1,\dots,k$ 
## Method
What we've got is 
$$
U=\text{span}\left\{ \underline{v}_{1},\dots,\underline{v}_{k} \right\}
$$
With $\underline{v}_{1},\dots,\underline{v}_{k}$ being [[Linear Independence|linearly independent]], we want 
$$
U=\text{span}\left\{ \underline{u}_{1},\dots,\underline{u}_{k} \right\}
$$
With $(\underline{u}_{i},\underline{u}_{j})=\delta_{ij}$
First, take 
$$
\underline{u}_{1}= \frac{\underline{v}_{1}}{\lvert \lvert \underline{v}_{1} \rvert \rvert }
$$
Clearly [[Norms|$\lvert \lvert \underline{u}_{1} \rvert \rvert=1$]], and $\text{span}\left\{ \underline{v}_{1} \right\}=\text{span}\left\{ \underline{u}_{1} \right\}$
Next set
$$
\underline{ \tilde{v}}_{2}=\underline{v}_{2}-(\underline{v}_{2},\underline{u}_{1})\underline{u}_{1}
$$
Then
$$
(\underline{\tilde{v}}_{2},\underline{u}_{1})=(\underline{v}_{2}-(\underline{v}_{2},\underline{u}_{1})\underline{u}_{1},\underline{u}_{1})
$$
$$
= (\underline{v}_{2},\underline{u}_{1})-(\underline{v}_{2},\underline{u}_{1})\underbrace{ (\underline{u}_{1},\underline{u}_{1}) }_{ =1 }=0
$$
Hence $\underline{\tilde{v}}\bot\underline{u}_{1}$
Note that $\underline{\tilde{v}}_{2}\neq 0$ since $\underline{\tilde{v}}_{2}\notin \text{span}\left\{ \underline{v}_{1} \right\}=\text{span}\left\{ \underline{u}_{1} \right\}$
But $\underline{\tilde{v}}_{2}$ might not have unit norm, so we fix this by setting 
$$
\underline{u}_{2}= \frac{\underline{\tilde{v}}_{2}}{\lvert \lvert \underline{\tilde{v}}_{2} \rvert \rvert }
$$
Next we consider a general step in an [[Proof by Mathematical Induction!!!!!|inductive]] method
Suppose we have constructed $\left\{ \underline{u}_{1},\dots,\underline{u}_{r} \right\}$ orthonormal with $\text{span}\left\{ \underline{u}_{1},\dots,\underline{u}_{r} \right\}=\text{span}\left\{ \underline{v}_{1},\dots,\underline{v}_{r} \right\}$
Then set
$$
\underline{\tilde{v}}_{r+1}=\underline{v}_{r+1}-(\underline{v}_{r+1},\underline{u}_{1})\underline{u}_{1}-(\underline{v}_{r+1},\underline{u}_{2})\underline{u}_{2}-\dots-(\underline{v}_{r+1},\underline{u}_{r})\underline{u}_{r}
$$
We can check that it is orthogonal to each other vector:
$$
(\underline{\tilde{v}}_{r+1},\underline{u}_{i})=(\underline{v}_{r+1},\underline{u}_{i})-(\underline{v}_{r+1},\underline{u}_{i})\underbrace{ (\underline{u}_{i},\underline{u}_{i}) }_{ =1 }=0
$$
For all $1\leq i\leq r$
Furthermore $\underline{\tilde{v}}_{r+1}\neq 0$ since $\underline{v}_{r+1}\notin \text{span}\left\{ \underline{u}_{1},\dots ,\underline{u}_{r} \right\}=\text{span}\left\{ \underline{v}_{1},\dots,\underline{v}_{r} \right\}$
So $\underline{\tilde{v}}_{r+1}\bot\underline{u}_{i}\forall i=1,\dots,r$
Then we make it a unit vector so set
$$
\underline{u}_{r+1}= \frac{\underline{\tilde{v}}_{r+1}}{\lvert \lvert \underline{\tilde{v}}_{r+1} \rvert \rvert }
$$
And then keep going provided $U$ is finite [[Dimension|dimensional]], eventually $r+1=k$ and we're done
## Conclusion
Given a finite dimensional [[Subspaces|subspace]] $\left\{ V,(,) \right\}$, one can always find an orthonomal basis. We also known what's left, perpendicular to $u$
## Examples
In $\mathbb{R}^{2}$
Suppose we have vectors $\underline{v}_{1}$ and $\underline{v}_{2}$, we start by nor malising $\underline{v}_{1}$ to get $\underline{u}_{1}$, then we subtract a component of $\underline{u}_{1}$ from $\underline{v}_{2}$ to get a vector orthogonal to $\underline{u}_{1}$, $\underline{\tilde{v}}_{2}$, finally normalise $\underline{\tilde{v}}_{2}$ to get $\underline{u}_{1}$:
![[Gran-Schmidt Procedure 2025-02-11 11.50.36.excalidraw]]
___
Let $V$ be the set of [[Continuity|continuous]] [[Functions|functions]] in the [[Intervals|interval]] $[-1,1]$; $V=C[-1,1]$ with the condition:
$$
(f,g)=\int_{-1}^{1} f(t)g(t) \, dt 
$$
Let $U=\text{span}\left\{ f_{1}(t),f_{2}(t) \right\}$ with $f_{1}(t)=1,f_{2}(t)=t^{2}$ find an orthonormal basis
Take $g_{1}=\frac{f_{1}}{\lvert \lvert f_{1} \rvert \rvert}$
$$
\lvert \lvert f_{1} \rvert \rvert ^{2}=\int _{-1}^{1}1\times 1 \, dt =2
$$
So $g_{1}=\frac{1}{\sqrt{ 2 }}$
Take $\tilde{f}_{2}=f_{2}-(f_{2},g_{1})g_{1}$:
$$
(f_{2},g_{1})=\int_{-1}^{1} \frac{t^{2}}{\sqrt{ 2 }} \, dt = \frac{\sqrt{ 2 }}{3}
$$
So
$$
\tilde{f}_{2}=t^{2}-\frac{\sqrt{ 2 }}{3} \frac{1}{\sqrt{ 2 }}=t^{2}-\frac{1}{3}
$$
Finally $g_{2}= \frac{\tilde{f}_{2}}{\lvert \lvert   \tilde{f}_{2} \rvert \rvert}$
$$
\lvert \lvert  \tilde{f}_{2} \rvert \rvert ^{2}=(\tilde{f}_{2},\tilde{f}_{2})=\int _{-1}^{1}\left( t^{2}-\frac{1}{3} \right)^{2} \, dt =\frac{8}{45}
$$
So
$$
g_{2}=\sqrt{ \frac{45}{8} }\left( t^{2}-\frac{1}{3} \right)
$$



