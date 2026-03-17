## Theorem
Suppose [[Complex Functions|$f$]] is [[Meromorphicity|meromorphic]] on and inside a simple closed contour $f$, and assume $f$ has no [[Poles|pole]] on $\gamma$, then
$$
\oint_{\gamma}f(z)~dz = 2\pi i \sum_{j=1}^{m}\mathrm{Res}_{z=a_{j}}(f)
$$
Where $a_{1},\dots,a_{m}$ are the poles of $f$ inside $\gamma$
### Proof
If $S_{\gamma}=\left\{ a_{1},\dots,a_{m} \right\}$ is the set of poles inside the countour is empty, we are done, by [[Cauchy-Goursat Theorem|Cauchy-Goursat]],
Otherwise for each pole $z=a_{j}$, we have a [[Laurent Series|Laurent series]] around $z=a_{j}$ on some ball. Let
$$
pp_{j}(z)=\sum_{n=-k_{j}}^{-1}c_{n,j}(z-a_{j})^{n}
$$
Be the principle parts of the Laurent series around $z=a$
Each $pp_{j}(z)$ is just a finite sum of reciprocals of $(z-a_{j})$, so these extend to holomorphic functions on $\mathbb{C}\setminus \left\{ a_{j} \right\}$
It makes sense to consider
$$
\oint_{\gamma} pp_{j}(z)~dz=\oint_{\gamma}\sum_{n=-k}^{-1} c_{n,j}(z-a_{j})^{n}~dz  
$$
$$
= \sum_{n=-k}^{-1} c_{n,j}\oint_{\gamma}(z-a_{j})^{n}~dz=2\pi i c_{-1,j}=2\pi i\mathrm{Res}_{z=a_{j}}(f)
$$
Cauchy considered
$$
g(z)=f(z)-\sum_{j=1}^{m}pp_{j}(z)
$$
$$
\implies g(z)=f(z)-pp_{i}(z)-\sum_{j\neq i} pp_{j}(z)=ap_{i}(z)-\sum_{j\neq i}pp_{j}(z)
$$
Where $ap_{i}$ is the analytic part of $f$ at $z=a_{i}$ and all the principle parts at $a_{j}$ where $j\neq i$ must all be holomorphic at $a_{i}$, so by Cauchy-Goursat,
$$
0=\oint_{\gamma}g(z)~dz=\oint_{\gamma}\left( f(z)-\sum_{j=1}^{m}pp_{j}(z) \right)~dz 
$$
$$
= \oint_{\gamma}f(z)~dz-\sum_{j=1}^{m} \oint_{\gamma}pp_{j}(z)~dz = \oint_{\gamma}f(z)~dz-2\pi i \sum_{j=1}^{m}\mathrm{Res}_{z=a_{j}}(f)
$$
Giving the required result
In fact the o.g. way this was proved was by approximating the contour with a polygon and then triangulate it and then only consider the triangles containing poles and then using the generalised Cauchy integral formula
## Example
Compute 
$$
\oint_{\left| z \right| =1} \frac{1}{\sin z}~dz
$$
Which has poles at $z=n\pi$, so by the Cauchy residue theorem,
$$
\oint_{\left| z \right| =1} \frac{1}{\sin z}~dz =2\pi i \mathrm{Res}_{z=0}(f)=2\pi i\cdot 1=2\pi i
$$
___
Calculate
$$
\oint_{\gamma} \frac{e^{ z }}{z^{2}+z^{3}}~dz
$$
Where $\gamma$ is any oriented simple closed contour such that $\hspace{0pt}0$ is inide $\gamma$ and $-1$ is outside, we have
$$
f(z)=\frac{e^{ z }}{z^{2}(z+1)}
$$
If we write 
$$
f(z)= \frac{g(z)}{z^{2}}
$$
Where $g(z)=\frac{e^{ z }}{z+1}$ then $g$ is holomorphic on and inside $\gamma$, so by rule $\hspace{0pt}3$, 
$$
\mathrm{Res}_{z=0}(f)= \frac{g^{(2-1)}(0)}{(2-1)!}=g'(0)
$$
And
$$
g'(z)= \frac{e^{ z }}{1+z} - \frac{e^{ z }}{(1+z)^{2}}
$$
So $g'(0)=0$, soo
$$
\oint_{\gamma}f~dz=0
$$
## Integrals of Rational Real Functions of $\cos$ and $\sin$
### Example
Show that
$$
\int_{0}^{2\pi}  \frac{1}{1+a\sin\theta} \, d\theta=\frac{2\pi}{\sqrt{ 1-a^{2} }} 
$$
For $a\in(-1,1)$
We know $\sin\theta=\frac{e^{ i\theta }-e^{ -i\theta }}{2i}$, assuming $a\neq 0$ then
$$
\int_{0}^{2\pi}  \frac{1}{1+a\sin\theta} \, d\theta =\int_{0}^{2\pi}  \frac{1}{1+a\left( \frac{e^{ i\theta }-e^{ -i\theta }}{2i} \right)} \, d\theta =\int_{0}^{2\pi}  \frac{2ie^{ i\theta }}{2ie^{ i\theta }+ae^{ 2i\theta }-a} \, d\theta 
$$
If we consider the function $\gamma(\theta)=e^{ i\theta }$ for $\theta \in[0,2\pi]$ is the unit circle in $\mathbb{C}$ hmmm
$$
=\int_{0}^{2\pi}  \frac{2\gamma'(\theta)}{a(\gamma(\theta))^{2}+2i(\gamma(\theta))-a} \, d\theta 
$$
$$
= \oint_{\left| z \right| =1} \frac{2}{az^{2}+2iz-a}~dz = \oint_{\left| z \right| =1} \frac{2}{a(z-z_{1})(z-z_{2})}~dz
$$
By completing the square, where $z_{1}=i\left( \frac{-1+\sqrt{ 1-a^{2} }}{a} \right), z_{2}=i\left( \frac{-1-\sqrt{ 1-a^{2} }}{a} \right)$
Note that $\left| z_{2} \right| <0$ and $z_{1}z_{2}=-1$, so $\left| z_{1} \right|<1$
So by Cauchy's residue theorem
$$
        \int_{0}^{2\pi}  \frac{1}{1+a \sin\theta} \, d\theta = 2\pi i \mathrm{Res}_{z=z_{1}}(f)=2\pi i \frac{2}{a(z_{1}-z_{2})}= \frac{2\pi i}{i\sqrt{ 1-a^{2} }}
$$
## Integrals of Rational Functions
We can perform this method for integrals of the form
$$
\int_{-R}^{R}  \frac{p(x)}{q(x)} \, dx
$$
When $\deg q\geq \deg p+2$ and $q$ has no real roots, it works by considering the D-shaped domain and taking it to infinity
### Example
Evaluate
$$
\int_{0}^{\infty} \frac{x^{2}}{x^{6}+1} \, dx :=\lim_{ R \to \infty } \int_{0}^{R}  \frac{x^{2}}{x^{6}+1} \, dx 
$$
We now perfrom the genius move of writing $z$ instead of $x$:
$$
f(z)= \frac{z^{2}}{z^{6}+1}
$$
We also note that $f$ is [[Even Functions|even]], so $\int_{0}^{R} \frac{x^{2}}{x^{6}+1} \, dx=\frac{1}{2}\int_{-R}^{R} \frac{x^{2}}{x^{6}+1} \, dx$ 
How does the integral of $f$ relate to the function above? Consider the straight line $L_{R}=x$ for $x\in[-R,R]$, so
$$
\int _{L_{R}}f(z) \, dz=2\int_{-R}^{R} f(L_{R}(x))L'_{R} \, dx =\int_{-R}^{R}  \frac{x^{2}}{x^{6}+1} \, dx =2\int_{0}^{R}  \frac{x^{2}}{x^{6}+1} \, dx  
$$
To close the contour, we consider the semicircular contour $C_{R}(t)=Re^{ it }$ for $t\in[0,\pi]$, and we write $\gamma_{R}:= L_{R}\cup C_{R}$, this is called a D-shaped contour
![[Pasted image 20260317121322.png]]
We have
$$
\oint_{\gamma_{R}}f=\int _{L_{R}}f+\int _{C_{R}}f
$$
$$
\implies \int_{0}^{\infty}  \frac{x^{2}}{x^{6}+1} \, dx =\lim_{ R \to \infty }  \int_{0}^{R} \frac{x^{2}}{x^{6}+1} \, dx =\frac{1}{2} \lim_{ R \to \infty } \int_{-R}^{R}  \frac{x^{2}}{x^{6}+1} \, dx 
$$
$$
= \frac{1}{2}\lim_{ R \to \infty } \int _{L_{R}}f(z) \, dz =\frac{1}{2}\lim_{ R \to \infty } \left( \oint_{\gamma_{R}}f(z)~dz-\int _{C_{R}}f(z) \, dz  \right)
$$
What happens to $\int _{C_{R}}f$ as $R\to \infty$, by the [[ML Inequality|ML inequality]],
$$
\left| \int _{C_{R}}f(z) \, dz  \right| \leq L(C_{R})\sup_{z\in  C_{R}} \left| f(z) \right| =\pi R\sup_{z\in  C_{R}} \left|  \frac{z^{2}}{z^{6}+1} \right|  \leq \pi R \sup_{z\in  C_{R}}  \frac{\left| z \right| ^{2}}{\left| z \right| ^{6}-1} 
$$
$$
= \pi R \cdot \frac{R^{2}}{R^{6}-1}=\frac{\pi R^{3}}{R^{6}-1}\to 0 \text{ as } R\to \infty
$$
So
$$
\int_{0}^{\infty} \frac{x^{2}}{x^{6}+1} \, dx =\frac{1}{2}\lim_{ R \to \infty }  \oint_{\gamma_{R}} f(z)~dz
$$
And by Cauchy's residue theorem,
$$
\oint_{\gamma_{R}}f(z)~dz = 2\pi i \sum\mathrm{Res}_{z=z_{i}} (f)
$$
And the poles of 
$$
f(z)= \frac{z^{2}}{z^6+1}
$$
Are at the zeros of $z^{6}+1$, so at
$$
z_{k}=e^{ \frac{i\pi}{6}+\frac{2k\pi i}{6} }
$$
For $k\in \overline{6}$, sooo
$$
z_{k}\in  \left\{ e^{ \frac{i\pi}{6} },e^{ i \frac{3\pi}{6} }, e^{ i \frac{5\pi}{6} },e^{ i \frac{7\pi}{6} }, e^{ i \frac{9\pi}{6} },e^{ i \frac{11\pi}{6} } \right\}
$$
And since we have a D-shaped contour, poles with $\mathfrak{I}( z)>0$
So by the second rule for residues with $g(z)= \frac{z^{2}}{z^{6}+1}$, $g(z)=z^{2},h(z)= z^{6}+1$,
$$
\mathrm{Res}_{z=z_{k}}(f)= \frac{g(z_{k})}{h'(z_{k})}= \frac{z_{k}^{2}}{6z_{k}^{5}}=\frac{1}{6z_{k}^{3}}= \frac{1}{6(-1)^{k}i}
$$
Soo
$$
\int_{ 0}^{\infty}  \frac{x^{2}}{x^{6}+1} \, dx=\frac{1}{2}\lim_{ R \to \infty }  \pi i \left( \frac{1}{6i}-\frac{1}{6i}+\frac{1}{6i} \right)=\frac{\pi}{6}
$$

## Indented Contours
### Lemma: Indentation Lemma
Suppose $g$ has a simple (order 1) pole at $z=a$, then for any $\rho>0$, let $C_{\rho}$ be the semicircular contour joining $a+\rho$ to $a-\rho$ via
$$
C_{\rho}(\theta)=a+\rho e^{ i\theta }
$$
For $\theta \in[0,\pi]$
Then
$$
\lim_{ \rho \to 0 } \int _{C_{\rho}}g(z) \, dz =\pi i \mathrm{Res}_{z=a}(g)
$$
#### Proof
Conider the Laurent series of $g$ around $z=a$, it is 
$$
g(z)=\sum_{n=-1}^{\infty} c_{n}(z-a)^{n} = \frac{c_{-1}}{z-a}+\underbrace{ \sum_{n=0}^{\infty} c_{n}(z-a)^{n} }_{ =h(z) }
$$
So
$$
\int _{C_{\rho} g(z)}g(z) \, dz  = c_{-1} \int _{C_{\rho}} \frac{1}{z-a} \, dz \int _{C_{\rho}}h(z) \, dz  
$$
And we claim that
$$
\lim_{ \rho \to 0 }  \int _{C_{\rho}}h(z) \, dz=0 
$$
Which we prove with our best friend the ML inequality
We know $h$ is holomorphic on $B_{R}(a)$, so by the [[Extreme Value Theorem|extreme value theorem]], $h$ attains a maximum on $\overline{B}_{\frac{\rho}{2}}(a)$, so there exists $M>0$ independent of $\rho$ such that
$$
\left| h(z) \right| \leq M \forall z \in  C_{\rho}
$$
So by the ML inequality:
$$
\left| \int _{C_{\rho}}h(z) \, dz  \right| \leq L(C_{\rho})\sup_{z\in  C_{\rho}} \left| h(z) \right| \leq \pi \rho M\to 0
$$
As $\rho\to 0$, finally, note
$$
\int _{C_{\rho}} \frac{1}{z-a} \, dz = \int _{0}^{\pi} \frac{C_{\rho}'(\theta)}{C_{\rho}(\theta)-a} \, d\theta =\int_{0}^{\pi}  \frac{i\rho e^{ i\theta }}{\rho e^{ i\theta }} \, d\theta=\int_{0}^{i} i \, d\theta  
$$
Thus
$$
\lim_{ \rho \to 0 }  \int _{C_{\rho}}g(z) \, dz=c_{-1} \pi i+0=\mathrm{Res}_{z=a}(g)\pi i 
$$
___
$$
\int_{0}^{\infty}  \frac{\sin x}{x} \, dx =\lim_{ \rho \to 0,R\to \infty } \int_{\rho}^{R} \frac{\sin x}{x} \, dx 
$$
Instead we consider the sneaky function $f(z)=\frac{e^{ iz }}{z}$
This has a nasty pole at $z=0$, aiaiai, so we can't use D-shape, so instead we step-around (omg pole reference????/?????!!?!?!?!?!???!?!???!?!?????)
So we actually have some freaky semiannulus
![[Pasted image 20260317121347.png]]
Sooo we let
$$
\gamma:= \gamma_{\rho,R}=L_{1} \cup C_{R}\cup L_{2}\cup(-C_{\rho})
$$
What is the relevance? First note that $f$ is holomorphic on and inside $\gamma$, so by Cauchy-Gourssat for simple closed curves,
$$
\oint_{\gamma}f~dz=0

$$
Consider
$$
\int _{L_{1}} e^{ iz } \, dz+\int _{L_{2}} e^{ iz } \, dz =\int _{\rho}^{R} \frac{e^{ ix }}{x} \, dx +\int_{-R}^{-\rho} \frac{e^{ iy }}{y} \, dy   
$$
$$
    = \int_{\rho}^{R}  \frac{e^{ ix }}{x} - \frac{e^{- ix }}{x} \, dx =2i \int_{\rho}^{R}  \frac{\sin x}{x} \, dx
     
$$
Which is what we were wanting omg
Soo we can do some rearranging to see that
$$
\int_{\rho}^{R}  \frac{\sin x}{x} \, dx =\frac{1}{2i}\left( \int _{C_{\rho}}f -\int _{C_{R}} f   \right)
$$
For $C_{R}$, we need the lemma that for $R>0$,
$$
\int_{0}^{\pi} e^{ -R\sin\theta } \, d\theta <\frac{\pi}{R}
$$
Note that on $C_{R}$, where $z=R e^{ i\theta }=R\cos\theta+Ri\sin\theta$, so
$$
\left| e^{ iz } \right| =\left| e^{ iRe^{ i\theta } } \right|=\left|  e^{ iR\cos\theta-R\sin\theta } \right|=e^{ -R\sin\theta }
$$
So using the Estimate lemma, 
$$
\left| \int _{C_{R}} \frac{e^{ iz }}{z} \, dz \right| \leq \int_{0}^{\pi}  \left| \frac{e^{ iR e^{ i\theta } }}{Re^{ i\theta }} \right|\cdot \left| iR e^{ i\theta } \right| \, d\theta=\int_{0}^{\pi} e^{ -R \sin\theta} \, d\theta<\frac{\pi}{R}\to 0\text{ as }R\to \infty
$$


