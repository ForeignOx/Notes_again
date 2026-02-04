The scalar triple product is a function in [[Vectorspace Rn|$\mathbb{R}^3$]]:
$$
\mathbb{R}^3\times \mathbb{R}^3\times \mathbb{R}^3\to \mathbb{R}
$$
$$
 (\underline{a},\underline{b},\underline{c})\mapsto[\underline{a},\underline{b},\underline{c}]
$$
Where:
$$
[\underline{a},\underline{b},\underline{c}]:=\underline{a}\cdot(\underline{b}\times \underline{c})
$$
So if:
$$
\underline{a}=\begin{pmatrix}
a_{1}\\a_{2}\\a_{3}
\end{pmatrix},\underline{b}=\begin{pmatrix}
b_{1}\\b_{2}\\b_{3}
\end{pmatrix},\underline{c}=\begin{pmatrix}
c_{1}\\c_{2}\\c_{3}
\end{pmatrix}\in \mathbb{R}^3,l_{1},l_{2},l_{3}\in \mathbb{R}
$$
Then the [[Systems of Linear Equations|system of equations]]:
$$
a_{1}x+a_{2}y+a_{3}z=l_{1}
$$
$$
 b_{1}x+b_{2}y+b_{3}z=l_{2}
$$
$$
 c_{1}x+c_{2}y+c_{3}z=l_{3}
$$
Has a unique solution iff $[\underline{a},\underline{b},\underline{c}]\neq 0$
## Note
$$
[\underline{a},\underline{b},\underline{c}]=\det(\underline{a}\,\underline{b}\,\underline{c})
$$
where $(\underline{a}\,\underline{b}\,\underline{c})$ is a $3\times 3$ [[Matrices|matrix]]
## Invariance Under Cyclic Permutation
If $\underline{a},\underline{b},\underline{c}\in\mathbb{R}^3$ then:
$$
[\underline{a},\underline{b},\underline{c}]=[\underline{b},\underline{c},\underline{a}]=[\underline{c},\underline{a},\underline{b}]
$$
$$
 =-[\underline{b},\underline{a},\underline{c}]=-[\underline{a},\underline{c},\underline{b}]=-[\underline{c},\underline{b},\underline{a}]
$$
### Proof
$$
[\underline{a},\underline{b},\underline{c}]=\underline{a}\cdot \left( \begin{pmatrix}
b_{1}\\ b_{2}\\b_{3}
\end{pmatrix}\times \begin{pmatrix}
c_{1}\\c_{2}\\c_{3}
\end{pmatrix} \right)=\begin{pmatrix}
a_{1}\\a_{2}\\a_{3}
\end{pmatrix}\cdot \begin{pmatrix}
b_{2}c_{3}-b_{3}c_{2}\\b_{3}c_{1}-b_{1}c_{3}\\b_{1}c_{2}-b_{2}c_{1}
\end{pmatrix}
$$
$$
= a_{1}b_{2}c_{3}+a_{2}b_{3}c_{1}+a_{3}b_{1}c_{2}-a_{1}b_{3}c_{2}-a_{2}b_{1}c_{3}-a_{3}b_{2}c_{1}
$$
We can see that the subscripts are in fact undergoing cyclic permutation, so we can see that there will be invariance if you interchange the $a$'s, $b$'s and $c$'s cyclically, then if you change the order, then we are using the second half of the equation and the negative signs switch


#Mathematics #LinAlg #Definition