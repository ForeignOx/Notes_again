Physical laws should not depend on our choice of inertial frame. In other words, if a law is valid for one freely moving observer, it should be valid for all freely moving observers. The transformations relating inertial frames are precisely those that leave the fundamental laws invariany
If we consider [[Newton's Second Law of Motion|Newton's second law]], $m\underline{\ddot{x}}=\underline{F}$ holds in all inertial frames, but we want to connect inertial frames to each other, this leads to the following transformations:
## Translations
A rigid translation is a constant shift of the spatial origin,
$$
\underline{y}(t)=\underline{x}(t)+\underline{c}
$$
So that $\underline{x}(t)=\underline{y}(t)-\underline{c}$, and hence $\underline{\ddot{x}}-\underline{\ddot{y}}$, thus Newton's law retains its form in the translated frame, provided the force is unchanged, $\underline{F}'=\underline{F}$ 
## Euclidean Rotation
A rigid rotation is given by
$$
\underline{y}(t)=R\underline{x}(t)
$$
 with [[Special Orthogonal Group|$R\in SO(3)$]] is a constant rotation matrix, and where $R^{\top} R=I_{3}$
 Differentiating twice gives $\ddot{\underline{y}}=R\ddot{\underline{x}}$ so Newton's llaw holds in the rotated frame as
 $$
 m\underline{\ddot{y}}(t)=\underline{F}',\underline{F}'=R\underline{F}
$$
## Galilean Boost
Two inertial observers moving with constant relative velocity $\underline{v}$ are related by
$$
\underline{y}(t)=\underline{x}(t)-\underline{v} t
$$
Taking two time derivatives again gives $\underline{\ddot{y}}=\underline{\ddot{x}}$, so Newton's law is invariant (with $\underline{F}'=\underline{F}$)
## Remark
Notice that in all these cases, time is just a parameter, Newtonian physics never touches it
## Application to Maxwell's Laws
Since Maxwell came up with his laws, we want to check whether they are compatable with Newton's so they would have to respect the same symmetries otherwise our theories are incompatible
We think of this by considering how waves obeying Maxwell's laws behave under Galilean boosts:
### Mechanical Waves in 1D
Imagine we live in one spatial dimension $x$, a very specific observes studies $\psi$ which satisfies the [[Wave Equation|wave equation]],
$$
\frac{ \partial^{2}\psi(t,x) }{ \partial t^{2} } -c^{2}\frac{ \partial^{2}\psi(t,x) }{ \partial x^{2} } =0
$$
So we have waves propagating with speed $c$. We know that these have general solution
$$
\psi(x,t)=f(x-ct)+g(x+ct)
$$
Since we can't physically boost the wave itself, we apply the boost by moving the ovserver.
Let's assume Galilean boosts are fundamental for all moving observers, what does a moving oberver see?
$$
x=x'+vt
$$
And $t$ stays the same
$\psi$ transforms as a scalar function; i.e.
$$
\psi'(x',t)=\psi(x(x',t'),t(x',t')) =\psi(x-vt,t)
$$
$$
\implies \psi'(x',t')=f(x'+vt-ct)+g(x'+vt+ct)
$$
$$
 =f(x'-(c-v)t)+g(x'+(c+v)t)
$$
$$
=f(x'-v_{R}t)+g(x'+v_{L}t)
$$
So the right moving waves have velocity $v_{R}=c-v$ and the left moving waves have velocity $v_{L}=c+t$
So the for the moving observer the physical law changes,
$$
x'=x-vt,t'=t
$$
$$
 \frac{ \partial  }{ \partial x } =\frac{ \partial x' }{ \partial x } \frac{ \partial  }{ \partial x' } +\frac{ \partial t' }{ \partial x } \frac{ \partial  }{ \partial t' } =\frac{ \partial  }{ \partial x' } 
$$
$$
\frac{ \partial  }{ \partial t } =\frac{ \partial t' }{ \partial t } \frac{ \partial  }{ \partial t } +\frac{ \partial x' }{ \partial t } \frac{ \partial  }{ \partial x' } =\frac{ \partial  }{ \partial t' } -v\frac{ \partial  }{ \partial 'x' } 
$$
Which is kinda strange
So our "wave equation" becomes:
$$
\frac{ \partial^{2}\psi' }{ \partial t'^{2} } -2v \frac{ \partial^{2}\psi' }{ \partial x'\partial t' } -(c^{2}-v^{2})\frac{ \partial^{2}\psi' }{ \partial x'^{2} } =0
$$
Which is different
Essentially this tells us that the movement of a wave has a preferred reference frame
### Mechanical Waves in 2D
We know electromagnetic waves propagate with the speed of light
Michelon and Morley showed in $\hspace{0pt}1887$ that all inertial observers see light propagating with the same speed
This tells us that Maxwell's equation are universal for all inertial frames
Note that the electromagnetic field is frame dependent but the electromagnetic field still satisfy Maxwell's equations
What the above example showed is that with Galilean boosts, Maxwell's equations aren't satisfied which is very sad
