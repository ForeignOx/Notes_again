## U substitution with ln??
If $\gamma:[a,b]\to \mathbb{C}$ is a simple closed contour, and $f$ is a holomorphic function, then $(f\circ \gamma)(t)=\Gamma_{f}(t)$ is a closed contour.
Say, we know $f$ has no zeros on $\gamma$, then $\hspace{0pt}0$ does not lie on the image contour $\Gamma_{f}$
How many times does $\Gamma_{f}$ wind around $z=0$?
$$
    I_{\Gamma_{f}}(0)=\frac{1}{2\pi i}\oint_{\Gamma_{f}} \frac{1}{z}~dz = \frac{1}{2\pi i} \int ^{b}_{a} \frac{1}{\Gamma_{f}(t)}\Gamma'_{f}(t) \, dt =\frac{1}{2\pi i} \int ^{b}_{a} \frac{(f\circ  \gamma)'(t)}{f(\gamma(t))} \, dt 
$$
$$
= \frac{1}{2\pi i} \int ^{b}_{a} \frac{f'(\gamma(t))\gamma'(t)}{f(\gamma(t))}   \, dt = \frac{1}{2\pi i} \oint_{\gamma} \frac{f'(z)}{f(z)}~dz
$$
## Example
Consider $f(z)=\frac{e^{ z }}{z}$, this has a pole at $z=0$, (of order 1), so
$$
f'(z)=\frac{e^{ z }}{z}-\frac{e^{ z }}{z^{2}}
$$
So
$$
g(z)= \frac{f'(z)}{f(z)}= \frac{\frac{e^{ z }}{z}-\frac{e^{ z }}{z^{2}}}{\frac{e^{ z }}{z}}
$$
This function $g$ has a pole at $1=\frac{1}{z}$ of order $\hspace{0pt}1$ at $z=0$
## Lemma
Suppose $f$ is meromorphic on a domain $D$, then the function $\frac{f'}{f}$ is also meromorphic on $D$ with simple poles at all points
