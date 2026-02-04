Let [[Natural Numbers|$n\in \mathbb{N}$]]. If we divide an [[Integers|integer]] by $n$, we always get a remainder $\in\left\{ 0,1,2,\dots,n-1 \right\}$.
When $a\in \mathbb{Z}$ is thought of as a remainder modulo $n$, we write it $\overline{a}$.
What is $\overline{a}$? It can't just be an integer, for example if $n=2$, then $\overline{0}=\overline{2}=\dots$, which means that we can't think of them as just numbers, we instead think of them as [[Sets|sets]]; in this example, we define $\overline{0}=\left\{ x\in \mathbb{Z}\mid x\equiv0\mod2 \right\}$, and $\overline{1}=\left\{ x\in \mathbb{Z}\mid x\equiv 1 \mod 2 \right\}$
## Definition
In general, we define:
$$
\overline{a}=\left\{ x\in  \mathbb{Z}\mid x\equiv a\mod n \right\}
$$
This is called a residue class/coset. There are precisely $n$ of these: $\overline{0},\overline{1},\dots,\overline{n-1}$. We deote this set by $\mathbb{Z}/n$. This set is in fact a commutative [[Rings|ring]] (i.e. $xy=yx$). To do this, we need our [[Binary Operations|binary operations]], $+,\cdot$:
$$
\overline{a}+\overline{b}:=\overline{a+b}
$$
$$
 \overline{a}\cdot \overline{b}:=\overline{ab}
$$
Thus, to define $+$ and $\cdot$ we have chosen $a$ and $b$ in $\mathbb{Z}$ as "representing" $\overline{a}$ and $\overline{b}$
This could potentially be problematic, as we might get a different result since $\overline{a}=\overline{a+n}$, so if we substituted $a+n$ to be our representations, we need that to be consistent - we need to be sure that the operations are indipendent of the choice of representatives. We leave the task of checking that $\mathbb{Z} /n$ is an abelian group as it will not be important (future oren pls fill(ik you didn't do very well last year :///))
Existance of a multiplicative identity is shown by $\overline{1}\in \mathbb{Z} /n$, we can show commutativity, associativity and distributivity all follow from the corresponding properties in $\mathbb{Z}$, for example with distributivity:
$$
\overline{a}(\overline{b}+\overline{c})=\overline{a}(\overline{b+c})=\overline{a(b+c)}=\overline{ab+ac}=\overline{ab}+\overline{ac}=\overline{a}\overline{b}+\overline{a}\overline{c}
$$
Another notation for $\overline{a}$ is $[a]_{n}$ which helps identify what $\overline{a}$ is modulo with respect to
## Example
Consider $\mathbb{Z} /3=\left\{ \overline{0},\overline{1},\overline{2} \right\}$, we can construct addition and multiplication tables:

| $+$            | $\overline{0}$ | $\overline{1}$ | $\overline{2}$ |
| -------------- | -------------- | -------------- | -------------- |
| $\overline{0}$ | $\overline{0}$ | $\overline{1}$ | $\overline{2}$ |
| $\overline{1}$ | $\overline{1}$ | $\overline{2}$ | $\overline{0}$ |
| $\overline{2}$ | $\overline{2}$ | $\overline{0}$ | $\overline{1}$ |

| $\cdot$        | $\overline{0}$ | $\overline{1}$ | $\overline{2}$ |
| -------------- | -------------- | -------------- | -------------- |
| $\overline{0}$ | $\overline{0}$ | $\overline{0}$ | $\overline{0}$ |
| $\overline{1}$ | $\overline{0}$ | $\overline{1}$ | $\overline{2}$ |
| $\overline{2}$ | $\overline{0}$ | $\overline{2}$ | $\overline{1}$ |
