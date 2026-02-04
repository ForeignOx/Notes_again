In general, if there are $n$ objects with $n_{1}$ of a first type, $n_{2}$ of a second type,..., and $n_{r}$ of an $r$th type, where $n_{1}+n_{2}+\dots+n_{r}=n$, then there are:
$$
P(n_{n}1,n_{2},\dots,n_{r}):=\frac{n!}{n_{1}!\times n_{2}!\times \dots \times n_{r}!}
$$
linear [[Arrangements old|arrangements]] of the given $n$ objects (objects of the same type are indistinguishable)
## Examples
The number of linear arrangements of the four letters in the word ball is $\hspace{0pt}12$, not $4!=24$ which we'd expect from the [[Permutations|permutations]], this is because we don't have $\hspace{0pt}4$ distinct letters to arrange. If the two L's are distinguished as $L_{1}$ and $L_{2}$, then we find that for each arrangement in the L's are indistinguishable there corresponds a pair of permutations with distinct L's. Consequenty,
$$
2\times \text{Number of arrangements of the letter B,A,L,L}=\text{Number of permutations of the symbols B,A,L}_{1}\text{,L}_{2}
$$
and the answer to the original problem of finding all arrangements of the four letters in BALL is $\frac{4!}{2}$
Using this idea, we now consider the arrangements of all six letter in PEPPER
There are $3!$ arrangements with the P's distinguished for each earrangement in which the P's are distinguished for each arrangement in which the P's are not distinguished, for example,
$$
\{P_{1},E,P_{2},P_{3},E,R\},\{ P_{1},E,P_{3},P_{2},E,R \},\{ P_{2},E,P_{1},P_{3},E,R \},\{ P_{2},E,P_{3},P_{1},E,R \},\{ P_{3},E,P_{1},P_{2},E,R \},
$$
$$
 \{ P_{3},E,P_{2},P_{1},E,R \}
$$
all correspond to PEPPER when we remove the subscripts on the P's. In addition, to the arrangement there corresponds a pair of permutations when the E's are distinguished. The reason it will always be factorial is because you are permuting the letters with subscripts, so there are $n!$ ways of doing so. Consequently, the number of arrangements of the six letters in PEPPER is $\frac{6!}{2!3!}=60$ 
## Staircase Paths
Determine the number of staircase paths in the $xy$ plane from $(x_{1},y_{1})$ to $(x_{2},y_{2})$, where $x_{2}>x_{1},y_{2}>y_{1}$ where each such path is made up of indivitdual steps going one urit to the right (R) or one unit upward (U), an example pictured below:
![[Staircase Paths 2024-10-18 11.57.59.excalidraw]]
The path must be made up of $r=x_{2}-x_{1}$ R moves and $u=y_{2}-y_{1}$ U moves. Consequently, each path corresponds with $r$ R moves and $u$ U moves and the solution is the number of arrangements of these, which we can work out, which is:
$$
\frac{(u+r)!}{u!r!}
$$
This theory can then be expanded to more dimensions

#Mathematics #Discrete 