We can perform the Eigenfunction method if the eigenfunctions $y_{n}(x)$ exist non-trivially. We can't guarantee this in general, but or a vast and physically important family, we can. This is the Surm-Liouville family (self-adjoint second order linear operators)
The weighted Sturm-Liouville eigenvalue problem takes the form
$$
\mathcal{L}y=\lambda r(x)y
$$
Where $r(x)\geq 0$ is a weighting function, and the operator $\mathcal{L}$ is of the form
$$
\mathcal{L}y=\frac{d }{dx} \left( p(x)\frac{d y}{dx}  \right)+q(x)y,a\leq x\leq b
$$
Where $p,q,r$ are all real valued scalar functions. We can put some boundary conditions:
$$
\alpha_{1}y(a)+\alpha_{2}y'(a)=0
$$
$$
 \alpha_{3}y(b)+\alpha_{4}y'(b)
$$
Where $\alpha_{1},\dots,\alpha_{4}$ are constants
We have showed that this form is self-adjoint
We actually already have the solution to this:
$$
\mathcal{L}y=f(x)
$$

If $\mathcal{L}$ is SL, then we follow the coefficient recipe:
$$
\left< \mathcal{L}y,y_{k} \right> =\left< f,y_{k} \right> 
$$
$$
\implies \left< y,\mathcal{L}y_{k} \right> =\left< f,y_{k} \right> 
$$
$$
\implies \left< y,\lambda_{k}ry_{k} \right> =\left< f,y_{k} \right> 
$$
$$
\implies \lambda_{k}c_{k}\left< y_{k},ry_{k} \right> =\left< f,y_{k} \right> 
$$
$$
\implies c_{k}= \frac{\left< f,y_{k} \right> }{\lambda_{k}\left< y_{k},ry_{k} \right> }
$$
And the siolution is the series solution
$$
y=\sum_{k}c_{k}y_{k}
$$
## Transforming to SL Form
Take a generic second order ODE:
$$
\mathcal{L}y=a_{2}(x)y''+a_{1}(x)y'+a_{0}(x)y
$$
With $a_{2}\neq 0$ in the interval, then we can turn it into a SL operator by multiplying by an integrating factor function $\mu(x)$:
$$
\mu a_{2}(x)y''+\mu a_{1}(x)y'+\mu a_{0}(x)y
$$
Which we compare to SL form:
$$
(py')'+qy=py''+p'y'+qy\mu a_{2}(x)y''+\mu a_{1}(x)y'+\mu a_{0}y
$$
So matching coeficients we need to solve:
$$
p=\mu a_{2}
$$
$$
p'=\mu a_{1}
$$
$$
q=\mu a_{0}
$$
Which are three equations with three unknowns
Importantly our aim is to solve:
$$
\mathcal{L}y=f(x)
$$
To turn $\mathcal{L}$ to $\hat{\mathcal{L}}$ which is SL, we have multiplied by $\mu$, so we must multiply $f$ by $\mu$
$$
\implies \mu \mathcal{L}y=\mu f\text{ or }\hat{\mathcal{L}}y= \hat{f}
$$
But $y$ does not change which is very important
## Properties of SL
### Orthogonality
The associated weighted eigenvalue problem is 
$$
\hat{\mathcal{L}}y=\mu y\lambda_{n}
$$
If the solutions to this exist, then they are orthogonal:
$$
\int ^{b}_{a} y_{k}(x)y_{j}(x)r(x) \, dx =0,k\neq j
$$
### Real Eigenvalues
The functions $p,q,r$ ($r=\mu$) aare real, then taking the complex conjugate:
$$
\overline{\mathcal{L}}=\mathcal{L}
$$
$$
\implies \mathcal{L}\overline{y_{k}}=\overline{\lambda_{k}}r\overline{y_{k}}
$$
$$
\implies \left< y_{k},\mathcal{L}\overline{y}_{k} \right>=\overline{\lambda}_{k}\left< y_{k},r\overline{y_{k}} \right>  
$$
$$
\left< y_{k},\mathcal{L}\overline{y}_{k} \right>= \left< \mathcal{L}y_{k},\overline{y}_{k} \right>=\lambda_{k} \left< ry_{k},\overline{y}_{k} \right> =\lambda_{k}\left< y_{k},r\overline{y}_{k} \right>   
$$
$$
\implies \lambda_{k}=\overline{\lambda}_{k}
$$
So the $\lambda_{k}$'s are real
### Eigenfunctions
The $\left\{ y_{k} \right\}$ are a complete set, that is all $h(x)$ with $\int f^{2}r \, dx<\infty$, can be expanded as:
$$
h(x)=\sum c_{k}y_{k}(x)
$$
Which we can take an inner product with $r(x)y_{j}(x)$:
$$
\left< ry_{j},f \right> =\left< ry_{j}\sum_{k}c_{k}y_{k} \right>  =\sum_{k}c_{k}\left<  ry_{j}y_{k} \right> =c_{j}\left< ry_{j},y_{j} \right> 
$$
$$
\implies c_{j}=\frac{\int ^{b}_{a} h(x)y_{j}(x)r(x) \, dx }{\int ^{b}_{a} y^{2}_{j}(x)r(x) \, dx }
$$
They ca actually represent anything we want which is very nice
