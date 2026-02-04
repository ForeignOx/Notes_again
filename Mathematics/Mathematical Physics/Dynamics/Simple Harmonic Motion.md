 Simple harmonic motion occurs when an object moves such that its acceleration is always directed towards a fixed point and is proportional to its distance from the fixed point
### Derivation
Consider a system such that:
![[Simple Harmonic Motion 2024-02-21 21.39.27.excalidraw]]
A sphere of mass $m$ is held in stable equilibrium at point O between two springs under tension. We shall consider the horizontal surface to be frictionless. If we move the sphere slightly to the left, the tension in spring A will decrease; the tension in spring B will increase. If we let the sphere go, there will be a resultant force on it to the right and it will therefore move back to its equilibrium position. When it gets back to O, the two tensions are equal, but the sphere is moving, so it carries on to the right, building up tension in A and lowering the tension in B. Hence decelerating until it stops and accelerates to the left...
The tension in the springs varies linearly with extension, so the restoring force, $F$, on the mass is directly proportional to the displacement, $x$, and in the opposite direction. By [[Newton's Second Law of Motion]], so is the acceleration $a$, i.e.
$$
F=-kx
$$
$$
a = -\frac{k}{m}x
$$
where $k$ is the stiffness of the arrangement of springs (in this arrangement, it is the sum of the spring constants of A and B), note that $k>0$
It is convenient to write $\frac{k}{m}$ as $\omega^{2}$. We can do this as both $k$ and $m$ are positive. Making this substitution gives
$$
a=-\omega^{2}x
$$
Where $\omega$ is angular frequency or pulsatance
## Graphical interpretations
Consider the function $x=A\cos \omega t$
```tikz
\begin{document}
  \begin{tikzpicture}[domain=0:5]
    \draw[very thin,color=gray] (-0.1,-4.1) grid (5.1,4.1);
    \draw[->] (-0.2,0) -- (5.2,0) node[right] {$t$};
    \draw[->] (0,-4.2) -- (0,4.2) node[above] {$x$};
    \draw[color=magenta]    plot (\x,{cos(2*\x r)})     node[right] {$x= A\cos\omega t$};
    \draw[color=green]   plot (\x,{-2*sin(2*\x r)}) node[right] {$x'= -\omega A\sin2
    \omega t$};
    \draw[color=cyan]   plot (\x,{-4*cos(2*\x r)}) node[right] {$x''= -\omega^2 A\sin\omega t$};
  \end{tikzpicture}
\end{document}
```
We see that $x''=-\omega^{2}A\cos\omega t$, so $x''=-\omega^{2}x$
Now also consider $x=A\cos(\omega t+\epsilon)$, $x''=-\omega^{2}A\cos(\omega t+\epsilon)$, so once again, $x''=-\omega^{2}x$
Since if $x$ is the displacement, $x'$ is $v$ and $x''$ is $a$. Hence the solution to the [[Second Order Ordinary Differential Equations|differential equation]] $a=-\omega^{2}x$ is:
$$
x=A\cos(\omega t+\epsilon)
$$
$$
\implies v=-\omega A\sin(\omega t+\epsilon)
$$
$$
\implies a = -\omega^{2}A\cos(\omega t+\epsilon)
$$
We know the extreme values of sine and cosine are $\pm 1$, so the maximum values for each are:
$$
x_{\text{max}}=A
$$
$$
v_{\text{max}}=\omega A
$$
$$
a_{\text{max}}=\omega^{2}a
$$
## Characteristics
### [[Amplitude|Amplitude]]
The amplitude of $x=A\cos(\omega t+\epsilon)$ is quite obviously $A$
### Phase
The phase of the system of equations is $\omega t+\epsilon$. as this is how far along in the motion the system is
### Period
The oscillation repeats itself with every increase by $2\pi$ in the value of the phase, in other works, if we add $T$ (the [[Period]]) to any time $t$, we add $2\pi$ to the phase:
$$
\forall t, \omega(t+T)+\epsilon=\omega t+\epsilon+2\pi
$$
$$
\implies \omega T=2\pi
$$
$$
\implies T=\frac{2\pi}{\omega}
$$
### Frequency
We can relate the period to the [[Frequency |frequency]] using $f=\frac{1}{T}$
$$
\implies\omega=2\pi f
$$
### Phase Constant
$\epsilon$ is the phase constant, and represents the shift from the starting point
### The relationship between velocity and displacement
We know
$$
v=-\omega A\sin(\omega t+\epsilon)=-\omega \sqrt{ A^{2}-A^{2}\cos ^{2}(\omega t+\epsilon) }=-\omega \sqrt{A^{2}-x^{2}  }
$$
## Light Spring Hanging under Gravity (Variant)
![[Simple Harmonic Motion 2025-01-22 11.28.48.excalidraw]]
Taking $x$ to point upwards, we have
$$
m\ddot{x}=-kx-mg
$$
Which is a second order non-homogeneous differential equation, so we have a complimentary function and a particular integral, and we get:
$$
x(t)=A\cos(\omega t)+B\sin(\omega t)-\frac{mg}{k}
$$
The effect is to shift the equilibrium by an amount $-\frac{mg}{k}$ 
Here
$$
V(x)=\frac{1}{2}kx^{2}+mg(x)
$$
Which will have a stationary point at $-\frac{mg}{k}$
## Damping


#Mathematics #Dynamics #Physics #Vibrations #Definition #Equation