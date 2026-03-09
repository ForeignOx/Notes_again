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