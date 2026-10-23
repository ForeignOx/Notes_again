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
\overline{A}=A\cup \left\{ a\in  X s:\middle|:a\text{ is a limit point of }A\right\}
$$
### Proof
Let $x\in \overline{A},$ we need to show that $\times \in A$ or $x$ is a limit pointof $A$, so assume $x\not\in X\setminus N$, but $$