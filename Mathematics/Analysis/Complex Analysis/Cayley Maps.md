## Definition
The Cayley [[Functions|map]] is defined to be
$$
M_{c}(z):= \frac{z-i}{z+i}
$$
It is a [[Mobius Transformations|mobius transformation]] which is represented by a [[Matrices|matrix]]:
$$
C=\begin{pmatrix}
1 & -i \\
1 & i
\end{pmatrix}
$$
A straight forward calculation shows that its [[Inverses|inverse]] is given by
$$
M^{-1}_{C}(z):= \frac{iz+i}{1-z}
$$
## Lemma
- The [[Image|image]] of the upper half plane $\mathbb{H}$ under the Cayley map is the unit disc $\mathbb{D}$
- The image of the unit disc $\mathbb{D}$ is the left half plane $\mathbb{H}_{L}$
- The image of the first quadrant,
$$
\Omega_{1}=\left\{ z\in \mathbb{C}:\middle|:0<\mathrm{Arg}(z)<\frac{\pi}{2} \right\}=\left\{ z\in \mathbb{C}:\middle|:\mathfrak{R}(z)>0,\mathfrak{I}(z)>0 \right\}
$$
    Under the Cayley map is the lower unit disc,
$$
\mathbb{D}_{-}=\left\{ z\in \mathbb{D} :\middle|: \mathfrak{I}(z)<0 \right\}
$$
- The image of the upper unit disc
$$
\mathbb{D}_{+}=\left\{ z\in \mathbb{D}s:\middle|:\mathfrak{I}(z)>0 \right\}
$$
    Under the Cayley map is the left unit disc,
$$
\mathbb{D}_{L}=\left\{ z\in \mathbb{D}:\middle|: \mathfrak{R}(z)<0 \right\}
$$
### Proof
Since the Cayley map is a Mobius map, we know that it will take the [[Open Sets|boundary]] of $\mathbb{H}$ $M_{C}(\mathbb{H})$ 
- In the first option, the boundary of $\mathbb{H}$ is a line that doesn't pass through the point that $M_{C}$ takes to infinity, $z=-i$. Consequently, $M_{C}(\partial \mathbb{H})$ is a circle
    To find which circle it is, we can see where three points from $\partial \mathbb{H}$ are mapped to
    We notice that
$$
M_{C}(-1)=i,~M_{C}(0)=-1,~M_{C}(1)=-i
$$
    And conclude that $M_{C}(\partial \mathbb{H})=\partial \mathbb{D}$. Since $M_{C}(i)=0\in\mathbb{D}$ and $i\in \mathbb{H}$, we find that
$$
M_{C}(\mathbb{H})=\mathbb{D}
$$
- As above, we need to consider where the boundary of $\mathbb{D}$ goes to. Since $\partial \mathbb{D}$ is a circle, it will be mapped to a circle or a line, since $-i\in\partial \mathbb{D}$ is a point that goe to infinity under $M_{C}$, $M_{C}(\partial \mathbb{D})$ must be a line
    To find which line we get, it is enough for us to see where two points on $\partial \mathbb{D}$ (that are not mapped to infinity) are mapped to. We have that
$$
M_{C}(i)=0,~M_{C}(1)=-i
$$
    We conclude that $M_{C}(\partial \mathbb{D})$ is the imaginary axis which is the boundary of $\mathbb{H}_{L}$. Since $M_{C}(0)=-i\in\mathbb{H}_{L}$, we conclude that
$$
M_{C}(\mathbb{D})=\mathbb{H}_{L}
$$
- We notice that we can write
$$
\Omega_{1}=\mathbb{H}\cap \mathbb{H}_{R}
$$
    Since $M_{C}$ is a bijection on [[Riemann Sphere|$\hat{\mathbb{C}}$]], we have that
    $$
M_{C}(\Omega_{1})=M_{C}(\mathbb{H}\cap \mathbb{H}_{R})=M_{C}(\mathbb{H})\cap M_{C}(\mathbb{H}_{R})=\mathbb{D}\cap M_{C}()
$$