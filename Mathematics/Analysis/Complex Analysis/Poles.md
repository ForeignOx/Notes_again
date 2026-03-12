## Lemma: Characterisation Lemma for Poles
Suppose [[Complex Functions|$f$]] has an [[Isolated Singularities|isolated singularity]] at $z=a$ (so $\exists R>0$ such that $f$ is [[Holomorphicity|holomorphic]] on $B^{*}_{R}(a)$). This singularity is a pole of order $k$ iff there exists a holomorphic function $g:B_{R}(a)\to \mathbb{C}$ with $g(a)\neq 0$ such that
$$
f(z)=(z-a)^{-k}g(z)
$$
For $z\in B_{R}^{*}(a)$
### Proof
If $f$ has a pole of order $k$, then on $B_{R}^{*}(a)$, it has a [[Laurent series|Laurent series]] of the form
$$
f(z)=\sum_{n=-\infty}^{\infty}c_{n}(z-a)^{n}=(z-a)^{-k}\sum_{n=-k}^{\infty}c_{n}(z-a)^{n+k} 
$$
$$
= (z-a)^{-k}\sum_{m=0}^{\infty} c_{m-k}(z-a)^{m}
$$
Which is a [[power series|power series]], so it is holomorphic on $B_{R}(0)$
Define $g(z)=\sum_{m=0}^{\infty}c_{m-k}(z-a)^{m}$, then $g$ is holomorphic with $g(a)=c_{-k}\neq 0$
For the other direction, we just do the same in reverse. If $g$ is holomorphic, then $g$ has a [[Taylor series|Taylor series]] by [[Cauchy-Taylor Theorem|Cauchy-Taylor]], so 
$$
f(z)=(z-a)^{-k}\sum_{m=0}^{\infty}d_{m}(z-a)^{m}
$$
So yeah
## Observation
Assume $h$ has a zero of order $k$ at $z=a$, then by the [[Order of a Zero|characterisation lemma for zeros]], there exists a $g$ holomorphic with $g(a)\neq 0$, such that $h(z)=(z-a)^{k}g(z)$ on $B_{R}(a)$, then by [[Continuity|continuity]], then theree exists $B_{r}(a)$ on which $g(z)\neq 0$, but then,
$$
f(z)=\frac{1}{h(z)}=(z-a)^{-k} \frac{1}{g(z)}
$$
But actually, $\frac{1}{g(z)}$ is holomorphic and nonzero on $B_{r}(a)$
So $f$ has a pole of order $k$ at $z=a$, so we can think of poles as being created by reciprocals of functions, and it turns out, this is the only way they can come about
## Proposition
Suppose $f$ has an isolated singularity at $z=a$ then it is a pole iff there exists $r>0$ and a holomorphic function $h:B_{r}(a)\to \mathbb{C}$ such that $f(z)=\frac{1}{h(z)}$ on $B_{r}^{*}(a)$ and $h$ has a zero of order $k$ at $z=a$
### Proof
For the converse direction, we found this in the above observation.
For the forward, suppose $f$ has a pole at $z=a$ and let $R>0$ be such that $f$ is holomorphic on $B_{R}^{*}(a)$, then by the characterisation lemma for poles, there exists $g:B_{R}(a)\to \mathbb{C}$ uch that $g(a)\neq 0$ and $f(z)=(z-a)^{-k}g(z)$ for $z\in B_{R}^{*}(a)$
By continuity, there exists $r>0$ such that $g(z)\neq 0$ on $B_{r}(a)$ and so the function
$$
h(z):= \frac{1}{f(z)}=(z-a)^{k} \frac{1}{g(z)}
$$
Where $\frac{1}{g(z)}$ is holomorphic and not zero, which satisfiess the property of having a zero of order $k$
Finally, note on $B_{r}^{*}(a)$, $f(z)=\frac{1}{h(z)}$ yay
## Remark
Almost all function we see will look like
$$
f(z)= \frac{g(z)}{h(z)}
$$
For holomorphic $g,h$
Thankfully we have a helpful corollary to deal with these
## Corollary
Let $g,h$ be holomorphic on some domain $D$. Let
$$
S_{g}:=\left\{ z\in D:\middle|: g(z)=0 \right\}
$$
$$
 S_{h}:=\left\{ z\in D:\middle|: h(z)=0 \right\}
$$
Then the function $f:D\setminus S_{h}\to \mathbb{C}$ defined by
$$
f(z)= \frac{g(z)}{h(z)}
$$
Is holomorphic with isolated singularities at all $z\in S_{h}$
Moreover, the singularity at a point $z=a$ is a pole of order $k$ if $a\in S_{h}\setminus S_{g}$ and $a$ is a zero of $h$ of order $k$
Also $f$ has a zero of order $k$ at $z=a$ if $a\in S_{g}\setminus S_{h}$ and $a$ is a zero of $g$ of order $k$
If $a\in S_{g}\cup S_{h}$ then investigate further
## Example
An example to aim for is $f(z)= \frac{\tan z}{z}=\frac{\sin z}{z\cos z}$ this might me kinda miserable to reciprocate and take lots of derivatives and stuff which makes us sad, but thanks to the corollary, we need to find the zeros of $f(z)=\sin z$ and $g(z)=z\cos z$, so
$$
\sin z=0 \iff \frac{e^{ iz }-e^{ -iz }}{2i}=0 \iff e^{ iz }=e^{ -iz }
$$
$$
\iff e^{ 2iz }=1 \iff 2iz=2\pi ni \iff z=n\pi
$$
For $n\in\mathbb{Z}$
And the zeros of $g$ are $z=0$ or $z=\frac{\pi}{2}+n\pi$ for $n \in \mathbb{Z}$ since
$$
\frac{d }{dz}z\cos z \big{|}_{z= \frac{\pi}{2}+n\pi}\neq 0
$$
and $f$ has zeros at $z=n\pi$ of order $\hspace{0pt}1$ since,
$$
\frac{d }{dz}\sin z \big{|}_{z=n\pi}=\cos(n\pi)=(-1)^{n}\neq 0
$$
At $z=0$ we need to investigate. Note that
$$
\lim_{ z \to 0 } zf(z)=\lim_{ z \to 0 }  \frac{\sin z}{\cos z}= \frac{\sin 0}{\cos 0}=\frac{0}{1}=0
$$
So it is a removable singularity
## Proposition
Suppose $f$ has an isolated singularity at $z=a$, then the singularity is a pole iff
$$
\lim_{ z \to a }  \left| f(z) \right| =\infty
$$
### Proof
Assume $f$ has a pole at $z=a$, then there exists $g$ which is holomorphic satisfying $g(a)\neq 0$ such that
$$
f(z)=\frac{1}{(z-a)^{k}}g(z)
$$
Then by continuity, there exists $B_{r}(a)$ such that $\left| g(z) \right|\geq M>0$ on $B_{r}(a)$, sooo
$$
\lim_{ z \to a } \left| f(z) \right| =\lim_{ z \to a }  \frac{1}{\left| z-a \right| ^{k}}\left| g(z) \right| \geq M\lim_{ z \to a }  \frac{1}{\left| z-a \right| ^{k}}=M\cdot \infty=\infty
$$
For the converse, if 
$$
\lim_{ z \to a } \left| f(z) \right| =\infty
$$
Then $\exists r>0$ such that $f(z)\neq 0$ when $z\in B^{*}_{r}(a)$
We consider the reciprocal $h(z)=\frac{1}{f(z)}$ which is holomorphic also on $B_{r}^{*}(a)$ and moreover,
$$
0\leq \left| (z-a)h(z) \right| \leq \frac{\left| z-a \right| }{\left| f(z) \right| }
$$
Which we can show tends to zero as $z\to a$ so yay