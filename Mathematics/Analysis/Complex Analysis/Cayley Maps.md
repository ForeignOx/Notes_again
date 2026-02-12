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
In the first option, the boundary of $\mathbb{H}$ is a line that doesn't pass through the point that $M_{C}$ takes to infinity, $z=-i$. Conseqe