This is a 'flat' coil that is turned by some external means in a [[Uniform Magnetic Fields|uniform magnetic field]]. As it rotates, the [[Flux Linkage]] changes, so an [[Emf]] is [[Emf Induced in a Moving Conductor|induced]]. For simplicity, we consider a rectangular coil, WXYZ, represented as a single turn
![[Simple Alternating Current Generator 2024-04-23 17.38.09.excalidraw]]
![[Simple Alternating Current Generator 2024-04-23 17.44.30.excalidraw]]
When the normal to the coil is at angle $\phi$ to the field, the [[Magnetic Flux]], $\Phi$ through the coil is
$$
\Phi=BA\cos \phi
$$
For a coil of $N$ turns, the flux linkage is
$$
N\Phi=NBA\cos \phi
$$
$A\cos \phi$ is the area that the coil presents normally to the flux. For example, when $\phi=0$, the coil presents 'full frontally' and $A\cos \phi=A$, but when $\phi=\frac{\pi}{2}$, the coil presents 'edge-on' and $A\cos \phi=0$
To find out how the emf changes with time, we note that, if the coil is being turned at a steady [[Angular Velocity]] $\omega$, then at time $t$:
$$
\phi=\omega t+\phi_{0}
$$
Here, $\phi_{0}$ is the angle that the normal to the coil makes with the field direction at time $t=0$. In general:
$$
N\Phi=NBA\cos(\omega t+\phi_{0})
$$
Due to [[Faraday's Law]], the emf is the negative derivative of this with respect to time, so:
$$
\mathscr{E}=BAN\omega \sin(\omega t+\phi_{0})
$$

## Peak emf
The maximum value of $\sin(\omega t+\phi_{0})$ is exactly 1, so the peak or maximum value of the emf is given by:
$$
\mathscr{E}_\text{max}=BAN\omega
$$

#Physics #Electromagnetic_induction #Equation