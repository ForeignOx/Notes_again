Circles are a set of points equidistance from a central point, they are useful in many situations

## Equation of Circles in $\mathbb{C}$
The equation of a general circle in the [[Complex Numbers|complex]] plane is given by
$$
\left| z-a \right| =r
$$
Where $r>0$ is the radius, and $a\in\mathbb{C}$ is the centre
___
Given $\gamma,\beta \in\mathbb{R}$ and $\alpha \in \mathbb{C}$, the equation
$$
\gamma z \overline{z}-\overline{\alpha}z-\alpha \overline{z}+\beta=0
$$
Describes a circle if $\gamma \neq 0$ and $\left| \alpha \right|^{2}-\beta\gamma>0$, and any circle can be described by an equation of this form
### Proof
The equation of a general circle we know is given by
$$
\left| z-a \right| =r
$$
For some $a\in\mathbb{C}$ and  $r>0$. This can be written equivalently as
$$
(z-a)(\overline{z}-\overline{a})=r^{2} 
$$
$$
 z\overline{z}-a\overline{z}-\overline{a}z+(\left| a \right| ^{2}-r^{2})=0
$$
This fits the general form with $\gamma=a,\alpha=a$ and $\beta=\left| a \right|^{2}-r^{2}$ as
$$
\left| \alpha \right| ^{2}-\beta\gamma=\left| a \right| ^{2}-(\left| a \right| ^{2}-r^{2})=r^{2}>0
$$
Conversely,
$$
\gamma z\overline{z}-\alpha \overline{z}-\overline{\alpha}z+\beta=0
$$
With $\gamma,\beta \in\mathbb{R},\alpha \in\mathbb{C},\gamma \neq 0$ and $\left| \alpha \right|^{2}-\beta\gamma>0$ holds iff
$$
z\overline{z}-\frac{\alpha}{\gamma}\overline{z}-\frac{\overline{\alpha}}{\gamma}z+\frac{\beta}{\gamma}=0
$$
Which can be rewritten as
$$
\left| z-\frac{\alpha}{\gamma} \right| =\sqrt{ \left| \frac{\alpha}{\gamma} \right| ^{2}-\frac{\beta}{\gamma} }=\frac{\sqrt{ \left| \alpha \right| ^{2}-\beta\gamma }}{\left| \gamma \right| }
$$
Giving us a circle centred at $\frac{\alpha}{\gamma}$ with radius $\frac{\sqrt{ \left| \alpha \right|^{2}-\beta\gamma }}{\left| \gamma \right|}$