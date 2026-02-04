Self-induction is the [[Emf Induced in a Moving Conductor|induction of an emf in a coil]] (or circuit) because of a changing [[Electric Current|current]] in that coil (or circuit)
A changing current in one coil induces an [[Emf]] in another coil, if flux from the first is linked with the second. But flux produced by any coil is linked with the very coil producing it, so we must have self-induction
A striking demonstration uses an inductor made of many turns of wire wound around an iron core. The two coils can be connected in series so that their fields are in the same sense around the core
![[Self-Induction 2024-04-23 19.50.40.excalidraw]]
When the switch is closed the lamp is slow to light, because of the emf in the conductor (often called a back-emf) opposing the battery emf, in accordance with [[Lenz's Law]]. When the switch is opened, it is important for no-one to be touching any part of the circuit. This is because the current, and therefore the magnetic flux, decreases to zero in a very short time, and a large emf is induced in the coil. This produces an arc at the switch contacts
___
We can calculate the magnitude of the emf when the current changes in a [[Magnetic Field due to a Current in a Circuit|long solenoid]] with no iron core
![[Self-Induction 2024-04-23 20.05.27.excalidraw]]
The flux through the solenoid, except near the ends, when it carries current $I$ is :
$$
\Phi=Ba=\mu_{0}nIA=\mu_{0}\frac{N}{l}IA
$$
Neglecting the decrease of flux near the ends (a good approximation if $l\gg \text{diameter}$),
$$
\text{Flux linkage}=N\Phi=\frac{\mu_{0}N^{2}A}{l}I
$$
If the current changes by $\delta I$, the change $\delta(N\Phi)$ in the flux linkage is:
$$
\delta(N\Phi)=\frac{\mu_{0}N^{2}A}{l}\delta I
$$
$$
\implies \int  \, dN\Phi =\int \frac{\mu_{0}N^{2}A}{l} \, dI  
$$
We hence call $\frac{\mu_{0}N^{2}A}{l}$ the [[Self-Inductance]], $L$, of the coil, using [[Faraday's Law]], we know:
$$
\mathscr{E}=\frac{d N\Phi}{dt} 
$$
$$
\implies \mathscr{E}=-L\frac{d I}{dt} 
$$
The value $L=\frac{\mu_{0}N^{2}A}{l}$ also holds for toroidal coils:
![[Self-Induction 2024-04-23 20.28.49.excalidraw]]
An iron core increases the inductance of a coil because of the extra [[Magnetic Flux|flux]] due to the alignment of magnetic domains. This extra flux is not strictly proportional to the current, so the inductance of an iron-cored coil is not really a constant, but depends upon the current, upon whether it is increasing or decreasing, and from what previous values

#Physics #Electromagnetic_induction 