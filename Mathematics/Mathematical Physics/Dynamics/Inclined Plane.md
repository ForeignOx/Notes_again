A [[Mass|mass]] $m$ is placed on a plane inclined at an angle $\alpha$ to the horizontal. We have gravity acting downwards with a magnitude $mg$. There is a frictional [[Newton's Second Law of Motion|force]] of [[Magnitude of a Vector|magnitude]] $\mu \left| \underline{N} \right|=\mu N$, where $\mu$ is a positive constant, and $\underline{N}$ is the normal force exerted by the plane on the mass. If $\alpha=0$, then $\left| \underline{N} \right|=mg$
Starting from rest, how far does it move in time $t$?
![[Inclined Plane 2025-01-31 16.23.59.excalidraw]]
We can choose where our [[Standard Basis Vectors|basis vectors]] point, and we can choose $\underline{e}_{1}$ to point down the slope. Then the required answer is $x(t)$, and $y=z=0\forall t$. We can then choose $\underline{e}_{2}$ as perpendicular to the plane, so $\underline{N}=N\underline{e}_{2}$ and the frictional force is $-\mu N\underline{e}_{1}$. There is nothing in $z$ direction or $\underline{e}_{3}$. Staing on slope means no net force in $y$-direction, thus
$$
\underline{N}=mg\cos(\alpha )\underline{e}_{2}
$$

In $x$-direction, we get the equation of motion
$$
m\ddot{x}=-\mu N+mg\sin(\alpha)=-\mu mg\cos\alpha+mg\sin\alpha
$$
So the solution is
$$
x(t)=\frac{1}{2}(g\sin\alpha-\mu g\cos\alpha)t^{2}
$$
Note that if $\mu g\cos\alpha>g\sin\alpha$, then it would be negative which is not the behaviour we want and corresponds to the friction being capped at $g\sin\alpha$, i.e. the solution is valid for $\tan\alpha>\mu$, if $\tan\alpha \leq \mu$, then there is too much friction and the particle doesn't move; $x(t)=0\forall t$

#Mathematics #Dynamics