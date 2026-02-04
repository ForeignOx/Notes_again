Suppose we have two [[Random Variables|random variables]]
$$
X:\Omega\to \mathbb{R}
$$
$$
Y:\Omega\to \mathbb{R}
$$
Then the covariance of $X$ and $Y$ is related to [[Expectation|expextation]] and is defined as:
$$
\mathbb{C}\mathrm{ov}(X,Y):=\mathbb{E}((X-\mathbb{E}(X))(Y-\mathbb{E}(Y)))
$$
If $\mathbb{C}\mathrm{ov}(X,Y)>0$, then $X$ and $Y$ are positively [[Correlation|correlated]]
If $\mathbb{C}\mathrm{ov}(X,Y)<0$, then $X$ and $Y$ are negatively correlated
Intuition: suppose $\mathbb{E}(X)=\mathbb{E}(Y)=0$, then $\mathbb{C}\mathrm{ov}(X,Y)=\mathbb{E}(XY)$
___
## $\mathbb{C}\mathrm{ov}(X,Y)=\mathbb{E}(XY)-\mathbb{E}(X)\mathbb{E}(Y)$
Proof:
$$
\mathbb{C}\mathrm{ov}(X,Y)=\mathbb{E}((X-\mathbb{E}(X))(Y-\mathbb{E}(Y)))=\mathbb{E}(XY-X\mathbb{E}(Y)-Y\mathbb{E}(X)+\mathbb{E}(X)\mathbb{E}(Y))
$$
Which by linearity gives:
$$
= \mathbb{E}(XY)-\mathbb{E}(X)\mathbb{E}(Y)-\mathbb{E}(X)\mathbb{E}(Y)+\mathbb{E}(X)\mathbb{E}(Y)=\mathbb{E}(XY)-\mathbb{E}(X)\mathbb{E}(Y)
$$

___
By LOTUS, for [[Discrete Random Variables|discrete]]
$$
\mathbb{C}\mathrm{ov}(X,Y)=\sum_{x}\sum_{y}(x-\mathbb{E}(X))(y-\mathbb{E}(Y))p(x,y)
$$
for [[Continuous Random Variables|continuous]]:
$$
\mathbb{C}\mathrm{ov}(X,Y)=\int_{-\infty}^{\infty} \int_{-\infty}^{\infty} (x-\mathbb{E}(X))(y-\mathbb{E}(Y))f(x,y) \, dx  \, dy 
$$
___
Note that [[Variance|variance]] is related in such a way:
$$
\mathbb{C}\mathrm{ov}(X,X)=\mathbb{E}((X-\mathbb{E}(X))(X-\mathbb{E}(X)))=\mathbb{E}((X-\mathbb{E}(X))^{2})=\mathbb{V}\mathrm{ar}(X)
$$
___
Covariance is symmetric, that is:
$$
\mathbb{C}\mathrm{ov}(X,Y)=\mathbb{C}\mathrm{ov}(Y,X)
$$
Which directly follows from the definition
___
Let $X,Y,Z$ be random variables, $\alpha,\beta,\gamma,\delta \in\mathbb{R}$,
$$
\mathbb{C}\mathrm{ov}(\alpha+\beta X,\gamma+\delta Y)=\beta\delta \mathbb{C}\mathrm{ov}(X,Y)
$$
$$
\mathbb{C}\mathrm{ov}(X+Y,Z)=\mathbb{C}\mathrm{ov}(X,Z)+\mathbb{C}\mathrm{ov}(Y,Z)
$$
$$
\mathbb{C}\mathrm{ov}(X,Y+Z)=\mathbb{C}\mathrm{ov}(X,Y)+\mathbb{C}\mathrm{ov}(X,Z)
$$
## Expecation
If $X$ and $Y$ are [[Independence|independent]], then $\mathbb{C}\mathrm{ov}(X,Y)=0$
### Proof
$$
\mathbb{C}\mathrm{ov}(X,Y)=\mathbb{E}(XY)-\mathbb{E}(X)\mathbb{E}(Y)
$$
When they are independent, $\mathbb{E}(XY)=\mathbb{E}(X)\mathbb{E}(Y)$, so
$$
\mathbb{C}\mathrm{ov}(X,Y)=\mathbb{E}(X)\mathbb{E}(Y)-\mathbb{E}(X)\mathbb{E}(Y)=0
$$
The converse is not true;
$$
\mathbb{P}((X,Y)=(1,0))=\mathbb{P}((X,Y)=(0,1))=\mathbb{P}((X,Y)=(0,-1))=\mathbb{P}((X,Y)=(-1,0))=\frac{1}{4}
$$
So
$$
\mathbb{P}(XY=0)=1
$$
So $\mathbb{E}(XY)=0$, and we can find $\mathbb{E}(X)=\mathbb{E}(Y)=0$
But
$$
\mathbb{P}(X=1,Y=1)=0\neq \mathbb{P}(X=1)\mathbb{P}(Y=1)
$$
$$
 \mathbb{P}(X=1)=\mathbb{P}(X=1,Y=0)=\frac{1}{4}
$$
Similarly $\mathbb{P}(Y=1)=\frac{1}{4}$
Hence $X$ and $Y$ are nt independent

