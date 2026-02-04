When the [[Magnetic Flux]], $\Phi$, through a circuit changes, an [[Emf]] is [[Emf Induced in a Moving Conductor|induced]] in the circuit, proportional to the rate of change of flux linkage. For a circuit with $N$ identical turns:
$$
\mathscr{E}=-\frac{d(N\Phi)}{dt}
$$
$N\Phi$ is the [[Flux Linkage]]. If the circuit is a coil of $N$ turns, each with the same flux, $\Phi$, through each, the emf is the same as if there were $N$ times the flux through a single turn
## Rod on Rails
The law gives the emf induced in a circuit in the general case. For a rod on rails, in the time $\delta t$, the rod sweeps across and area $l\times v\delta t$
![[Faraday's Law 2024-04-22 18.16.42.excalidraw]]
Because the [[Magnetic Flux Density|flux density]] is normal to the area ($\phi=0$) the flux linked with the circuit has increased by an amount
$$
\delta \Phi=B\times l\times v\delta t
$$
This much more flux goes through WXYZ than when it was W\[X]\[Y]Z. Since $N=1$, Faraday’s law gives the induced emf magnitude as:
$$
\mathscr{E}=\frac{\delta\Phi}{\delta t}=\frac{Blv\delta t}{\delta t}=Blv
$$
## Loop Moving in a [[Uniform Magnetic Fields|Uniform Magnetic Field]]
![[Faraday's Law 2024-04-22 18.26.21.excalidraw]]
Side ZW of the wire loop has an induced emf, $Bbv$, in the direction WZ and XY has an emf, $Bbv$, in the direction XY. These emfs are in opposite 'senses' meaning that, as we go round the circuit, the emfs encountered are equal and opposite. The resultant emf is zero. Using Faraday's Law, we say that, as the whole loop is moving, and the field is uniform, the same amount of flux is always passing through it, so
$$
\mathscr{E}=\frac{d\Phi}{dt}=0
$$
## Shrinking Band Cutting Flux
Suppose a round balloon with a band of metallic paint around its equator deflates by a radius $\delta r$ in a time $\delta t$. Assuming a uniform field of strength $B$ is at right angles to the balloon's equatorial plane, as the area enclosed by the band decreases, so does the flux linked with it. $N=1$ and the flux density is always normal to the area, so $\phi=0$
![[Faraday's Law 2024-04-22 18.54.33.excalidraw]]
We therefore have:
$$
\mathscr{E}=\frac{d\Phi}{dt}=\frac{d(BA)}{d t}=B \frac{dA}{dt}
$$
And $\frac{d A}{dt}=\pi \frac{(\delta r)^{2}}{\delta t}$, so:
$$
\mathscr{E}=\frac{B(\delta r)^{2}}{\delta t}
$$
Note that this is in fact the mean emf
## Mean emf in a Loop Turning in a Uniform Field
Suppose that, in a time $\delta t$, we turn a metal loop through $\pi$ in a magnetic field so that the normal to its plane shown below changes from being parallel to a uniform magnetic field to being antiparallel
![[Faraday's Law 2024-04-22 20.12.26.excalidraw]]

Initially, the flux through the loop is $BA$, in which $A$ is the area enclosed by the ring. Finally, the flux of the same magnitude, $BA$, threads through the ring in the opposite direction. This counts as a flux change of $2BA$. So the mean emf is:
$$
\mathscr{E}=\frac{d\Phi}{dt}=\frac{2BA}{\delta t}
$$

## Mutual Induction
This occurs when a changing [[Electric Current|current]] in one circuit causes an emf to be produced in another circuit, because some or all of the (changing) magnetic flux produced by the first is linked with the second
![[Faraday's Law 2024-04-22 20.43.25.excalidraw]]
Suppose that the current in the [[Magnetic Field due to a Current in a Circuit|long solenoid]] is reduced at a constant rate from $I_{0}$ to zero in a time $\delta t$, we can calculate the emf induced as a result in the $N$-turn coil inside the solenoid. In the central region of the solenoid, the flux density is uniform and parallel to the axis of the axis of the solenoid. Its magnitude is 
$$
B=\mu_{0}MI_{0}
$$
So the initial flux linkage for the $N$ turn coil is:
$$
N\Phi=NBA=N\mu_{0}MI_{0}A
$$
In which $A=\pi r_{1}^{2}$. So the emf in the $N$-turn coil is:
$$
\mathscr{E}=\frac{d(N\Phi)}{dt}=\frac{\pi\mu_{0}I_{0}MNr_{1}^{2}-0}{\delta t}=\frac{\pi \mu_{0}I_{0}MNr_{1}^{2}}{\delta t}
$$

#Physics #Electromagnetic_induction #Law #Equation