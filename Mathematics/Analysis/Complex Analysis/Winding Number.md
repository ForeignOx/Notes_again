## Definition
Let $\gamma:[a,b]\to \mathbb{C}$ be a path in the form of [[Curves#Theorem|this theorem]] then the quantity
$$
I_{\gamma}(w)= \frac{\theta(b)-\theta(a)}{2\pi}
$$
For $w\not\in \gamma$ is called the winding number of $\gamma$ around $w$
## Example
For $\gamma_{1}=e^{ 2\pi it }$ (which is the right form with $w=0,r(t)=1,\theta(t)=2\pi t$), so
$$
I_{\gamma_{1}}(0)=\frac{\theta(1)-\theta(0)}{2\pi}=\frac{2\pi-0}{2\pi}=1
$$
___
For $\gamma_{2}=e^{ -4\pi it }$ (which has $w=0,r=1,\theta(t)=-4\pi t$)
Soo
$$
I_{\gamma_{2}}(0)= \frac{\theta(1)-\theta(0)}{2\pi} = \frac{-4\pi}{2\pi}=-2
$$
## Remark
The function $\theta$ is unique up to an additive constant
If $\gamma$ is a contour, we can so that $r,\theta$ are piecewise $C^{1}$
## Proposition
If $\gamma$ is closed, then for all $w\not\in \gamma$, we have $I_{\gamma}\in \mathbb{Z}$
### Proof
Since the contour $\gamma(t)=w+r(t)e^{ -\theta(t) }$ is closed, we have $r(a)=r(b)$ (since $\gamma(a)=\gamma(b)$)and soo
$$
r(a)e^{ i\theta(a) }=r(b)e^{ i\theta(b) } 
$$
$$
\iff e^{ i\theta(a) }=e^{ i\theta(b) }
$$
$$
 \iff e^{ i(\theta(b)-\theta(a)) }=1 
$$
$$
\iff i(\theta(b)-\theta(a))=2n\pi i 
$$
$$
 \iff \frac{\theta(b)-\theta(a)}{2\pi}=n
$$
wow
## Lemma
Let $\gamma:[a,b]\to \mathbb{C}$ be a closed contour. Then for any $w\not\in \gamma$,
$$
I_{\gamma}(w)=\frac{1}{2\pi i} \oint_{\gamma} \frac{1}{z-w}~dz
$$
### Prof
By a theorem previously referenced, we know we can write $\gamma(t)=w+r(t)e^{ i\theta(t) }$, where $r,\theta$ are piecewise $C^{1}$
$$
\oint_{\gamma} \frac{1}{z-w}~dz=\int ^{b}_{a} \frac{\gamma'(t)}{\gamma(t)-w} \, dt =\int ^{b}_{a} \frac{r'(t)e^{ i\theta(t) }+i\theta'(t)r(t)e^{ i\theta(t) }}{r(t)e^{ i\theta(t) }} \, dt 
$$
$$
= \int ^{b}_{a} \frac{r'(t)}{r(t)} \, dt+i \int ^{b}_{a} \theta'(t) \, dt 
$$
$$
= [\log(r(t))]_{a}^{b}+i[\theta(t)]_{a}^{b}=0+i(\theta(b)-\theta(a))=2\pi i\frac{\theta(b)-\theta(a)}{2\pi}=2\pi iI_{\gamma}(w)   
$$
## Proposition
Given a simple closed contour $\gamma$, one can place an orientation on $\gamma$ such that for $w\not\in \gamma$, we have
$$
I_{\gamma}(w)=\begin{cases}
1 & w\in D_{\gamma} \\
0 & w\in \mathbb{C}\setminus(D_{\gamma}\cup\gamma)
\end{cases}
$$
## Proposition
Let $D$ be a starlike domain, then for any close contour $\gamma$ in $D$, $I_{\gamma}(w)=0$ for every $w\not\in D$
### Proof
If $d=\mathbb{C}$ there are no points to check
$\frac{1}{z-w}$ is holomorphic and irreducible and
$$
\oint_{\gamma} \frac{1}{z-w}\delta z=0
$$
