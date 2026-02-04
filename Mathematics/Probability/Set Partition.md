## Definition
A partition of a [[Sets|set]] $A$ is a [[Disjoint Families of Sets|disjoint]] family $\mathfrak{F}$ of sets whose [[Union|union]] is $A$
We call the elements of $\mathfrak{F}$ fibres, and we say that $\mathfrak{F}$ fibres $A$, or is a fibering of $A$
If $\overline{x}$ designates the unique fiber containing the point $x$, then $x\mapsto \overline{x}$ is a [[Surjective Functions|surjective]] [[Functions|mapping]] $\pi:A\to \mathfrak{F}$ which we call the projection of $A$ on $\mathfrak{F}$
Passing from a set $A$ to a fibering $\mathfrak{F}$ of $A$ is one of the principle ways of forming new mathematical objects
## Examples
The set of straight lines parallel to a given line in the Euclidean plane is a fibering of the plane
## Generating a Fibering
Any function $f$ automatically fibers its [[Domain|domain]] into sets on which $f$ is contant
For example, if $A$ is the Euclidean plane and $f(p)$ is the $x$-coordinate of the point $p$ in some coordinate system, then $f$ is constant on each vertical line; more exactly, $f^{-1}(x)$ is a vertical line for every $x\in \mathbb{R}$. Moreover $x\mapsto f^{-1}(x)$ is a [[Bijective Functions|bijection]] from $\mathbb{R}$ to the set of all fibers
In general, if $f:A\to B$ is any surjective mapping, and if for each value $y$ in $B$ we set:
$$
A_{y}=f^{-1}(y)=\left\{ x\in  A::\middle| :dle|: f(x)=y \right\}
$$
Then $\mathfrak{F}=\left\{ A_{y}::\middle| :dle|: y\in B \right\}$ is a fibering of $A$ and $\varphi: y\mapsto A_{y}$ is a bijection from $B$ to $\mathfrak{F}$
Also [[Composition of Functions|$\varphi \circ f$]] is the projection $\pi:A\to \mathfrak{F}$, since $\varphi \circ f(x)=\varphi(f(x))$ is the set $\overline{x}$ of all $z$ in $A$ such that $f(z)=f(x)$
___
The above process of generating a fibering of $A$ from a function on $A$ is relatively trivial, a more important way is by using an [[Equivalence Relation|equivalence relation]]
Every fibering $\mathfrak{F}$ of $A$ generates a relation $\sim$ by the stipulation that $x\sim y$ iff $x$ and $y$ are in the same fiber, and the more important fact is the converse:
### Theorem
Every equivalence relation $\sim$ on $A$ is the equivalence relation of a fibering
#### Proof
We obviously have to define $\overline{x}$ as the set of elements $y$ equivalent to $x$, $\overline{x}=\left\{ y:\middle| : y\sim x \right\}$, and our problem is to show that the family $\mathfrak{F}$ of all [[Subsets|subsets]] of $A$ obtained this way is a fibering.
The reflective, symmetric and transitive laws become:
$$
x\in  \overline{x}, x\in  \overline{y}\implies y\in  \overline{x}, x\in  \overline{y}\text{ and }y\in  \overline{z}\implies x\in  \overline{z}
$$
Reflexivity thus implies that $\mathfrak{F}$ covers $A$, transitivity says that $\overline{y}\subseteq \overline{z}$, but also by performing the reverse implication, which we can do by symmetry, we get $\overline{z} \subseteq \overline{y}$, thus $y\in \overline{z}$ implies $\overline{y}=\overline{z}$
Therefore if two of our sets $\overline{a}$ and $\overline{b}$ have a point $x$ in common, then $\overline{a}=\overline{x}=\overline{b}$. In other words, if $\overline{a}$ is not the set $\overline{b}$, then $\overline{a}$ and $\overline{b}$ aredisjoint, and we have a fibering
### Examples
The fundamental role this argument plays in mathematics is due to the fact that in many important situations, equivalence relations occur as the primary object, and then are used to define partitions and functions
___
For example, consider [[Integers|$\mathbb{Z}$]]. A fraction $\frac{m}{n}$ can be considered an [[Ordered Pairs|ordered pair]] $(m,n)$ of integers with $n\neq 0$. The set of all fractions is thus $\mathbb{Z}\times(\mathbb{Z}\setminus \left\{ 0 \right\})$
Two fractions $(m,n)$ and $(p,q)$ are "equal" if and only if $mq=np$ and the equality is checked to be an equivalence relation
The equivalence class $\overline{(m,n)}$ is the object taken to be the rational numbeer $\frac{m}{n}$, thus the rational number system [[Rational Numbers|$\mathbb{Q}$]] is th set of fibers in a partition of $\mathbb{Z}\times(\mathbb{Z}\setminus \left\{ 0 \right\})$
___
Next we choose a fixed integer $p \in \mathbb{Z}$ and define a relation $E$ on $\mathbb{Z}$ by $mEn \iff p$ divides $m-n$
Then $E$ is an equivalence relation, and the set $\mathbb{Z} /p$ of its equivalence classes is the [[Integers Modulo n|integers modulo $p$]]
It is easy to see that $mEn$ if and only $f$ $m$ and $n$ have the same remainder when divided by $p$, so that in this case, there is an easily calculated function $f$, where $f(m)$ is the remainder after dividing $m$ by $p$, which defines the fibering
The set of possible remainders is $\left\{ 0,1,\dots,p-1 \right\}$, so that $\mathbb{Z} /p$ contains $p$ elements
A function on a set $A$ can be "factored" through a fibering of $A$ by the following theorem
## Theorem
Let $g$ be a function on $A$, and let $\mathfrak{F}$ be a fibering of $A$. Then $g$ is constant on each fiber of $\mathfrak{F}$ if and only if there exists a function $\overline{g}$ on $\mathfrak{F}$ such that $g=\overline{g} \circ \pi$ 
### Proof
If $g$ is constant on each fiber of $\mathfrak{F}$, then the association of this unique value with the fiber defines the function $\overline{g}$, and clearly $g=\overline{g}\circ \pi$. The converse is obvious
## For Probability
The [[Sets|sets]] $E_{1},E_{2},\dots,E_{k}\in\mathfrak{F}$ form a finite partition of the [[Sample Spaces|sample space]] $\Omega$ if it satisfies the following properties:
- $\mathbb{P}(E_{i})>0$ for all $1\leq i\leq k$
- $E_{i}$ and $E_{j}$ are pairwise disoint, i.e. $\forall i\neq j,E_{i}\cap E_{j}=\emptyset$
- $\Omega=\bigcup_{i=1}^k E_{i}$
An easy upshot of this is that $\sum_{i=1}^k\mathbb{P}(E_{i})=1$ this is true since
$$
\Omega=\bigcup_{i=1}^kE_{i}
$$
$E_{i}$ are pairwise [[Mutual Exclusivity|mutually exclusive]], so we can take the probability of both sides to get
$$
1=\mathbb{P}\left( \bigcup_{i=1}^k E_{i}\right)=\sum_{i=1}^k(\mathbb{P}(E_{i}))
$$

#Mathematics #Probability #Set #Definition 