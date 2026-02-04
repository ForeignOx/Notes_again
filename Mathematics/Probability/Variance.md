$\mathbb{V}\mathrm{ar}(X)$ is the variance of a [[Discrete Random Variables|discrete random variable]] and tells us about the spread of the possible values of $X$, we calculate it like so:
$$
\mathbb{V}\mathrm{ar}(X)=\mathbb{E}((X-\mathbb{E}(X))^{2})=\mathbb{E}(X^2-2X\mathbb{E}(X)+\mathbb{E}(X)^2)
$$
$$
=\mathbb{E}(X^2)-\mathbb{E}(2X\mathbb{E}(X))+\mathbb{E}(\mathbb{E}(X)^{2})
$$
$\mathbb{E}(X)$ is a constant, so
$$
=\mathbb{E}(X^{2})-2\mathbb{E}(X)\mathbb{E}(X)+\mathbb{E}(X)^{2}
$$
$$
\mathbb{V}\mathrm{ar}(X)=\mathbb{E}(X^{2})-\mathbb{E}(X)^{2}
$$
It is useful to note that variance is the square of the [[Standard Deviation|standard deviation]], $\mathbb{V}\mathrm{ar}(X)=\sigma^{2}$
___
By LOTUS, taking $g(x)=(X-\mathbb{E}(x))^{2}$, for discrete,
$$
\mathbb{V}\mathrm{ar}(X)=\sum_{x}(x-\mathbb{E}(X))^{2}p(x)
$$
For continuous:
$$
\mathbb{V}\mathrm{ar}(X)=\int_{-\infty}^{\infty} (x-\mathbb{E}(X))^{2}f(x) \, dx 
$$

___
To find $\mathbb{V}\mathrm{ar}(f(X))$, where $f(X)$ is a function of X, we do:
$$
\mathbb{V}\mathrm{ar}(f(X))=\mathbb{E}(f(X)^{2})-\mathbb{E}(f(X))^{2}
$$
Usefully, this means:
$$
\mathbb{V}\mathrm{ar}(aX+b)=\mathbb{E}((aX+b)^{2})-\mathbb{E}(aX+b)^{2}
$$
$$
=\mathbb{E}(a^{2}X^{2}+2abX+b^{2})-(a\mathbb{E}(X)+b)^{2}
$$
$$
=a^{2}\mathbb{E}(X^{2})+2ab\mathbb{E}(X)+b^2-a^{2}\mathbb{E}(X)^{2}-2ab\mathbb{E}(X)-b^{2}
$$
$$
=a^{2}\mathbb{E}(X^{2})-a^{2}\mathbb{E}(X)^{2}=a^{2}\mathbb{V}\mathrm{ar}(X)
$$
$$
\implies \mathbb{V}\mathrm{ar}(aX+b)=a^{2}\mathbb{V}\mathrm{ar}(X)
$$
___
Consider two [[Discrete Random Variables|discrete random variables]] $X$ and $Y$, where
$$
p(x,y)=\mathbb{P}(X=x, Y=y)
$$
We can write
$$
\mathbb{V}\mathrm{ar}(X \pm Y)=\mathbb{E}(((X\pm Y)-\mathbb{E}(X\pm Y))^{2})
$$
$$
=\mathbb{E}((X- \mathbb{E}(X))\pm (Y-\mathbb{E}(Y))^{2})
$$
$$
=\mathbb{E}((X-\mathbb{E}(X))^{2}+(Y-\mathbb{E}(Y))^{2} \pm 2(X-\mathbb{E}(X))(Y-\mathbb{E}(Y)))
$$
$$
=\mathbb{E}((X-\mathbb{E}(X))^{2})+\mathbb{E}((Y-\mathbb{E}(Y))^{2})\pm \mathbb{E}(2(X-\mathbb{E}(X))(Y-\mathbb{E}(Y)))
$$
$$
=\mathbb{V}\mathrm{ar}(X)+\mathbb{V}\mathrm{ar}(Y)\pm 2\mathbb{C}\mathrm{ov}(X,Y)
$$
So if $X$ and $Y$ are independent, their [[Covariance|covariance]] will be 0, so we can write:
$$
\mathbb{V}\mathrm{ar}(X\pm Y)=\mathbb{V}\mathrm{ar}(X)+\mathbb{V}\mathrm{ar}(Y)
$$
Another way of showing this using properties of covariance is as follows:
$$
\mathbb{V}\mathrm{ar}(X+Y)=\mathbb{C}\mathrm{ov}(X+Y,X+Y)=\mathbb{C}\mathrm{ov}(X,X)+\mathbb{C}\mathrm{ov}(X,Y)+\mathbb{C}\mathrm{ov}(Y,X)+\mathbb{C}\mathrm{ov}(Y,Y)
$$
$$
= \mathbb{V}\mathrm{ar}(X)+\mathbb{V}\mathrm{ar}(Y)+2\mathbb{C}\mathrm{ov}(X,Y)
$$
Using this,
$$
\mathbb{V}\mathrm{ar}\left( \sum_{i=1}^{n}X_{i} \right)=\sum_{ i=1} ^{ n}\mathbb{V}\mathrm{ar}(X_{i})+2\sum_{i<j}\mathbb{C}\mathrm{ov}(X_{i},X_{j})
$$



#Mathematics #Statistics 