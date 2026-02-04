## Definition
If [[Vectorspaces|$V=\mathbb{R}^{I}$]] for some [[Sets of Indices|index set]] $I$, and $i\in I$, then the $i$th coordinate [[Linear Functionals|functional]] $\pi_{i}$ is simply evaluation at $i$, such that
$$
\pi_{i}(f)=f(i)
$$
These functionals are obviously [[Linear Maps|linear]]
In fact, the [[Vectors|vector]] operations on [[Functions|functions]] were defined to make sure this was linear; since $sf+tg$ is defined to be that function whose value at $i$ is $sf(i)+tg(i)$ for all $i$, we see that $sf+tg$ is by definition that function such that
$$
\pi_{i}(sf+tg)=s\pi_{i}(f)+t\pi_{i}(g)
$$
For all $i$
## Example
If $V$ is [[Vectorspace Rn|$\mathbb{R}^{n}$]], then $\pi_{j}$ is the mapping
$$
\underline{x}=(x_{1},x_{2},\dots,x_{n})\mapsto x_{j}
$$
In this case, we know from [[Linear Maps#Theorem|this theorem]] that $\pi_{j}$ must be of the form $\pi_{j}(\underline{x})=\sum_{i=1}^{n}b_{i}x_{i}$ for some $n$-tuple $\underline{b}=(\delta^{j},\delta^{j},\dots ,\delta^{j})$
