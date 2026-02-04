Consider a [[Continuity|continuous]] [[Functions|function]] $f(x)$ on the [[Intervals|interval]] $[a,b]$ such that
$$
\int ^{b}_{a} f(x)g(x) \, dx =0
$$
For all smooth $g(x)$ in $[a,b]$ with $g(a)=g(b)=0$. Then $f(x)=0\forall x\in(a,b)$
## Proof
By contradiction. Assume that $f(x)>0$ for some $x\in(a,b)$
Continuity implies that there is an interval $[p_{0},p_{1}]$ such that $f(x)>\epsilon$ for some $\epsilon>0$ for all $x\in[p_{0},p_{1}]$
Choose 
$$
g(x)=\begin{cases}
\nu(x-p_{0})\nu(p_{1}-x)  & x\in [p_{0},p_{1}]\\
0 & \text{otherwise}
\end{cases}
$$
This looks like a little bump, $g(x)$ is smooth
$$
\int ^{b}_{a} f(x)g(x) \, dx =\int_{p_{0}}^{p_{1}} f(x)g(x) \, dx 
$$
$$
 > \epsilon \int_{p_{0}}^{p_{1}} g(x) \, dx >0
$$
This is a contradiction