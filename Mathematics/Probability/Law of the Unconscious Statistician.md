This relates [[Expectation|$\mathbb{E}(X)$]] to the pmf or pdf
$$
\mathbb{E}(g(X))=\sum_{x}g(x)p(x)
$$
$$
 E\left( g(X) \right)=\int_{-\infty}^{\infty} g(x)f(x) \, dx 
$$
## Multiple r.v.
$$
(X,Y):\Omega\to \mathbb{R}^{2}
$$
$$
 g:\mathbb{R}^{2}\to \mathbb{R}
$$
Then
$$
\mathbb{E}(g(x,y))=\sum_{x}\sum_{y}g(x,y)p(x,y)
$$
Where $(X,Y)$ is jointly discrete with the joint pmf of $p(\cdot,\cdot)$, or for continuous:
$$
\mathbb{E}(g(X,Y))=\int_{-\infty}^{\infty} \int_{-\infty}^{\infty} g(x,y)f(x,y) \, dy \, dx 
$$

