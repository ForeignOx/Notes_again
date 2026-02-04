## Real Inner Product Space
A [[Vectorspaces|real vectorspace]], $V$ equipped with an [[Inner Product|inner product]] $(\cdot,\cdot)$ is called a real inner product space
### Examples
$V=\mathbb{R}^{n}$ with usual Euclidian [[Dot Product|dot product]]
$$
(\underline{u},\underline{v})=\underline{u}\cdot \underline{v}=u_{1}v_{1}+u_{2}v_{2}+\dots+u_{n}v_{n}=\underline{v}^{\top}I\underline{u}
$$
___
Weighted inner product on $\mathbb{R}^{n}$:
$$
(\underline{u},\underline{v})=a_{1}u_{1}v_{1}+a_{2}u_{2}v_{2}+\dots+a_{n}u_{n}v_{n}
$$
With $a_{i}>0\forall i$, note that it would still be a reasonable [[Bilinear Form|bilinear form]] if the $a_{i}$'s were negative, but not an inner product
___
On $V=\mathbb{R}^{4}$, the expression $(\underline{x},\underline{y})=x_{1}y_{1}+x_{2}y_{2}+x_{3}y_{3}-x_{4}y_{4}$ is not an inner product: symmetry and bilinearity hold, but positivity does not. For example $\underline{x}=(1,0,0,1)$ is a non-zero vector with $(\underline{x},\underline{x})=0$. However, it is of great importance: from Einstein, we know that this is the pseudo-inner product on flat space-time, with $x_{4}$ being the time coordinate. The vectorspace with this pseudo-inner product is called Minkowski space
___
Take $V=C[a,b]$, the vector space of [[Continuity|continuous]] [[Functions|functions]] $f:[a,b]\to \mathbb{R}$ (we assume $a<b$). Now $V$ is [[Dimension|infinite dimensional]], and the zero vector is the function $f$ which is identically $\hspace{0pt}0$. Define
$$
(f,g)=\int ^{b}_{a}f(t)g(t)  \, dt
$$
This is an inner product, the first $\hspace{0pt}3$ properties follow from the properties of [[Integration|integration]], for the fourth,
$$
(f,f)=\int ^{b}_{a} (f(t))^{2} \, dt \geq 0
$$
Since $(f(t))^{2}\geq 0$, since it is a [[Real Functions|real-valued function]], but does $(f,f)=0\implies f=0$?
#### Proof
Suppose there exists $t_{0}\in[a,b]:f(t_{0})\neq 0$, take $c>0$. Since $f$ is continuous, there exists a small neighbourhood $(t_{0}-\delta,t_{0}+\delta):f(t)>\frac{c}{2}\forall t\in(t_{0}-\delta,t_{0}+\delta)$, then
$$
(f,f)=\int ^{b}_{a} f^{2}(t) \, dt \geq \int_{t_{0}-\delta}^{t_{0}+\delta} f^{2}(t) \, dt \geq \int_{t_{0}-\delta}^{t_{0}+\delta} \frac{c^{2}}{4} \, dt\geq \frac{c^{2}}{2}\delta>0 
$$
Giving us our contradiction

#Mathematics #LinAlg #Definition 