## Theorem
Suppose $f,g$ are holomorphic on and inside a simple closed contour $\gamma$, if $\left| f(z)-g(z) \right|<\left| g(z) \right|$ for all $z\in \gamma$, then $f$ and $g$ have the same number of zeros inside $\gamma$
### Proof
First note that for the analogy to work, we need no zeros to lie on $\gamma$
But if $z_{0}\in \gamma$ is such that $f(z_{0})=0$, then $\left| g(z_{0}) \right|>\left| f(z_{0})-g(z_{0}) \right|=\left| g(z_{0}) \right|$
If $z_{0}\in \gamma$ is such that $g(z_{0})=0$, then $\left| f(z_{0}) \right|=\left| f(z_{0})-g(z_{0}) \right|<\left| g(z_{0}) \right|=0$
So $f$, g have no zeros on $\gamma$ itself.
We aim to show that $z_{f}=z_{g}$ or that $z_{f}-z_{g}=0$ where $z_{f}$ is the sum of the orders of the zeros of $f$ inside $\gamma$
So by the Argument principle,
$$
z_{f}-z_{g}=\frac{1}{2\pi i} \oint_{\gamma} \frac{f'(z)}{f(z)}~dz-\frac{1}{2\pi i} \oint_{\gamma} \frac{g'(z)}{g(z)}~dz 
$$
$$
=  \frac{1}{2\pi i} \oint_{\gamma} \frac{f'(z)g(z)-f(z)g'(z)}{f(z)g(z)}~dz = \frac{1}{2\pi i} \oint_{\gamma} \frac{h'(z)}{h(z)}~dz = z_{h}-p_{h}=I_{\Gamma_{h}}(0)
$$
So we just need to show that $\Gamma_{h}$ doesn't wind around zero at all

