## Theorem
Let $f$ have an [[Isolated Singularities|essential singularity]] at $z=a$ and let $R>0$ such that [[Complex Functions|$f$]] is [[Holomorphicity|holomorphic]] on $B_{R}^{*}(a)$, then for any $w\in \mathbb{C}$ and all $0<r<R$ and all $\varepsilon>0$ there exists $z\in B^{*}_{r}(a)$ such that $f(z)\in B_{\varepsilon}(w)$, or written another way,
$$
(\forall w_{\in  \mathbb{C}})(\forall r_{0<r<R})(\forall\varepsilon_{>0})(\exists B_{r}^{*}(a)): f(z)\in B_{\varepsilon}(w)
$$
You can think of this as being able to reach any point in the image of $f$ by getting closer to the essential singularity, or that the image around the singularity is dense in $\mathbb{C}$
### Proof
Argue by contradiction: that is, assume there is $b\in \mathbb{C}$ and $r>0$ and $\varepsilon>0$ such that $f$ is holomorphic on $B_{r}^{*}(a)$ but $f(z)\not\in B_{\varepsilon}(b)$ for every $z\in B_{r}^{*}(a)$
$$
f(z)\not\in B_{\varepsilon}(b)\implies \left| f(z)-b \right| \geq \varepsilon>0 ~\forall z\in  B_{r}^{*}(a)
$$
Considering $g(z)=\frac{1}{f(z)-b}$, this is holomorhpic on $B_{r}^{*}(a)$ and we have a bound below for the denominator so a bound above, i.e.
$$
\left| g(z) \right| =\frac{1}{\left| f(z)-b \right| }\leq \frac{1}{\varepsilon}
$$
So by the [[Riemann extension theorem|Riemann extension theorem]], $g$ extends to a holomorphic function at $z=a$
We extend it by giving $g$ a value at $z=a$
In the first case, $g(a)=0$, which would imply 
$$
f(z)= b+\frac{1}{g(z)}=\frac{bg(z)+1}{g(z)}
$$
Which means $f$ has a pole at $z=a$
Otherwise $g(a)\neq 0$, so
$$
\lim_{ z \to a }  (z-a)f(z)=\lim_{ z \to a }  \frac{(z-a)(bg(z)+1)}{g(z)}= \frac{(a-a)(b-g(a)+1)}{g(a)}=0
$$
So $f$ has a removable singularity at $z=a$ 