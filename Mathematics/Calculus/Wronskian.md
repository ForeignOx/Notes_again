Given two [[Differentiation|differentiable]] [[Functions|functions]], $y_{1}$ and $y_{2}$, a Wronskian is defined in the following way:
$$
W(y_{1},y_{2})=\det \begin{pmatrix}
y_{1}&y_{2}\\y_{1}'&y_{2}'
\end{pmatrix}=y_{1}y_{2}'-y_{2}y_{1}'
$$
If $y_{1}$ and $y_{2}$ are linearly dependent, $y_{1}(x)=\lambda y_{2}(x)$ for all $x$. Then $y_{1}'(x)=\lambda y_{2}'(x)$ and $W(y_{1},y_{2})=\lambda y_{2}y_{2}'-\lambda y_{2}'y_{2}=0$, so $W(y_{1},\lambda y_{1})=0\forall x$
Therefore, if $W(y_{1},y_{2})$ is not identically zero, $y_{1}$ and $y_{2}$ are [[Linear Independence|linearly independent]]

#Mathematics #Calculus #Definition 