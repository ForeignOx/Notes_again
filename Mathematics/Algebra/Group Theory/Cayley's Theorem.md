## Theorem
Every finite [[Groups|group]] is [[Isomorphisms|isomorphic]] to a [[Subgroups|subgroup]] of some [[Symmetric Groups|symmetric group]]
### Proof
Consider the [[Homomorphisms|homomorphism]] $\varphi:G\to S_{G}\cong S_{n}$ defined by setting $\varphi(g)$ for any $x\in X$ to $g*x$. We will show that $\varphi$ is [[Injective Functions|injective]]; [[Kernel|$\text{ker}(\varphi)=\left\{ e \right\}$]]. By the [[First Isomorphism Theorem|First Isomorphism Theorem]], if $\varphi:G\to H$ is a homomorphism, then
$$
G /\text{ker}(\varphi)\cong \text{im}(\varphi)
$$
So $G\cong \text{im}(\varphi)\subseteq S_{n}$ which would mean that $G$ is isomorphic to a subgroup of $S_{n}$
To show that $\varphi$ is injective, suppose that $\varphi(g)=e$, for some $g\in G$, then
$$
\varphi(g)h=g*h=gh\forall h\in  G
$$
$$
\implies \varphi(g)h=h 
$$
So $gh=h$, so $g=e$, so $\varphi$ is injective as required

#Mathematics #Theorem