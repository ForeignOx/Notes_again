## Definition
Let $X$ be a topological space. A subset $A\subseteq X$ is called dense in $X$ if $\overline{A}=X$
It is called nowhere dense if $(\overline{A})^{0}=\emptyset$
## Example
Look at $\mathbb{Q}\subset \mathbb{R}$, what is $\overline{\mathbb{Q}}$, think of a closed set $A\subset  \mathbb{R}$ with $\mathbb{Q}\subset A$
Assume $A\neq \mathbb{R}$, then there is $x \in\mathbb{R}\setminus \mathbb{Q}$ with $x\in \mathbb{R}\setminus A$ which is an open set, so there is $\varepsilon>0$ such that $(x-\varepsilon,x+\varepsilon)\subseteq \mathbb{R}\setminus A\subseteq \mathbb{R}\setminus \mathbb{Q}$, which is not possible, so $\overline{\mathbb{Q}}=\mathbb{R}$
Then consider $\mathbb{Q}^{0}=\emptyset$ by a similar argument
The integers satisfy $\mathbb{Z}=\overline{\mathbb{Z}}$, and are nowhere dense in $\mathbb{R}$
## Lemma
Let $X$ be a topological space, and $B\subseteq A\subseteq X$, then
- We have $B^{0}\subseteq A^{0}$ and $\overline{B}\subseteq \overline{A}$
- If $B\subseteq X$ is open, then $B^{0}=B$, in particular $(A^{0})^{0}=A^{0}$
- Similarly if $B\subseteq X$, is closed, then $\overline{B}=B$, in particular, $\overline{\overline{A}}=\overline{A}$
