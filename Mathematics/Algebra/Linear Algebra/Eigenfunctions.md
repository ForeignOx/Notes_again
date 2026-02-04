For a [[Linear Differential Operators|linear differential operator]], the [[Differential Equations|differential equation]]:
$$
\mathcal{L}(f(x))=\lambda f(x),\lambda \in \mathbb{R}
$$
We call such an $f(x)$ an eigenfunction of the operator $\mathcal{L}$, with [[Eigenvalues|eigenvalue]] $\lambda$
## Anaylisis of an Eigenfunction Problem
We shall study
$$
\mathcal{L}y_{i}(x)=\lambda _{i}r(x)y_{i}(x)
$$
Where $r(x)>0$ on $x\in(a,b)$
Here $y_{i}(x)$ is an eigenfunction corresponding to the [[Eigenvalues|eigenvalue]] $\lambda_{i}$. An $\mathcal{L}$ is a [[Linear Differential Operators|linear differentiable operator]] which is our equivalent of a [[Matrices|matrix]] for [[Eigenvectors|eigenvectors]] 
$\mathcal{L}$ acts on the the [[Function Spaces|function space]] of sufficiently smooth functions on $x\in[a,b]$
We take the [[Inner Product|inner product]] of a pair of [[Functions|functions]] $u(x),v(x),x\in[a,b]$ as the following:
$$
\left< u,v \right>  =\int ^{b}_{a} u(x)\overline{v(x)} \, dx 
$$
Assuming real functions, we can drop the complex conjugate
Hence, a pair of functions $u(x),v(x)$ are [[Orthogonality|orthogonal]] on $x\in[a,b]$ with weight $r(x)$ if their inner product is zero:
$$
\left< r(x)u,v \right> =\left< u,r(x)v \right>  =\int ^{b}_{a} r(x)u(x)v(x) \, dx =0
$$
It is important that this weighting is positive definite function on the domain interior. This ensures that the inner product of a function with itself is positive definite, so we can define the ength of a function
$$
\left< u,r(x)u \right> =\lvert \lvert u \rvert \rvert ^{2}>0\text{ unless }=0
$$
This is the weighted norm of the function $u$
## Proposition
Eigenfunctions of the (weighted) [[Adjoint Operators|adjoint]] problem have the same eigenvalues as the original problem:
$$
\mathcal{L}y=\lambda r(x)y\implies \exists w: \mathcal{L}^{*}w=\lambda r(x)w
$$
### Proof
From the definition of the inner product:
$$
\left< \mathcal{L}y,w \right> =\left< \lambda r(x)y,w \right> =\left< y,\lambda r(x)w \right> 
$$
$$
\left< \mathcal{L}y,w \right> =\left< y,\mathcal{L}^{*}w \right> 
$$
$$
\implies \left< y,\mathcal{L}^{*}w \right> =\left< y,\lambda rw \right> 
$$
$$
\implies \mathcal{L}^{*}w=\lambda rw
$$
## Theorem
Eigenfunctions corresponding to different eigenvalues are orthogonal to each orthers adjoint
I.e. if $\mathcal{L}y_{j}=\lambda_{j}ry_{j}$ (so from proposition above $\mathcal{L}^{*}w_{j}=\lambda_{j}rw_{j}$) and $\mathcal{L}y_{k}=\lambda_{k}ry_{k}$ then for $\lambda_{j}\neq\lambda_{k}$, we have $\left< y_{j},r(x)w_{k} \right> =0$ 
### Proof
$$
\lambda_{j}\left< y_{j},rw_{k} \right> =\left< \lambda_{j}ry_{j},w_{k} \right>
$$
$$
= \left< \mathcal{L}y_{j},wk \right> 
$$
$$
= \left< y_{j},\mathcal{L}^{*}w_{k} \right> 
$$
$$
= \left< y_{j},\lambda_{k}rw_{k} \right> 
$$
$$
= \lambda_{k}\left< y_{j},rw_{k} \right>  
$$
But by assumption $\lambda_{j}\neq \lambda _{k}$, so we need $\left< y_{j},rw_{k} \right> =0$
## Inhomogeneous Problems
Consider 
$$
\mathcal{L}u=f(x)
$$
With homogeneous BC's: $BC_{1}(a)=BC_{2}(b)=0$
Why do we care?
This is an equilibrium or steady state problem which basically says where will our full time dependent PDE will end up