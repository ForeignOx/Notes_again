Vectors are points in $n$-space, where the coordinates of the point are given by the elements of the vector
Vectors can be the point, or they can be thought of as the directions to a point, or they can be thought of as simply the direction in general
Vectors can have be $n$ dimensional and are represented as an ordered system of $n$ numbers $a_{i},(i=1,2,\dots,n)$ such as:
$$
\underline{a}=\begin{pmatrix}
a_{1}\\a_{2}\\\vdots\\a_{i}\\\vdots\\a_{n}
\end{pmatrix}
$$
The number $a_{i}$ is called the $i$th component
Two vectors:
$$
\underline{a}=\begin{pmatrix}
a_{1}\\a_{2}\\\vdots\\a_{n}
\end{pmatrix},\underline{b}=\begin{pmatrix}
b_{1}\\b_{2}\\\vdots\\b_{n'}
\end{pmatrix}
$$
Are equal if and only if the dimensions $n$ and $n'$ are equal and, furthermore, the corresponding components $a_{i}$ and $b_{i}$ are equal for all $1\leq i\leq n$, thus we can say $\underline{a}=\underline{b}$
When two vectors $\underline{a}$ and $\underline{b}$ are given, the equation
$$
\underline{x}+\underline{a}=\underline{b}
$$
is satisfied by exactly one vector $\underline{x}$ given by $\underline{b}+(-\underline{a})=\underline{b}-\underline{a}$, hence $x_{i}=b_{i}-a_{i}$
For a given scalar $\lambda \neq 0$ and a vector $\underline{a}$, the equation
$$
\lambda \underline{x}=\underline{a}
$$
is satisfied by the unique vector given by $\left( \frac{1}{\lambda} \right)\underline{a}$, so $x_{i}=\frac{a_{i}}{\lambda}$
## Vectors as [[Functions|Functions]]
Since vectors have an order imposed by some [[Sets of Indices|set of indices]], and are often displayed as some $n$-tuple, we can think of a vector $\underline{a}$ as a function with domain $I$ the index set, where $a_{i}$ is the value of the function $\underline{a}$ at $I$, this [[Vectorspaces|vectorspace]] suggets a general type called a functrtion space
## Vector Addition
![[Vectors 2024-10-13 21.43.04.excalidraw]]

## Scalar multiplication
![[Vectors 2024-10-13 21.44.11.excalidraw]]
## Ket Notation
A vector in a [[Hilbert Spaces|Hilbert space]] is written as a ket $\ket{\cdot}$, and the $\cdot$ can be represented by any letter as the name of the vector, e.g. $\ket{\psi}$
### Basis Expansion
Take a basis of $\mathcal{H}$ $\ket{i}$ for $i\in\left\{ 1,\dots,n \right\}$, then we can write any state $\ket{v}\in\mathcal{H}$ uniquely as
$$
\ket{v} =\sum_{i=1}^{n}v_{i}\ket{i} 
$$
For some $v_{i}\in \mathbb{C}$ which are the components of $\ket{v}$ in basis $\ket{i}$ (you can think of them as coordinates)
### Proposition
The basis is orthonormal if
$$
\braket{ i | j } =\delta_{ij}
$$
### Proof
$$
\braket{ j | v } =\braket{ j | \sum_{ i=1} ^{ n} v_{i}\ket{i}   } 
$$
$$
= \sum_{ i=1} ^{ n}  v_{i}\ket{}  
$$


#Mathematics #LinAlg 