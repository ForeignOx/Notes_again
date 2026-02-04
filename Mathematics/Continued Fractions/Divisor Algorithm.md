Split our number $x$ into its integer part ($a_{0}$) and the remainder, which if non-zero as $\frac{1}{y_{1}}$, repeat with $y_{1}$ to obtain $y_{2}$:
$$
x=a_{0}+\frac{1}{y_{1}}
$$
$$
y_{1}=a_{1}+\frac{1}{y_{2}}
$$
$$
y_{2}=a_{2}+\frac{1}{y_{3}}
$$
$$
\vdots
$$
$$
y_{n-1}=a_{n-1}+\frac{1}{y_{n}}
$$
This process terminates when we have a unit fraction as the remainder, i.e. $y_{n}\in\mathbb{Z}$

#Mathematics #Fractions #Algorithm