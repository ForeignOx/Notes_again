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
=  \frac{1}{2\pi i} \oint_{\gamma} \frac{f'(z)g(z)-f(z)g'(z)}{f(z)g(z)}~dz  = \frac{1}{2\pi i} \oint_{\gamma} \frac{ \frac{f'(z)}{g(z)}-\frac{f(z)g'(z)}{g(z)^{2}}}{\frac{f(z)}{g(z)}}
$$
$$
 = \frac{1}{2\pi i} \oint_{\gamma} \frac{h'(z)}{h(z)}~dz = z_{h}-p_{h}=I_{\Gamma_{h}}(0)
$$
Where $h=\frac{f}{g}$
So we just need to show that $\Gamma_{h}$ doesn't wind around zero at all
Let's consider the quantity
$$
\left| \Gamma_{h}(t)-1 \right| =\left| h(\gamma(t))-1 \right| = \left|  \frac{f(\gamma(t))}{g(\gamma(t))} - 1 \right| =\left|  \frac{f(\gamma(t))-g(\gamma(t))}{g(\gamma(t))} \right| <1 
$$
So $\Gamma_{h}(0)=0$
## Example
$$
f(z)=z^{4}+6z+\pi
$$
How many zeros does $f$ have in $A_{1,2}(0)=\left\{ z:\middle|: 1<\left| z \right|<2 \right\}$
Set $g_{2}(z)=z^{4}$, then on $\left| z \right|=2$, we have
$$
\left| f(z)-g_{2}(z) \right| =\left| 6z+\pi \right| \leq 6\left| z \right| +\pi=12+\pi<16=2^{4}=\left| z \right| ^{4}=\left| g_{2}(z) \right| 
$$
So by Rouche's theorem, $f$ and $g_{2}$ have the same number of zeros inside $\left| z \right|=2$, so $f$ has $\hspace{0pt}4$ zeros in $\left| z \right|=2$, as that's how many $g_{2}$ has
Setting $g_{1}(z)=6z$, then on $\left| z \right|=1$, we have
$$
\left| f(z)-g_{1}(z) \right| =\left| z^{4}+\pi \right| \leq \left| z^{4}+\pi \right| =1+\pi<6=6\left| z \right| =\left| g_{1}(z) \right| 
$$
So by Rouche's theorem, $f$ has the same number of zeros insider $\left| z \right|=1$ as $g_{1}(z)$, which is 1
Soo $f$ has $4-1=3$ zeros in $A_{1,2}(0)$
___
For some $m\in \mathbb{N}$, consider the function
$$
f(z)=\cos(\pi z)-\pi^{\pi}z^{m}
$$
How many zeros does it have in the unit disc $\mathbb{D}$
Picking $g(z)=-\pi^{\pi}z^{m}$, 
$$
\left| f(z)-g(z) \right| =\left| \cos(\pi z) \right| = \left| \frac{e^{ i\pi z }+e^{ -i\pi z }}{2} \right| \leq \frac{\left| e^{ i\pi z } \right| +\left| e^{ -i\pi z } \right| }{2}
$$
Writing $z=x+iy$, when $\left| z \right|=1$, we know $-1\leq x,y\leq 1$ then
$$
\left| e^{ i\pi z } \right| =\left| e^{ i\pi(x+iy) } \right| =e^{ -y\pi }\leq e^{ \pi }
$$
And
$$
\left| e^{ -i\pi z } \right| =e^{ y\pi }\leq e^{ \pi }
$$
Sooo
$$
\left| f(z)-g(z) \right| \leq \frac{2e^{ \pi }}{2}=e^{ \pi }<\pi^{\pi}=\pi^{\pi}\left| z \right| =\left| g(z) \right| 
$$
So by Rouche's theorem, $f$ has $m$ zeros inside $\mathbb{D}$ since $g$ 
