## Definition
If we have [[Functions|functions]] $f:A\to B$ and $g:B\to C$, then the composition of $g$ with $f$, $g\circ f$ is the map of [[Sets|$A$]] into $C$ defined by
$$
(g\circ f)(x)=g(f(x))\,\forall x\in  A
$$
Note that the codomain of $f$ must be the [[Domain|domain]] of $g$ in order for $g\circ f$ to be defined
This operation can be thought of as the most basic binary operation of mathematics
## Associativity of Composition
Composition satisfies the associative law:
$$
f \circ (g\circ h)=(f\circ g)\circ h
$$
### Proof
$$
(f\circ (g\circ h))(x)=f((g\circ h)(x))=f(g(h(x)))=(f\circ g)(h(x))=((f\circ g)\circ h)(x)
$$
For all $x\in \text{dom}(h)$
## Definition for Relations
Composition can also be defined for [[Relations|relations]] as follows:
If $R\subset A\times B$ and $S\subset B\times C$, then $S\circ R\subset A\times C$ is defined by:
$$
(x,z)\in S\circ R \iff (\exists y^{\in  B})((x,y)\in  R\text{ and }(y,z)\in S)
$$
If $R$ and $S$ are mappings, the definition agrees with the above one

#Mathematics #Functions #Definition