As a body moves through an oscillatory cycle, its [[Kinetic Energy|kinetic]], [[Gravitational Potential Energy|gravitational potential]] and [[Elastic Potential Energy|elastic potential energies]] are constantly changing. Consider a general example of [[Simple Harmonic Motion]], with $\epsilon=0$
$$
x=A\cos\omega t
$$
$$
v=-\omega A\sin\omega t
$$
The elastic potential energy at $x$ is the area under the $F-x$ graph, which is the same for a spring, i.e. $\frac{1}{2}kx^{2}$. The kinetic energy is $\frac{1}{2}mv^{2}$, combining these with the above equations, we get
$$
E_{p}=\frac{1}{2}kA^{2}\cos ^{2}\omega t
$$
$$
E_{k}=\frac{1}{2}m\omega^{2}A^{2}\cos ^{2}\omega t
$$
But $k=m\omega^{2}$, so
$$
E_{p}=\frac{1}{2}m\omega^{2}A^{2}\cos ^{2}\omega t
$$
So the total vibrational energy is:
$$
E_{p}+E_{k}=\frac{1}{2}m\omega^{2}A^{2}(\cos ^{2}\omega t+\sin ^{2}\omega t)=\frac{1}{2}m\omega^{2} A^{2}
$$
The actual details are a bit more complicated if gravitational energy is involved, for example consider a load of mass $m$ attached to a spring with spring constant $k$, which is clamped vertically. The tension in the spring is initially 0
![[Energy of Oscillation 2024-03-02 15.31.35.excalidraw]]
The equilibrium point is a distance $A$ below the release point, where $mg=kA\implies A=\frac{mg}{k}$, the initial value of $x$ is $A$, so the variation of $x$ with $t$ is:
$$
x(t)=\frac{mg}{k}\cos\omega t
$$
Where $\omega=\sqrt{ \frac{k}{m} }$
So the variation of GPE with time is:
$$
E_{g}(t)=mgx(t)=\frac{m^{2}g^{2}}{k}\cos\omega t
$$
The elastic potential energy is:
$$
E_{e}(t)=\frac{1}{2}k(A-x(t))^{2}=\frac{1}{2}k\left( \frac{mg}{k}-\frac{mg}{k}\cos\omega t \right)^{2}=\frac{m^{2}g^{2}}{2k}(1-\cos\omega t)^{2}
$$
Multiplying out the $(1-\cos\omega t)^{2}$ and adding the GPE gives us the total potential energy to be:
$$
E_{p}(t)=\frac{m^{2}g^{2}}{2k}(2\cos\omega t+1-2\cos\omega t+\cos ^{2}\omega t)=\frac{m^{2}g^{2}}{2k}(1+\cos ^{2}\omega t)
$$

#Physics #Vibrations 