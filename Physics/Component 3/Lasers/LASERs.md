Lasers work by [[Stimulated Photon Emission]]. Consider, an atom undergoes stimulated emission and produces two [[Photoelectric Effect|photons]]. If each of these photons now interacts with an atom in the upper state, there will be four photons: the light will be progressively amplified as it passes through the medium, giving rise to the name laser: 
    **L**ight **A**mplification by the **S**timulated **E**mission of **R**adiation
Clearly for the light to be continuously amplified in this way, the photons have to carry on meeting atoms, all of which are in the upper state, this is not very likely to occur naturally
For convenience, we'll consider a monatomic gas. Suppose we could have a gas at room temperature with all the molecules being in the ground state (G). The molecules could be put into an excited state (E) occasionally by collision; some of the [[Kinetic Energy]] of the molecules is used to put one of the molecules into the state E (an [[Inelastic Collisions|inelastic collision]]), however, the next time the excited molecule collides, it is likely to be with a molecule in the ground state and also likely to drop again into the ground state with the energy reappearing as translational kinetic energy (this is also known as a superelastic collision). Also, the molecule is likely after a short time to lose its extra [[Energy]] by spontaneous emission. If we raised the temperature, all we'd achieve is to increase the fraction of molecules in the excited state. The best we can hope is that as we raise the temperature to approach 50% of the molecules being excited because at this point the collisions would be equally likely to decrease or raise the energy level. Essentially, lasers can only work if a [[Population Inversion]] is achieved. In order to do this, we need to find some non-thermal means of boosting the population of the upper state, we call such a process [[Pumping]]. It is not normally possible to achieve population inversion with a two-state system because the upper state will usually empty as fast as it fills
## Three-State Laser Systems
![[LASERs 2024-04-11 16.13.13.excalidraw]]
The three states are referred to as the ground state (G), the pumped state (P) and the upper state (U)
Note that downward transitions can occur by a variety of routes, not all of which are equally likely. Laser engineers choose systems in which state P is much more likely to decay via the intermediate state U, rather than directly back to G. Some energy states are very short-lived, so they are populated only for a very brief period of time before decaying
If the laser medium is pumped, for example by [[Optical Pumping]], atoms in the ground state will be raised to the pumped state and rapidly decay into the metastable upper state (partly by [[Spontaneous Photon Emission|spontaneous emission]] but mainly collisions). If the pumping is rapid enough, the population of U will exceed that of G, i.e. a population inversion will have been achieved: any spontaneous transition from U to G will produce a photon which will stimulate emissions from other atoms in state U
Historically, a three-state laser based on a ruby laser medium was the first one to be built. However, because over half the atoms in the ground state must be pumped to achieve laser operation, three-state laser systems are inefficient, so we tend to use four-state systems
## Four-State Laser Systems
![[LASERs 2024-04-11 16.31.17.excalidraw]]
The characteristics of the pumped and upper states in a four-state laser are the same as in the three-state laser. The additional, lower, state (L), is between the upper and round states. L is a short-lived state and rapidly decays, mainly by collisions, to G. The advantage of this system over the three-state laser is that L is initially empty, so a population inversion between L and U is present from the first few electrons in U. The short-lived nature of L ensures that population inversion is maintained with a much lower level of pumping, and hence requires less energy input than the three-state laser
## Laser Inefficiency
Most of the energy input into the laser is converted into the [[Internal Energy]] of the atoms of the amplifying medium rather than raising the energy state of the atoms themselves from G to P. Even for successful pumping evens, the energy input is $E_\text{P}-E_\text{G}$ but the lasing output is less: $E_\text{U}-E_\text{L}$ for a four-state laser, $E_\text{U}-E_\text{G}$ for a three-state laser
## Laser Construction
### Ruby Laser
The ruby laser was the first one to be produced
![[Pasted image 20240411164331.png]]
The laser operates as follows:
- The pumping radiation creases a population inversion in the amplifying medium
- Photons of energy $E_\text{U}-E_\text{L}$ or $E_\text{U}-E_\text{G}$ are produced by spontaneous emission in the amplifying medium
- These photons pass through the amplifying medium and produce two coherent photons travelling in the same direction by stimulated emission. Each photon becomes two, four, eight etc. in an exponential increase
- The photons travelling parallel to the axis of the medium are reflected backwards and forwards stimulating more photons and eventually escaping through the partly transmitting mirror in the laser beam
- A dynamic equilibrium is soon established when the rate of escape of photons is equal to the rate of their production
### Semiconductor Diode Laser
The lasers in everyday households are almost all semiconductor laser diodes. These are constructed out of small chips of semiconductor material, often gallium arsenide, $\ce{ GaAs }$. They have many advantages:
- They are electrically pumped and operate at low [[Potential Difference|voltage]]
- The laser chip is very small and can e incorporated into small standard electrical packages for wiring into circuits
- They are very [[Efficiency|efficient]]
- They can be mass-produced cheaply
Typical uses in the home are DVD and CD reading and writing, Blu-ray reading, optical fibre data transfer, computer scanners and printer. The structure of a typical semiconductor is shown below:
![[Pasted image 20240411165745.png]]
See [[Light Emitting Diodes|LEDs]]. The advantage of semiconductor laser diodes for optical fibres relates to the spectral purity of the output (practically only one [[Frequency]]) and the [[Coherence]] of the output, which allows for very rapid switching

#Physics #Lasers 