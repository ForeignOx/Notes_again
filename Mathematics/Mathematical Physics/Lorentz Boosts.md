## In $1+1$D
We know electromagnetic waves propagate with the speed of light
Michelon and Morley showed in $\hspace{0pt}1887$ that all inertial observers see light propagating with the same speed
This tells us that Maxwell's equation are universal for all inertial frames
Note that the electromagnetic field is frame dependent but the electromagnetic field still satisfy Maxwell's equations
We can show that with [[Galilean Symmetries|Galilean boosts]], Maxwell's equations aren't satisfied which is very sad, so we have to throw away Newton's law
To find a replacement, we want to find a more general transformation:
$$
x'=Ax+Bt
$$
$$
 t'=Et+Dx
$$
Which gives su the derivatives:
$$
\frac{ \partial  }{ \partial t } =\frac{ \partial x' }{ \partial t } \frac{ \partial  }{ \partial x' } +\frac{ \partial t' }{ \partial t } \frac{ \partial  }{ \partial t' } =B\frac{ \partial  }{ \partial x'+E\frac{ \partial  }{ \partial t' }  } 
$$
$$
\frac{ \partial  }{ \partial x } =\frac{ \partial x' }{ \partial x } \frac{ \partial  }{ \partial x' } +\frac{ \partial t' }{ \partial x } \frac{ \partial  }{ \partial t' } =A\frac{ \partial  }{ \partial x' } +D\frac{ \partial  }{ \partial t' } 
$$
And we demand the wave equation preserves its form with the same speed of light:
doing some mathsy maths, we get that the simplest case is the Lorentz boost in 1+1D:
$$
x'=\gamma(x-vt),t'=\gamma\left( t-\frac{v}{c^{2}}x \right)
$$
Where $\gamma= \frac{1}{\sqrt{ 1-\frac{v^{2}}{c^{2}} }}$
### Remarks
This means that there is no sense of global time, $\gamma$ has to be real, and two observes cannot move with relative speed $v>c$
In the limit $\frac{v}{c}\to 0$, we see that
$$
\gamma=\frac{1}{\sqrt{ 1-\frac{v^{2}}{c^{2}} }}\to 1,x'\to x-vt,t'=t
$$
So Galilean boosts are the limit of Lorentz boosts
We also see that one of the key properties, the [[Euclidean Space|Euclidean distance]] is not preserved
The invariant distance is the spacetime distance
# In $3+1$D
The general $\Lambda$!!
The most important thing is that they satisfy:
$$
\Lambda ^{\top}\eta\Lambda=\eta
$$
So it's an equation that is symmetric in its indices i.e.
$$
(\Lambda ^{\top}\eta\Lambda)^{\top}=\eta ^{\top} 
$$
$$
\implies \Lambda ^{\top}\eta(\Lambda ^{\top})^{\top}=\eta ^{\top} 
$$
$$
\implies \Lambda ^{\top}\eta\Lambda=\eta
$$
So if we think of our $4\times 4$ matrix:
$$
\begin{pmatrix}
a_{11} & a_{12} & a_{13} & a_{14} \\
 & a_{22} & a_{23} & a_{24} \\
 &  & a_{33} & a_{34} \\
 &  &  & a_{44}
\end{pmatrix}
$$
Because the lower diagonal must satisfy the symmetry, so we only get $10$ independent equations (rather than 16), so we are left with $\hspace{0pt}6$ free parameters
## Lorentz Boosts in $x$-Direction
We recall
$$
x'=\gamma(x-v_{x}t)
$$
$$
 t'=\gamma\left( t-\frac{v_{x}}{c}x \right)
$$
$$
y'=y
$$
$$
 z'=z
$$
Which we can write in our new notation:
$$
(x^{0})'=\gamma\left( x^{0}- \frac{v_{x^{1}}}{c}x^{1} \right)
$$
$$
 (x^{1})'=\gamma\left( x^{1}-\frac{v_{x^{1}}}{c}x^{0} \right)
$$
$$
(x^{2})'=x^{2} 
$$
$$
 (x^{3})'=x^{3}
$$
So we can write this as a matrix:
$$
\Lambda_{x}(v_{x})=\begin{pmatrix}
\gamma & -\frac{v_{x}}{c}\gamma & 0 & 0 \\
-\frac{v_{x}}{c}\gamma & \gamma & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1
\end{pmatrix}

$$
We can show that this transforms how we'd like:
$$
\eta \Lambda_{x}=\begin{pmatrix}
-1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1
\end{pmatrix}\begin{pmatrix}
\gamma & -\frac{v_{x}}{c}\gamma & 0 & 0 \\
-v_{x}
\end{pmatrix}
$$
## Lorentz Boosts in the $y$-direction
This is derived similarly:
$$
\Lambda_{y}(v_{y})=\begin{pmatrix}
meow
\end
{pmatrix}
$$
and in $z$-direction
## Lorentz Boosts in Higher Dimension
We also have
$$
\Lambda _{R}=\begin{pmatrix}
1 & 0 & 0 & 0 \\
0 \\
0  &  & R\\  
0 
\end{pmatrix}
$$
Where $R$ is a $3\times 3$ rotation
$R$ is parametrised by $\hspace{0pt}3$ angles
So the most general Lorentz transformation is a combination of the above:
$$
\Lambda= \Lambda_{x}(v_{x})\Lambda_{y}(v_{y})\Lambda_{z}(v_{z})\Lambda_{R}
$$
This class is continuously connected to the identity
$$
\Lambda=I
$$
However the equation
$$
\Lambda^{\mu}_{~ ~\rho}\eta_{\mu \nu}\Lambda^{\nu}_{~ ~\sigma}=\eta_{\rho\sigma} 
$$
$$
\implies 
\Lambda ^{\top}\eta\Lambda=\eta
$$
Which admits solutions outside the family of $\Lambda$ 
Taking the determinant of our equation we see this:
$$
\det(\Lambda ^{\top}\eta\Lambda)=\det \eta 
$$
$$
 \implies \det(\Lambda ^{\top})\det(\eta)\det(\Lambda)=\det(\eta)
$$
$$
\implies  \det(\Lambda)^{2}=1 
$$
$$
\implies \det\Lambda=\pm 1
$$
Some solutions have $\det\Lambda=-1$, but these cannot be continuously connected to the identity as the identity has determinant 1
For example time reversal:
$$
\Lambda_{T}=\mathrm{diag}(-1,1,1,1)
$$
Or spatial reflection:
$$
\Lambda_{p}=\mathrm{diag}(1,-1,1,1)
$$
So the matrices with $\det\Lambda=1$ form the proper Lorentz group $SO(1,3)$