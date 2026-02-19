## Contour Integration
Let $U\subseteq \mathbb{C}$ be an [[open sets|open set]] and let $f:U\to \mathbb{C}$ be a [[Continuity|continuous]] [[functions|function]]. Let $\gamma:[a,b]\to U$ be $C^{1}$. Then we define the [[Integration|integral]] of $f$ along the curve $\gamma$ by its contour integral:
$$
\int _{\gamma}f(z) \, dz:=\int ^{b}_{a} f(\gamma(t))\gamma'(t) \, dt  
$$
If $\gamma:[a,b]\to U$ is a contour with partition $a=a_{0}<a_{1}<\dots<a_{n}=b$ such that $\gamma |_{[a_{i-1},a_{i}]}\to \mathbb{C}$ are $C^{1}$ curves for $i=1,\dots,n$, then we define
$$
\int _{\gamma}f(z) \, dz=\sum_{i=1}^{n} \int _{\gamma_{i}}f(z) \, dz 
$$
## Remark
Since $f\circ\gamma$ is a continuous function from $[a,b]$ to $U$ when $f$ and $\gamma$ are continuous, our definition is valid
___
To be very precise, we need to check that the definition of integration over controus is independent of the partition (since we can always refine a given partition)
This is similar to the standard theory of Riemann integration
___
Note that integration in this form is not as simple as [[Line Integrals|line integration]] as the dot product and complex multiplication are not comparable
## Lemma: Basic Properties
Assuming that $f_{1}$ and $f_{2}$ are continuous on $U$, we find that for any $C^{1}$ cuve $\gamma:[a,b]\to U$:
$$
\int _{\gamma}f_{1}(z)+f_{2}(z) \, dz=\int _{\gamma}f_{1}(z) \, dz+\int _{\gamma}f_{2}(z) \, dz
$$
For any $c\in \mathbb{C}$:
$$
 \int _{\gamma} cf_{1}(z) \, dz = c\int _{\gamma}f_{1}(z) \, dz 
$$
Defining $(-\gamma):[-b,-a]\to U$ by $(-\gamma)(t)=\gamma(-t)$, wee have that
$$
\int _{\gamma}f(z) \, dz=-\int _{-\gamma}f(z) \, dz  
$$
![[Pasted image 20260219171904.png]]
## Example
Consider the path $\gamma:[0,2\pi]$ defined by $\gamma(\theta)=re^{ i\theta }$ with $r>0$, find $\int _{\gamma} \, dz$ and $\int _{\gamma}\overline{z} \, dz$
We see that $\gamma'(\theta)=ire^{ i\theta }$, so by definition
$$
\int _{\gamma} \, dz=\int_{0}^{2\pi} ire^{ i\theta } \, d\theta =ir \left( \int_{0}^{2\pi} \cos\theta \, d\theta+i\int_{0}^{2\pi} \sin\theta \, d\theta \right)=0
$$
$$
 \int _{\gamma}\overline{z} \, dz = \int_{0}^{2\pi} (re^{ -i\theta })ire^{ i\theta } \, d\theta = ir^2 \int_{0}^{2\pi}   \, d\theta    =2\pi ir^{2}
$$

___
Consider a path $\gamma:[0,2\pi]\to \mathbb{C}$ by $\gamma(\theta)=a+re^{ i\theta }$ with $a\in\mathbb{C}$ and $r>0$, find $\int _{\gamma}(z-a)^{n} \, dz$ for $n\in\mathbb{Z}$
$$
\int _{\gamma}(z-a)^{n} \, dz=\int_{0}^{2\pi} (\gamma(\theta)-a)^{n}\gamma'(\theta) \, d\theta 
$$
$$
= \int_{0}^{2\pi} (re^{ i\theta })^{n}ire^{ i\theta } \, d\theta =\int_{0}^{2\pi} r^{n }e^{ in\theta }ire^{ i\theta } \, d\theta 
$$
$$
= ir^{n+1}\int _{0}^{2\pi} e^{ i(n+1)\theta } \, d\theta=ir^{n+1}\left[ \int_{0}^{2\pi} \cos((n+1)\theta) \, d\theta+i\int_{0}^{2\pi} \sin((n+1)\theta) \, d\theta   \right]    
$$
$$
= \begin{cases}
ir^{0}\left( \int_{0}^{2\pi} \cos(0) \, d\theta +i\int_{0}^{2\pi} \sin(0) \, d\theta  \right) & n+1=0 \\
ir^{n+1}\left( \frac{\sin((n+1)\theta)}{n+1}\Bigg{|}_{0}^{2\pi}-i \frac{\cos((n+1)\theta)}{n+1}\Bigg{|}_{0} ^{2\pi}   \right) & n+1\neq 0 
\end{cases}
$$
$$
=\begin{cases}
2\pi i & n=-1 \\
0 & n\in\mathbb{Z}\setminus \left\{ -1 \right\}
\end{cases}
$$
___
Motivated by this, we might ask the following: given an image of a curve in $\mathbb{C}$ (for instance a circle), can we define an integration on its image or does the parametrisation of it matter? For instance, the maps $\delta:[0,1]\to \mathbb{C}$ and $\gamma:[0,2\pi]\to \mathbb{C}$ defined by
$$
\delta(t)=re^{ 2\pi it },~\gamma(\theta)=re^{ i\theta }
$$
Five us the same image and direction of movement - a circle of radius $r$ in the anticlockwise direction
We saw above 
$$
    \int _{\gamma}\overline{z} \, dz=2\pi ir^{2}
$$
So let's compute the same integral over $\delta$: we have that $\delta'(t)=r(2\pi i)e^{ 2\pi it }$ and as such
$$
\int _{\delta} \overline{z} \, dz = \int_{0}^{1} (re^{ -2\pi it })(2\pi ir)e^{ 2\pi it } \, dt=2\pi ir^{2}\int_{0}^{1}  \, dt=2\pi ir^{2}  
$$
It seems to have worked yay, does it do so in general?
## Lemma: Reparamerisation of Curves
Let $U\subset \mathbb{C}$ be an open set, $f:U\to \mathbb{C}$ be continuous and let $\gamma:[a,b]\to \mathbb{C}$ be a $C^{1}$ curve. If $\varphi:[a',b']\to [a,b]$ is a continuously differentiable bijection with $\varphi(a')=a,\varphi(b')=b$ and we define $\delta:[a,b]\to \mathbb{C}$ by
$$
\delta(t):=\gamma(\varphi(t))=(\gamma \circ \varphi)(t)
$$
Then
$$
\int _{\gamma}f(z) \, dz=\int _{\delta}f(z) \, dz  
$$
### Proof
$$
\int _{\delta}f(z) \, dz=\int_{a'}^{b'} f(\delta(t))\delta'(t) \, dt      = \int ^{b'}_{a'} f(\gamma(\varphi(t)))\gamma'(\varphi(t)) \, dt
$$
Changing variables,
$$
=\int _{\varphi(a')}^{\varphi(b')} f(\gamma(s)) \, ds = \int ^{b}_{a} f(\gamma(s)) \, ds = \int _{\gamma}f(z) \, dz   
$$

## Remark
The requirement that $\varphi$ is a bijection is important, we might have that the curves are the same, but they wrap around multiple times or sommet
## Notation
Given a domain $D$ such that there exists a bijective contour $\gamma:[a,b]\to \partial D$ with a continuous inverse $\gamma ^{-1}:\partial D\to[a,b]$ and such that $\gamma'(t)\neq 0$, we define
$$
\int _{\partial D}f(z) \, dz=\int _{\gamma}f(z) \, dz  
$$
Where we assume that we start at $\gamma(a)$ and end at $\gamma(b)$ (a prescribed direction). This notion is well defined and doesn't depend on $\gamma$ due to our reparametrisation of curves lemma
When the boundary has no end points, such as the circle, we can extend to above definition to the case where $\gamma:[a,b)\to \partial D$ has the previously mentioned properties and $\gamma(a)=\gamma(b)$
## Example
When $D=B_{r}(a)$ with $a\in \mathbb{C}$ and $r>0$, we have that
$$
\partial D=\left\{ z\in  \mathbb{C}:\middle|: \left| z-a \right| =r \right\}
$$
Which is the bijective image of the $C^{1}$ curve $\gamma:[0,2\pi)\to \mathbb{C}$
$$
\gamma_{a,r}(\theta)=a+re^{ i\theta }
$$
Going int he anticlockwise direction. Consequently,
$$
\int _{\left| z-a \right| =r}f(z) \, dz = \int_{0}^{2\pi} f(a+re^{ i\theta })ire^{ i\theta } \, d\theta  
$$
## Definition: Concatenation of Countours
Let $\gamma:[a,b]\to \mathbb{C}$ and $\delta:[c,d]\to \mathbb{C}$ be two conttours such that $\gamma(b)=\delta(c)$. The addition of these contours, denoted by $\gamma \cup\delta$ is the contour defined by $\gamma \cup\delta:[a,b+d-c]\to \mathbb{C}$ by
$$
\gamma \cup\delta:= \begin{cases}
\gamma(t) & a\leq t\leq b \\
\delta(t+c-b) & b\leq t\leq b+d-c
\end{cases}
$$
![[Pasted image 20260219175855.png]]
## Lemma
Let $f:U\to \mathbb{C}$ be a continuous function and let $\gamma:[a,b]\to U$ and $\delta:[c,d]\to U$ be two controus such that $\gamma(b)=\delta(c)$
