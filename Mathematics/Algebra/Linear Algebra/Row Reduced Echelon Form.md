A [[Matrices|matrix]] is said to be in row reduced echelon form (RREF) iff the folowing hold:
- The first (leftmost) non-zero entry is a $\hspace{0pt}1$, and is called the "leading $\hspace{0pt}1$" 
- If a row has a leading one in the $j$th column:
    - All other entries in the $j$th column are $\hspace{0pt}0$ 
    - Leading $\hspace{0pt}1$'s of subsequent rows are to the right of the $j$th column
- Any rows of all $\hspace{0pt}0$'s occur after all non-zero rows
## Examples
### $2\times 2$ matrices:
$$
\begin{pmatrix}
1&0\\0&1
\end{pmatrix},\begin{pmatrix}
1&a\\0&0
\end{pmatrix},\begin{pmatrix}
0&1\\0&0
\end{pmatrix},\begin{pmatrix}
0&0\\0&0
\end{pmatrix}
$$
Consider the system with unknowns and $\hspace{0pt}2$ equations:
$$
\left(
\begin{array}{cc|c}
1&0&b_{1}\\0&1&b_{2}
\end{array}
\right)
$$
Which can be read off $x_{1}+0x_{2}=b_{1}$ and $0x_{1}+x_{2}=b_{2}$, so the solution [[Sets|set]] is:
$$
\left\{  \begin{pmatrix}
b_{1}\\b_{2}
\end{pmatrix}  \right\}
$$
Or:
$$
\left(
\begin{array}{cc|c}
1&a&b_{1}\\0&0&b_{2}
\end{array}
\right)
$$
Second equation states $0x_{1}+0x_{2}=b_{2}$, so solution set [[Empty Set|empty]] unless $b_{2}=0$, in which case $x_{1}=b_{1}-ax_{2}$, so the solution set is:
$$
\left\{  \begin{pmatrix}
b_{1}-ax_{2}\\x_{2}
\end{pmatrix}\middle| x_{2}\in \mathbb{R}  \right\}
$$
Or:
$$
\left(
\begin{array}{cc|c}
0&1&b_{1}\\0&0&b_{2}
\end{array}
\right)
$$
Second equation states $0x_{1}+0x_{2}=b_{2}$, so solution set empty unless $b_{2}=0$, in which case $x_{2}=b_{1}$, so solution set is:
$$
\left\{  \begin{pmatrix}
x_{1}\\b_{1}
\end{pmatrix}\middle| x_{1}\in \mathbb{R}  \right\}
$$
___

![[Row Reduced Echelon Form 2024-10-29 11.29.35.excalidraw]]
Is in RREF
So what is the solution set?, here we see the system is:
$$
x_{2}+3x_{4}+329x_{6}+12x_{7}=-3
$$
$$
 x_{3}+2x_{4}+4x_{6}-7x_{7}=-3
$$
$$
 x_{5}-x_{6}+5x_{7}=-3
$$
$$
 x_{8}=-3
$$
The variables corresponding to non-leading $\hspace{0pt}1$ positions are "free variables", so $x_{4},x_{6},x_{7}$ are free variables in this case:
$$
x_{2}=-3-3x_{4}-329x_{6}-12x_{7}
$$
$$
 x_{3}=-3-2x_{4}-4x_{6}+7x_{7}
$$
$$
 x_{5}=-3+x_{6}+5x_{7}
$$
$$
 x_{8}=-3
$$
and so the solution set is:
$$
\left\{  \begin{pmatrix}
0\\-3-3x_{4}-329x_{6}-12x_{7}\\-3-2x_{4}-4x_{6}+7x_{7}\\x_{4}\\-3+x_{6}+5x_{7}\\x_{6}\\x_{7}\\-3
\end{pmatrix}  \right\}=\left\{  \begin{pmatrix}
0\\-3\\-3\\0\\-3\\0\\0\\-3
\end{pmatrix}+\lambda_{1}\begin{pmatrix}
0\\-3\\-2\\1\\0\\0\\0\\0
\end{pmatrix}+\lambda_{2}\begin{pmatrix}
0\\-329\\-4\\0\\1\\1\\0\\0
\end{pmatrix}+\lambda_{3}\begin{pmatrix}
0\\-12\\7\\0\\5\\0\\1\\0
\end{pmatrix}\mid\lambda_{1},\lambda_{2},\lambda_{3}\in \mathbb{R}  \right\}
$$


#Mathematics #LinAlg #Definition 