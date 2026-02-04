## Theorem
If $\underline{f}:\mathbb{R}^{3}\to \mathbb{R}^{3}$ is a [[Continuity|continuously]] [[Differentiation|differentiable]] $C^{1}$ vector field and $S$ is a closed [[Surfaces|surface]] with outward normal $\underline{\hat{n}}$ bounding a region $V$, then
$$
\oint_{S}\underline{f}\cdot  \underline{\hat{n}}\,dS=\int _{V}\underline{\nabla } \cdot \underline{f} \, dV 
$$
So the [[Surface Integrals|flux]] is equal to the [[Volume Integrals|volume integral]] of the [[Divergence and Curl|divergence]] of the vector field
Many call this the Gauss theorem, this is another generalisation of the [[Fundamental Theorem of Calculus|fundamental theorem of calculus]]
## Remark
This generalises to $V\subset\mathbb{R}^{n}$, with boundary $S$ an $(n-1)$D hypersurface
For $n=1$, we have $V=[a,b],S=\left\{ a,b \right\}$, so the boundary is just the two distinct points, so
$$
\underline{\hat{n}}=\begin{cases}
-\underline{e}_{1} & x=a \\
\underline{e}_{1} & x=b
\end{cases}
$$
$$
\underline{f}=f(x)\underline{e}_{1}, \underline{\nabla} \cdot \underline{f} =f'(x)
$$
So the theroem reduces to $f(b)-f(a)=\int ^{b}_{a} f'(x) \, dx$, or the fundamental theorem of calculus we know
This theorem applies even when the boundary $S$ is not connected, for example if we had two concentric spheres $S=S_{0}\cup S_{1}$, we'd get
$$
\oint_{S_{0}}\underline{f}\cdot  \underline{\hat{n}}_{1}\,dS+\oint_{S_{1}}\underline{f}\cdot  \underline{\hat{n}}_{2}\,dS=\int _{V}\underline{\nabla} \cdot \underline{f}  \, dV 
$$
This theorem plays a fundamental role in connecting integral and differential forms of conservation laws
### Proof
In idea; subdivide $V$ into a disjoint union of small domains $V_{i}$ for $i=1,\dots,m$ whose boundaries $S_{i}$ have unit normals $\underline{\hat{n}}_{i}$
![[Pasted image 20251028121727.png]]
Each interior segment of $S_{i}$ is shared by a neighbouring subdomain $V_{j}$ with equal and opposite normal $\underline{\hat{n}}_{j}=-\underline{\hat{n}}_{i}$
Soo
$$
\oint_{S} \underline{f}\cdot  \underline{\hat{n}}\,dS=\sum_{i=1}^{m}\oint_{S_{i}} \underline{f}\cdot  \underline{\hat{n}}_{i} \,dS
$$
As only contributions from the global boundary survive, all others cancel out with their neighbours.
$$

$$
$$
= \sum_{i=1}^{m} \frac{1}{\left| V_{i} \right| }\oint_{S_{i}} \underline{f}\cdot  \underline{\hat{n}}_{i}\,dS \left| V_{i} \right| 
$$
$$
=\lim_{ m \to \infty } \sum_{i=1}^{m} \underbrace{ \frac{1}{\left| V_{i} \right| }\oint_{S_{i}} \underline{f}\cdot  \underline{\hat{n}}_{i}\,dS }_{ \to \underline{\nabla} \cdot \underline{f}  } \left| V_{i} \right| 
$$
$$
= \int _{V}\underline{\nabla} \cdot \underline{f}  \, dV 
$$
Which needs $\underline{f}\in C^{1}$ to work (proof beyond the scope of this course)
## Example
Verify the divergence theorem by computing borh sides for $\underline{f}=r^{2}\cos ^{2}\theta \underline{e}_{r}$ in spherical coordinates, where $S$ is the sphere $x^{2}+y^{2}+z^{2}=a^{2}$.
For the flux:
$$
\oint_{S} \underline{f}\cdot  \underline{\hat{n}}\,dS=\int_{0}^{2\pi} \int_{0}^{\pi} \underline{f}\cdot \underline{e}_{r}h_{\theta}h_{\phi} \, d\theta  \, d\phi 
$$
$$
= \int_{0}^{2\pi} \int_{0}^{\pi} a^{2}\cos ^{2}\theta a^{2}\sin\theta \, d\theta  \, d\phi 
$$
$$
= a^{4}\int_{0}^{2\pi} \int_{0}^{\pi} \cos ^{2}\theta \sin\theta \, d\theta  \, d\phi 
$$
$$
    = a^{4}\int_{0}^{2\pi} \left[ -\frac{\cos ^{3}\theta}{3} \right]_{0}^{\pi} \, d\phi 
$$
$$
= \frac{2a^{4}}{3}\int_{0}^{2\pi}  \, d\phi=\frac{4\pi a^{4}}{3}   
$$
Now we calculate the volume integral of $\underline{\nabla} \cdot \underline{f}$.
$$
\underline{\nabla} \cdot \underline{f}=\frac{1}{h_{r}h_{\theta}h_{\phi}}\left( \frac{ \partial  }{ \partial r } (h_{\theta}h_{\phi}f_{r})+\frac{ \partial  }{ \partial \theta } (h_{r}h_{\phi}f_{\theta})+\frac{ \partial  }{ \partial \phi } (h_{r}h_{\theta}f_{\phi}) \right)
$$
$$
= \frac{1}{r^{2}\sin\theta}\frac{ \partial  }{ \partial r } (r^{2}\sin\theta r^{2}\cos ^{2}\theta)
$$
$$
= \frac{\cos ^{2}\theta}{r^{2}}\frac{ \partial  }{ \partial r } r^{4}=4r\cos ^{2}\theta 
$$
So
$$
\int _{V}\underline{\nabla} \cdot \underline{f}  \, dV = \int_{0}^{2\pi} \int_{0}^{\pi} \int_{0}^{a} 4r\cos ^{2}\theta h_{r}h_{\theta}h\phi \, dr  \, d\theta  \, d\phi 
$$
$$
= \int_{0}^{2\pi} \int_{0}^{\pi} \int_{0}^{a} 4r^{3}\cos ^{2}\theta \sin\theta \, dr  \, d\theta  \, d\phi 
$$
$$
= \int_{0}^{2\pi} \int_{0}^{\pi} [r^{4}\cos ^{2}\theta \sin\theta]_{0}^{a} \, d\theta  \, d\phi 
$$
$$
= a^{4}\int_{0}^{2\pi} \int_{0}^{\pi} \cos ^{2}\theta \sin\theta \, d\theta  \, d\phi =\frac{4\pi a^{4}}{3}  
$$
As it is the same as above, which is what we wanted.
___
The integral conservation of electric charge:
$$
\frac{d }{dt}\int _{V}q \, dV  
$$
Where $q$ is the charge density
$$
=-\oint_{S} \underline{j}\cdot  \underline{\hat{n}}dS
$$
Where $\underline{j}$ is the current density, and we are interested in what happens on the boundary, so this second integral is the total current flowing out of the boundary
Now the divergence theorem tells us
$$
\frac{d }{dt} \int _{V}q \, dV=\int _{V}\frac{ \partial q }{ \partial t }  \, dV=-\oint_{S} \underline{j}\cdot  \underline{\hat{n}}\,dS=-\int _{V}\underline{\nabla} \cdot \underline{j}  \, dV   
$$
Since this holds for any volume $V$, we see that $q(\underline{x},t)$ and $\underline{j}(\underline{x},t)$ must obey the differential conservation law
$$
\frac{ \partial q }{ \partial t } =-\underline{\nabla} \cdot \underline{j} 
$$
And in general 
$$
\frac{ \partial }{ \partial t } (\text{conserved quantity})+\underline{\nabla} \cdot \underline{\text{flux}} =0
$$
