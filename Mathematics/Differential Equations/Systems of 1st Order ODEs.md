## Systems of 1st Order Linear ODEs
A system of $n$ coupled [[First Order Ordinary Differential Equations|1st order linear ODEs]] for $n$ dependent variables can be re-written as a single $n$th order linear ODE for a single dependent variable by eliminating the other dependent variables
An associated IVP is obtained if all the values of the dependent variables are specified at a single value of the independent variable
Note this process can be used to convert an $n$th order ODE as a set of $n$ first order linear ODEs, which can be solved with linear algebra :)
### Example
Find the solution $y(x),z(x)$ of the pair of 1st order linear ODEs
$$
y'=y-2z+2x
$$
$$
 z'=3y-4z+2x
$$
Satisfying the initial conditions $y(0)=1,z(0)=2$
We rewrite the system of two coupled first order ODEs as a [[Second Order Ordinary Differential Equations|second order ODE]] for $y$ or $z$, which we can solve
From the first equation;
$$
z=-\frac{y'}{2}+\frac{y}{2}+x
$$
$$
\implies z'=-\frac{y''}{2}+\frac{y'}{2}+1
$$
Then we can substitute these expressions for $z$ and $z'$ into the second equation:
$$
-\frac{y''}{2}+\frac{y'}{2}+1=3y-4\left( -\frac{y'}{2}+\frac{y}{2}+x \right)+2x
$$
Which can be rearranged to:
$$
y''+3y'+2y=4x+2
$$
Which has characteristic equation
$$
\lambda^{2}+3\lambda+2=(\lambda+1)(\lambda+2)=0
$$
So 
$$
y_{CF}=Ae^{ -x }+Be^{ -2x }
$$
Try
$$
y_{PI}=a_{1}x+a_{0}
$$
$$
y'_{PI}=a_{1}
$$
$$
y''_{PI}=0
$$
Which substituting gives:
$$
3a_{1}+2a_{1}x+2a_{0}=4x+2
$$
By comparing coeffcients gives:
$$
a_{1}=2,a_{0}=-2
$$
So 
$$
y_{PI}=2x-2
$$
And hence the general solution for $y$ is:
$$
y=Ae^{ -x }+Be^{ -2x }+2x-2
$$
And using the first of the system of equations:
$$
z=-\frac{1}{2}y'+\frac{1}{2}y+x=\frac{A}{2}e^{ -x }+Be^{ 2x }-1+\frac{A}{2}e^{ -x }+\frac{B}{2}e^{ -2x }+x-1+x
$$
$$
=Ae^{ -x }+\frac{3B}{2}e^{ -2x }+2x-2
$$
We now apply the initial conditions:
$$
y(0)=A+B-2=1\implies A+B=3
$$
$$
z(0)=A+\frac{3}{2}B-2=2\implies A+\frac{3}{2}B=4
$$
Which can be solved and have solution $B=2,A=1$, so the solution is:
$$
y(x)=e^{ -x }+2(e^{ -2x }+x-1)
$$
$$
z(x)=e^{ -x }+3e^{ -2x }+2(x-1)
$$

#Mathematics #Calculus 