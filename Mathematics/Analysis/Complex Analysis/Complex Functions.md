Complex [[Functions|functions]] are functions whose [[Domain|domain]] and [[Range|range]] are [[Complex Numbers|complex numbers]];
$$
f:\mathbb{C}\to \mathbb{C}
$$
This is hard to fully visualise, as doing so, would require $\hspace{0pt}4$ dimensions.
We can always write every complex function with its real and imaginary parts
$$
f(z)=\mathfrak{R}(f(z))+i\mathfrak{I}(f(z))
$$
Consequenctly, a complex function can be thought of as two functions from $\mathbb{R}^{2}$ to $\mathbb{R}$, though this is not always the right way to look at it
## Elementary Functions
### $f(z)=z^{n},n\in\mathbb{N}$
Using polar coordinates, which are more suitable for multiplilcation and hence natural powers, we find that if $z=re^{ i\theta }$, then
$$
z^{n}=r^{n}e^{ in\theta }
$$
When we fix $r$; i.e. move on a circle, we see that the angle of the image is sped up by $n$, for example, $n=2$ and $r=1$:
![[Pasted image 20260113132655.png]]
In general if we take a segment of angular length $\eta$ in a circle of radius $r,$ $\theta<\mathrm{arg}(z)<\theta+\eta$, our map will transfer it to a segment of angular length $n\eta \mod 2\pi$ described as $n\theta \mod 2\pi<\mathrm{arg}(z^{n})<(n\theta+n\eta)\mod 2\pi$ in a circle of radius $r^{n}$. Notice that the domain of the argument need to be calculated carefully
In particular, if the length of a segment is $\frac{2\pi}{n}$, then $z^{n}$ will take it to a full circle. In general, $z^{n}$ is not injective, but we can divide the space into slices where it is; one possible partition is given by:
$$
S^{(n)}_{k}=\left\{ z\in \mathbb{C}::\middle|:dle|: -\pi+ \frac{2\pi k}{n}<\mathrm{Arg}(z)\leq-\pi+\frac{2\pi(k+1)}{n}   \right\}
$$
For $k\in\overline{n-1}$
Another is
$$
R^{(n)}_{k}=\left\{ z\in \mathbb{C} ::\middle|:dle|: \frac{2\pi k}{n}\mod 2\pi<\mathrm{Arg}(z)\leq \frac{2\pi(k+1)}{n} \mod 2\pi \right\}
$$
Also for $k\in \overline{n-1}$
If we fix $\theta$, we want to take a segment
Looking at how $z^{n}$ acts, we see that it takes a segment on the ray of angle $\theta$ and changes the distance of each point in this segment $r$ by a power of $n$ (shrinks if $r<1$ and expands if $r>1$)
Moreover, besides the shrinkin/stretching we found, the segment is rotated to a ray of angle $n\theta \mod 2\pi$. For example with $n=3$:
![[Pasted image 20260115143556.png]]

### Lemma
 The map $z^{n}$ [[Injective Functions|injectively]] takes an angular segment of length $\frac{2\pi}{n}$f which is open at one end and closed at the other from a circle of radius $r$ to the entire circle of radius $r^{n}$. If the above segment is closed, or its size larger than $\frac{2\pi}{n}$, the image is no longer injective
 The map $z^{n}$ injectively takes a ray of angle $\theta$ to a ray of angle $n\theta \mod 2\pi$. Consequently, if $n\left| \theta_{1}-\theta_{2} \right|\leq 2\pi$, the map injectively takes the wedge:
 $$
W=\left\{ z\in \mathbb{C} :\middle|: \theta_{1}<\mathrm{Arg}( z)<\theta_{2}\right\}
$$
to the wedge:
$$
\mathfrak{W} = \left\{ z\in \mathbb{C}:\middle|: n\theta_{1}\mod  2\pi<\mathrm{Arg}(z)<n\theta_{2}\mod 2\pi \right\}
$$
with the convention that for any $-\pi<\nu<\xi<\pi$:
$$
\left\{ z\in \mathbb{C}:\middle|: \xi<\mathrm{Arg}(z)<\nu\right\} =\left\{ z\in \mathbb{C}:\middle|:\xi<\mathrm{Arg}(z)\leq \pi \right\}\cup \left\{ z\in \mathbb{C}:\middle|:-\pi<\mathrm{Arg}(z)<\nu \right\}

$$
If we replace one strict inequality ($<$) with an inequality $(\leq)$ the above claim remains true. In this case, if $n\left| \theta_{1}-\theta_{2} \right|=2\pi$, the image of the map will be $\mathbb{C}\setminus \left\{ 0 \right\}$ but not injectively
