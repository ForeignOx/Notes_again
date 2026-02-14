These are useful to find [[Domains|domains]] that are [[Holomorphicity|holomorphically]] equivalent
## Definition
Let $D$ and $D'$ be domains. We say that a [[functions|function]] $f:D\to D'$ is biholomorphic if $f$ is holomorphic, a [[Bijective Functions|bijection]], and the [[Inverses|inverse]] $f^{-1}:D'\to D$ is also holomorphic
A biholomorphic map $f$ is called a biholomorphism. When $f$ as above exists, we say that the domains $D$ and $D'$ are biholomorphic and write $f:D \tilde{\to} D'$
## Remark
It is possible to prove that if $f$ as above is holomorphic and bijective then it is automatic that its inverse is holomorphic
## Example
The map $f(z)=az+b$ is biholomorphic between $\mathbb{C}$ and $\mathbb{C}$ if $a\neq 0$, in that case, its inverse is 
$$
f^{-1}(z)=\frac{z-b}{a}
$$
___
[[Exponential Functions|$f(z)=e^{ z }$]] is not biholomorphic from $\mathbb{C}$ to $\mathbb{C}^{*}$ as it is not injective. It is, however, a biholomorphism between $\left\{ z\in\mathbb{C}:\middle|: c<\mathfrak{I}(z)<c+2\pi \right\}$ and [[rays|$\mathbb{C}\setminus R_{c}$]] for any $c\in\mathbb{R}$
The inverse in that case is the appropriate branch of [[Logarithms|$\log z$]]
One natural example is the case when $c=-\pi$, in which we get the principal logarithm $\mathrm{Log}$ as the inverse
Note that $e^{ z }$ is a holomorphic bijection from $\left\{ z\in\mathbb{C}:\middle|:c<\mathfrak{I}(z)\leq c+2\pi \right\}$ to $\mathbb{C}^{*}$ but it has no holomorphic inverse in that case
___
$f(z)=z^{2}$ is not biholomorphic from $\mathbb{C}$ to $\mathbb{C}$. It is biholomorphic from $\mathbb{H}_{R}$ to $\mathbb{C}\setminus \mathbb{R}_{\leq 0}$
The inverse is the "positive" [[roots|root]] function $z^{\frac{1}{2}}$. Changeing $\mathbb{H}_{R}$ to $\mathbb{H}_{L}$ gives the "negative" root function as the holomorphic inverse
## Remark
The desire for our biholomorphic map to be also defined on the boundary and that it maps $\partial D$ to $\partial D'$ is far from trivial:
- The map $f(z)=e^{ z }$ takes $D=\left\{ z\in\mathbb{C}:\middle|:-\pi<\mathfrak{I}(z)<2\pi \right\}$ to $D'=\mathbb{C}^{*}$. It is not injective so the map is not biholomorphic. Boundary is not mapped to boundary in this case as
$$
\partial D=\left\{ z\in \mathbb{C}:\middle|:\mathfrak{I}(z)=-\pi \right\}\cup \left\{ z\in \mathbb{C}:\middle|:\mathfrak{I}(z)=2\pi \right\}=\mathbb{R}\setminus \left\{ 0 \right\}
$$
    while
$$
\partial f(D)=\partial D'=\left\{ 0 \right\}\neq \mathbb{R}\setminus \left\{ 0 \right\}=f(\partial D)
$$
- The map $f(z)=e^{ z }$ takes $D=\left\{ z\in\mathbb{C}:\middle|:-\pi<\mathfrak{I}(z)<\pi \right\}$ biholomorphically to $D'=\mathbb{C}\setminus \mathbb{R}_{\leq 0}$. While the boundary is mapped to the boundary in this case, every point in $\partial D'=\mathbb{R}_{\leq 0}$ is achieved twce from the $\partial D$: once from $\left\{ z\in\mathbb{C}:\middle|: \mathfrak{I}(z)=-\pi \right\}$ and once from $\left\{ z\in\mathbb{C}:\middle|: \mathfrak{I}(z)=\pi \right\}$
## Remark
We can compose biholomorphic maps to create new biholomorphic maps. In particular, we have that the set of biholomorphic maps from a set to itself has a nice structure, it is that of [[Automorphism Groups|automorphism groups]]
## Example
We have gathered a large collection of biholomorphic map with which we can start mapping one domain in the complex plane to another. Here is a table summarising some of the important maps we've considered:

| Function                                                                                                    | Maps the Domain                                                                                                                                    | To the Domain                                                                | Inverse                                                                  |
| ----------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| $z^{n},n\in\mathbb{N}$                                                                                      | $\left\{ \theta_{1}<\mathrm{Arg}(z)<\theta_{2} \right\}$ with $-\pi \leq\theta_{1}<\theta_{2}\leq \pi$, $\theta_{2}-\theta_{1}\leq \frac{2\pi}{n}$ | $\left\{ n\theta_{1}\mod 2\pi<\mathrm{Arg}(z)<n\theta_{2}\mod 2\pi \right\}$ | Appropriate branch of $z^{\frac{1}{n}}$                                  |
| Principle branch of $z^{\frac{1}{n}},n\in\mathbb{N}$                                                        | $\left\{ \theta_{1}<\mathrm{Arg}(z)<\theta_{2} \right\}$ with $-\pi \leq\theta_{1}<\theta_{2}\leq \pi$                                             | $\left\{ \frac{\theta_{1}}{n}<\mathrm{Arg}(z)<\frac{\theta_{2}}{n} \right\}$ | $z^{n}$                                                                  |
| $e^{ z }$                                                                                                   | $\left\{ \alpha<\mathfrak{I}(z)<\alpha+2\pi \right\}$ with $\alpha \in \mathbb{R}$                                                                 | $\mathbb{C}\setminus R_{\alpha}$                                             | Appropriate branch of $\log z$                                           |
| $\mathrm{Log}(z)$                                                                                           | $\left\{ \theta_{1}<\mathrm{Arg}(z)<\theta_{2} \right\}$ with $-\pi \leq \theta_{1}<\theta_{2}\leq \pi$                                            | $\left\{ \theta_{1}<\mathfrak{I}(z)<\theta_{2} \right\}$                     | $e^{ z }$                                                                |
| $\frac{1}{z}$                                                                                               | $\left\{ r_{1}<z<r_{2} \right\}$                                                                                                                   | $\left\{ \frac{1}{r_{2}}<\left\| z \right\|< \frac{1}{r_{1}} \right\}$       | $\frac{1}{z}$                                                            |
| $M_{C}=\frac{z-i}{z+i}$                                                                                     | $\mathbb{D}$                                                                                                                                       | $\mathbb{H}_{L}$                                                             | $M_{C}^{-1}(z)= \frac{iz+i}{1-z}$                                        |
| $M_{C}=\frac{z-i}{z+i}$                                                                                     | $\mathbb{H}$                                                                                                                                       | $\mathbb{D}$                                                                 | $M_{C}^{-1}(z)= \frac{iz+i}{1-z}$                                        |
| $M_{C}=\frac{z-i}{z+i}$                                                                                     | $\Omega_{1}$                                                                                                                                       | $\mathbb{D}_{-}$                                                             | $M_{C}^{-1}(z)= \frac{iz+i}{1-z}$                                        |
| $M_{C}=\frac{z-i}{z+i}$                                                                                     | $\mathbb{D}_{+}$                                                                                                                                   | $\mathbb{D}_{L}$                                                             | $M_{C}^{-1}(z)= \frac{iz+i}{1-z}$                                        |
| $M_{T}(z)$ with $T\in SL_{2}(\mathbb{R})$                                                                   | $\mathbb{H}$                                                                                                                                       | $\mathbb{H}$                                                                 | $M_{T^{-1}}(z)$                                                          |
| $M(z)=e^{ i\theta } \frac{z-z_{0}}{\overline{z_{0}}z-1}$ with $\theta \in(-\pi,\pi]$, $z_{0}\in \mathbb{D}$ | $\mathbb{D}$                                                                                                                                       | $\mathbb{D}$                                                                 | $M^{-1}(z)=\frac{z-z_{0}e^{ i\theta }}{z\overline{z_{0}}-e^{ i\theta }}$ |
___
Find a biholomorphic map that takes $\mathbb{C}\setminus \mathbb{R}_{\leq 0}$ to $\mathbb{D}$ 
We know that a [[Cayley Maps|Cayley tranformation]] takes the upper half plane to $\mathbb{D}$, so we do this by going $z^{\frac{1}{2}}$, to make the right half plane, $e^{ i \frac{\pi}{2} }$ to rotate to upper half plane, and then Cayley map to turn it to unit disk
![[Pasted image 20260210111554.png]]
![[Pasted image 20260210111531.png]]
It is important to note that $f_{1}(z)=z^{\frac{1}{2}}$ is the principle branch of the square root which is indeed holomorphic in the domain $\mathbb{C}\setminus \mathbb{R}_{\leq 0}$. Both $f_{2}$ and $f_{3}$ are Mobius transformations and as such are holomorphic in their domains of definition
One option for our desired map is
$$
f(z)=f_{3}(f_{2}(f_{1}(z)))= \frac{z^{\frac{1}{2}}-1}{z^{\frac{1}{2}}+1}
$$
___
Find a biholomorphism that takes $\mathbb{D}_{-}$ to $\mathbb{H}$
Once again we build the desired map by composing biholomorphic maps as described in the following diagram
![[Pasted image 20260214175018.png]]
![[Pasted image 20260214175049.png]]
It is important to note that $f_{2}(z)=z^{2}$ is a biholomorphism between $\Omega_{1}$ and $\mathbb{H}$ with its inverse being the principal square root $z^{\frac{1}{2}}$ (which is well defined since the real axis is not in the domain)
$f_{1}$ is a Mobius transformation and as such holomorphic in their domain of definition
One option for our desired map is
$$
f(z)=f_{2}(f_{1}(z))-\left( \frac{z+1}{z-1} \right)^{2}
$$
