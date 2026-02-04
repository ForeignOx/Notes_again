The fundamental object that alloows us to think of charges a generating transformations is the poisson bracket
## Definition
Given $f(\underline{q},\underline{p})$ and $g(\underline{q},\underline{p})$, we define the Poisson bracket $\left\{ f,g \right\}$ (another funciton in the [[Phase Spaces|phase space]]) as:
$$
\left\{ f,g \right\}=\sum_{i=1}^{N}\left( \frac{ \partial f }{ \partial q_{i} } \frac{ \partial g }{ \partial p_{i} } -\frac{ \partial f }{ \partial p_{i} } \frac{ \partial g }{ \partial q_{i} }  \right)
$$
And in this definition, we treat $q_{i},p_{j}$ as independent:
$$
\frac{ \partial q_{i} }{ \partial q_{j} } =\frac{ \partial p_{i} }{ \partial p_{j} } =\delta_{ij}
$$
$$
\frac{ \partial q_{i} }{ \partial p_{j} } =\frac{ \partial p_{i} }{ \partial q_{j} } =0
$$
## Fundamental Examples
Some examples of fundamental Poisson brackets are:
$$
\left\{ q_{i},q_{j} \right\}=\sum_{k=1}^{N}\left( \frac{ \partial q_{i} }{ \partial q_{k} } \cancel{ \frac{ \partial q_{j} }{ \partial p_{k} } } -\cancel{ \frac{ \partial q_{i} }{ \partial p_{k} } } \frac{ \partial q_{j} }{ \partial q_{k} }  \right)=0
$$
Similarly
$$
\left\{ p_{i},p_{j} \right\}=0
$$
A more interesting example:
$$
\left\{ q_{i},p_{j} \right\}=\sum_{k=1}^{N}\left( \frac{ \partial q_{i} }{ \partial q_{k} } \frac{ \partial p_{j} }{ \partial p_{k} } -\cancel{ \frac{ \partial q_{i} }{ \partial p_{k} } \frac{ \partial p_{j} }{ \partial q_{k} }  } \right)=\delta_{i,j}
$$
## Properties
- The Poisson bracket is antisymmetric:
$$
\left\{ f,g \right\}=-\left\{ g,f \right\}
$$
- The poisson bracket is [[Linear|linear]]:
$$
\left\{ \alpha f+\beta g,h \right\}=\alpha \left\{ f,h \right\}+\beta \left\{ g,h \right\}
$$
    Together with asymmetry, this implies that
$$
\left\{ h,\alpha f+\beta g \right\}=\alpha \left\{ h,f \right\}+\beta \left\{ h,g \right\}
$$
    So the poisson bracket is a [[Bilinear Form|bilinear form]]
- The poisson bracket obeys the Leibniz identity:
$$
\left\{ fg,h \right\}=f\left\{ g,h \right\}+g\left\{ f,h \right\}
$$
- The poisson bracket obeys the Jacobi identity for the sum of the cyclic permutations
