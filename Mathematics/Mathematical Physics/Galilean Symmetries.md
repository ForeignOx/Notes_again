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
\frac{ \partial^{2}\psi(t,x) }{ \partial t^{2} } -c^{2}
$$