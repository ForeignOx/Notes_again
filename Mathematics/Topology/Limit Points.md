## Definition
Let $X$ be a [[Topology|topological space]] and $A\subseteq X$. An element $x\in X$ is called a limit point of $A$, if every neighbourhood $N$ of $x$ satisfies $(N\setminus \left\{ x \right\})\cap A\neq \emptyset$

Notice that in this definition, we remove $x$ from the neighbourhood before we intersect with $A$. If we only demanded $N\cap A\neq \emptyset$, any element of $a$ will be a limit point
## Example
Let $A\subseteq \mathbb{R}$ be given by
$$
A=\left\{ \frac{1}{n}\in \mathbb{R}:\middle|: n\in\mathbb{N} \right\}
$$
0 is the only limit point of $A$. Any neighbourhood of $0$ contains $(-\varepsilon,\varepsilon)$ for some $\varepsilon>0$, since $(0,\varepsilon)\cap A\neq \emptyset$, $0$ is a limit point
## Lemma
Let $X$ be a topological space and $A\subset X$, then
$$
\overline{A}=A\cup \left\{ a\in  X :\middle|:a\text{ is a limit point of }A\right\}
$$
### Proof
Let $x\in \overline{A},$ we need to show that $x \in A$ or $x$ is a limit point of $A$, so assume $x\not\in A$, let $N$ be an open [[Neighbourhoods|neighbourhood]] of $x$. If $N\setminus \left\{ x \right\}\cap A=\emptyset$, then $A\subseteq X\setminus N$
But $X\setminus N$ is a closed set, which implies $\overline{A}\subseteq X\setminus N$, since $x\in N$, we have $x\not\in \overline{A}$, giving a contradiction
For the other inclusion, note that $A\subseteq \overline{A}$ by construction, so it only remains to show that any limit points of $A$ are also contained in $\overline{A}$
So let $x$ be a limit point of $A$, if $x\not\in \overline{A}$, then $N=X\setminus \overline{A}$ is an open neighbourhood of $x$
But since $A\subseteq \overline{A}$, we must have $N\cap A=\emptyset$, contradicting that $x$ is a limit point of $A$
## Proposition
Let $X,Y$ be topological spaces and $f:X\to Y$ be a function, the following are equivalent:
- $f$ is continuous
- We have $f(\overline{A})\subseteq \overline{f(A)}$ for all $A\subseteq X$
- We have $\overline{f^{-1}(B)}\subseteq f^{-1}(\overline{B})$ for all $B\subseteq Y$
### Proof

