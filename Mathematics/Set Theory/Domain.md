A variable used in mathematics is not allowed to take all objects as values, it can only take as values the members of a certain [[Sets|set]], called the domain of the variable
## Restricted Variables
Using a domain in a [[Proposition|proposition]] can restrict quantifiers, for example $\exists n\in \mathbb{N}$ or $\forall n\in \mathbb{Z}$ etc.
Resticted variables can be defined as abbreviations of unrestricted variables by:
$$
(\forall x\in  A)P(x) \iff (\forall x)(x\in  A\implies P(x))
$$
$$
 (\exists x\in  A)P(x) \iff (\exists x)(x\in  A \cap P(x))
$$
$$
 \left\{ x\in A\mid P(x) \right\}= \left\{ x\mid x\in  A\cap P(x) \right\}
$$
Sometimes restricting phrases are written in superscript position, for example $(\forall\varepsilon^{>0})(\exists n^{\in\mathbb{Z}})$
## Domains of Relations
The set of all first elements occuring in the [[Ordered Pairs|ordered pairs]] of a [[Relations|relation]] $R$ is called the domain of $R$ and is designated $\text{dom}(R)$ or $\mathfrak{D}(R)$, thus
$$
\mathfrak{D}(R)=\left\{ x\mid(\exists y)(x,y)\in  R \right\}
$$


#Mathematics #Logic #Set