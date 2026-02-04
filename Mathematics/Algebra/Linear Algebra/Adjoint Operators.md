## Definition
For a [[Linear Differential Operators|linear operator]] $\mathcal{L}$ with boundary condition associated with an [[Inner Product|inner product]] $\left< . \right>$, the adjoint operator $(\mathcal{L}^{*},BC*)$ is defined by the inner product relation:
$$
\left< \mathcal{L}y,w \right> =\left< y,\mathcal{L}^{*}w \right> 
$$
To determine the adjoint, one needs to move the derivatives of the operator from $y$ to $w$, and define adjoint boundary conditions so that all boundary terms vanish
## Example
Find the adjoint $(\mathcal{L}^{*},BC*)$ for $\mathcal{L}=\frac{d ^{2}}{dx^{2}}$ with BCs $y(a)=0,y'(b)-3y(b)=0$
So
$$
\int ^{b}_{a} wy'' \, dx =\int ^{b}_{a} y\mathcal{L}^{*}w \, dx
$$
Using [[Integration by Parts|integration by parts]], 
$$
\int ^{b}_{a} wy'' \, dx =[wy']_{a}^{b}-\int ^{b}_{a} w'y' \, dx 
$$
$$
= [wy'-w'y]_{a}^{b}+\int ^{b}_{a} yw'' \, dx 
$$
So comparison of the integrals suggests
$$
\mathcal{L}^{*}w=\frac{d ^{2}w}{dx^{2}}\implies \mathcal{L}^{*}=\frac{d^{2} }{dx^{2}}  
$$
So $\mathcal{L}$ is [[Self-Adjoint|self-adjoint]]
But for this we need the boundary terms to vanish:
$$
w(b)y'(b)-w'(b)y(b)-w(a)y'(a)+w'(a)y(a)
$$
We can use $y'(b)=3y(b)$ and $y(a)=0$:
$$
0=y(b)(3w(b)-w'(b))-w(a)y'(a)+w'(a)y(a)
$$
Which allows us to infer two boundary conditions on $w$:
- $3w(b)-w'(b)=0$
- $w(a)=0$
So the solution includes these as our $BC^{*}$
