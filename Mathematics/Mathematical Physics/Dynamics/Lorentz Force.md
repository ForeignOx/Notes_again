A particle of quarge $q$ experiences the Lorentz force relating [[Electric Field Strength|electric field strength]], [[Velocity|velocity]] and [[Magnetic Flux Density|magnetic flux density]]:
$$
\underline{F}=q\underline{E}+q\underline{v}\times \underline{B}
$$
## Example
Take $\underline{E}=\vec{0},\underline{B}=B\underline{e}_{3}$ (using [[Standard Basis Vectors|standard basis vectors]]) With initial conditions $r(0)=\vec{0}$ and $\underline{\dot{r}}=u\underline{e}_{1}$. Find $\underline{r}(t)$
First we find [[Newton's Second Law of Motion|equation of motion]]:
$$
m \underline{\ddot{r}}=\underline{F}=q \underline{\dot{r}}\times \underline{B}=qB \underline{\dot{r}}\times \underline{e}_{3}
$$
We can simplify both sides by [[Integration|integrating]] with respect to time:
$$
m \dot{r}=qB  \underline{r}\times \underline{e}_{3}+mu\underline{e}_{1}
$$
Where $m u\underline{e}_{1}$ is the constant of integration. Now we have to write out the components:
$$
\underline{r}=x\underline{e}_{1}+y\underline{e}_{2}+z\underline{e}_{3}
$$
Then we get three components of the [[Vectors|vector]], so $\hspace{0pt}3$ simultaneous equations
$$
m\begin{pmatrix}
\dot{x}\\\dot{y}\\\dot{z}
\end{pmatrix}=m\begin{pmatrix}
u\\0\\0
\end{pmatrix}+qB \begin{pmatrix}
y\\-x\\0
\end{pmatrix}
$$
So we get 
$$
m \dot{x}=m u +qBy
$$$$
m\dot{y}=-qBx
$$
$$
 m\dot{z}=0
$$
Since $z$ starts at a constant and is constant, we say $z(t)=0\forall f$
So we are left with two [[Systems of 1st Order ODEs|coupled equations]] for $x$ and $y$. The general strategy is to eliminate $x$ or $y$, we'll eliminate $y$. [[Differentiation|differentiating]] the first equation:
$$
m\ddot{x}=qB\dot{y}=-\frac{qB}{m}xqB
$$
$$
\implies \ddot{x}+\left( \frac{qB}{m} \right)^{2}x=0
$$
Then this is [[Simple Harmonic Motion|simple harmonic motion]], ahas genral sulution:
$$
x(t)=\alpha\cos(\omega t)+\beta \sin(~\omega t)
$$
With $\alpha,\beta$ constants, and $\omega=\frac{qB}{m}$, we also have that 
$$
x(0)=0\implies\alpha=0
$$
$$
\implies x(t)=\beta \sin(\omega t)
$$ 
And, 
$$
\dot{x}(0)=u\implies \beta\omega=u\implies x\left( t \right)=\frac{u}{\omega}\sin(\omega t)
$$
Finally, substituting into the first equation
$$
y=\frac{m}{qB}(\dot{x}-u)=\frac{mu}{qB}(\dot{x}-u)-\frac{m u}{qB}(1-\cos(\omega t))=\frac{u}{\omega}(1-\cos(\omega t))
$$
This ends up being quite circular motion. If you consider $x^{2}+\left( y-\frac{u}{\omega} \right)^{2}=\frac{u^{2}}{\omega^{2}}$ 
___
As with before, with $m=q=1$, and electric field $\underline{E}=E\underline{e}_{2}$ 
Again we find the equatio of motion:
$$
\underline{\ddot{r}}=B \underline{\dot{r}}\times u\underline{e}_{3}+\underline{E}_{2}
$$
Integrating with respect to time, we get:
$$
\underline{\dot{r}}=B\underline{r}\times \underline{e}_{3}+Et \underline{e}_{2}+u\underline{e}_{1}
$$
So $z(t)=0$ for all $t$. Now we eliminate $y$:
$$
\ddot{xq}=B\dot{q}=-B
$$

#Mathematics #Dynamics #Equation 