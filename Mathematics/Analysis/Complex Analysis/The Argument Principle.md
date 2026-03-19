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
Suppose $f$ is meromorphic on a domain $D$, then the function $\frac{f'}{f}$ is also meromorphic on $D$ with simple poles at all points $a\in \mathbb{C}$ at which $f$ has a zero or a pole, moreover,
$$
\mathrm{Res}_{z=a}\left( \frac{f'}{f} \right)=\begin{cases}
k & \text{if }z=a\text{ is a zero of }f\text{ of order }k \\
-k & \text{if }z=a\text{ is a pole of }f\text{ of order }k
\end{cases}
$$
### Proof
Clearly $\frac{f'}{f}$ is holomorphic everywhere except potentially places $f$ has a pole or zero or any isolated singularity
Suppose $f$ has a zero or order $k$ at $z=a$, then by the characterisation lemma,
$$
f(z)=(z-a)^{k}g(z)
$$
For some holomorphic $g$ with $g(a)\neq 0$, soo
$$
\frac{f'(z)}{f(z)}= \frac{k(z-a)^{k-1}g(z)+(z-a)^{k}g'(z)}{(z-a)^{k}g(z)}=\frac{k}{z-a}+ \frac{g'(z)}{g(z)}
$$
i.e. the principle and analytic parts, so $\frac{f'}{f}$ has a pole of orderr $\hspace{0pt}1$ at $z=a$, and $\mathrm{Res}_{z=a}\left( \frac{f'}{f} \right)=k$
Suppose instead that $f$ has a pole of order $k$ at $z=a$, then by the characterisation lemma, $f(z)=(z-a)^{-k}g(z)$ for some holomorphic $g$, with $g(a)\neq 0$, so
$$
\frac{f'(z)}{f(z)} =  \frac{-k(z-a)^{-k-1}g(z)+(z-a)^{-k}g'(z)}{(z-a)^{-k}g(z)}=-\frac{k}{z-a}+\frac{g'(z)}{g(z)}
$$
As before this is a pole of order $1$, $\mathrm{Res}_{z=a}\left( \frac{f'}{f} \right)=-k$
## Notation
Given meromorphic $f$ and simple closed contour $\gamma$, let $z_{f}$ be the sum of the orders of zeros of $f$ inside $\gamma$, and similarly, let $p_{f}$ be the sum of the orers of the poles of $f$ inside $\gamma$ (which is the number of poles of $f$ inside $\gamma$ counted with orders)
## Theorem: The Argument Principle
Suppose $f$ is meromorphic on and inside a simple closed contour $\gamma$, and that $f$ has no zeros or poles on $\gamma$, then
$$
\frac{1}{2\pi i} \oint_{\gamma} \frac{f'(z)}{f(z)}~dz=z_{f}-p_{f}
$$
### Proof
Suppose $h(z)=\frac{f'(z)}{f(z)}$, then by the lemma above, $h$ is meromorphic on and inside $\gamma$, so by Cauchy's residue theorem,
$$
\frac{1}{2\pi i} \oint_{\gamma} \frac{f'(z)}{f(z)}~dz =\frac{1}{2\pi i} \oint_{\gamma}h(z)~dz = \sum_{\text{poles of }h\text{ inside }\gamma}\mathrm{Res}_{z=a}(h)
$$
Which by the lemma, these are the poles and zeros of $f$, and residues each contribute the order
## Corollary
Suppose $f$ is meromorphic on and inside a simple closed contour $\gamma$ with no zeros or poles on $\gamma$, then the closed contour $\Gamma_{f}=f\circ\gamma$ satisfies
$$
I_{\Gamma_{f}}(0)=z_{f}-p_{f}
$$

