From early in the 20th century, physicists have used high-speed particles as missiles to 'fire' at nuclei and, later, at smaller targets, such as nucleons. By noticing how the missile particles are deflected, and what comes out of the target particles and in which directions, physicists have learned much about the structure of subatomic particles
At first, [[Alpha Decay|$\alpha$]] particles from [[Nuclear Radiation|radioactive]] sources were used as missile particles. This is how the very existence of the atomic nucleus was revealed. But for more detailed work, $\alpha$ particles have too much internal structure of their own and not enough [[Kinetic Energy]]
## The Electron Gun
![[Pasted image 20240415214514.png]]
In the 1920s, physicists started to develop ways of accelerating particles such as electrons and protons. The electron gun is a simple form of accelerator - one in which the acceleration occurs in a single step.
The electrons are emitted from a metal filament heated to a high temperature by passing a [[Electric Current|current]] through it. They are accelerated towards a cylindrical metal 'anode' by means of a potential difference applied between cathode and anode. Many electrons are captured by the anode and returned straight to the filament via the power supply, but some escape through a small hole in the anode's end cap, to form the beam. The speed $v$, of these escapees is easily found, using:
$$
\frac{1}{2}mv^{2}=qV
$$
Unfeasibly, enormous [[Potential Difference|potential differences]] would be needed to give the particles enough kinetic energy for use as missiles in modern particle physics. The problem is overcome by accelerating the particle over and over again, through a large potential difference...
## The Linear Accelerator
Below is a diagram of a simplified linear accelerator
![[Particle Accelerators 2024-04-15 21.28.48.excalidraw]]
Suppose the particles to be accelerated are positively charged. They will be accelerated across the first gap into drift tube (1), when this is at a negative potential with respect to the particle production chamber (0). The particles will travel through the first drift tube at constant speed. The potential difference needs to alternate at such a [[Frequency]] that (2) is negative with respect to (1) when the particles reach the gap between (1) and (2), but the potential difference has reversed again so that (3) is negative with respect to (2) when the particles reach the gap between (2) and (3) and so on. The increasing length of the drift tubes is designed to keep pace with the increasing speed of the particles, so that the frequency of the alternating potential difference can be roughly constant
The longest linear accelerator in the world ($3.2\pu{ km}$) forms a main part of the SLAC laboratory in California. It accelerates electrons or positrons up to kinetic energies of $50\pu{ GeV}$
## The Cyclotron
The cyclotron is a particle accelerator that can take up much less space than the equivalent linear accelerator. This is because a cyclotron uses a [[Magnetic Fields|magnetic field]] (at right angles to the particle velocity) to confine the charged particles to (semi)circular paths between the times when they acquire kinetic energy
![[Pasted image 20240415215757.png]]

A particle sent out from the injector gets faster each time it crosses the gaps between the hollow electrode chambers, because a high voltage is applied between them. The potential difference must alternate with a [[Period|periodic time]] equal to the time, $T_{C}$, for the particle to make one revolution. When the particle has attained a speed $v$ and a path radius $r$, we can calculate $T_{C}$ using what we know about [[Magnetic Fields on Moving Charges]]:
$$
T_{C}=\frac{2\pi r}{v}=\frac{2\pi}{v}\times \frac{mv}{Bq}=\frac{2\pi m}{Bq}
$$
The reciprocal of $T_{C}$ gives us the frequency of revolution, the number of circles per second. It is sometimes called the cyclotron resonance frequency, $f_{C}$, but it applies to any charged particle moving at right angles to a uniform magnetic field, provided $v\ll c$. We have then:
$$
f_{C}=\frac{Bq}{2\pi m}
$$
The really neat thing is that $T_{C}$ and $f_{C}$ are independent of $v$ and $r$. The faster the particle, the wider its circular path, and these factors cancel
Therefore we should be able to stick with only one frequency of alternating voltage for all particles of the same type anywhere in the cyclotron...
The cyclotron was invented in 1932 and was brilliant for producing fast protons to use as missiles in nuclear research. Cyclotrons are still used in hospitals to produce proton beams for cancer therapy and for bombarding nuclei to produce short-lived isotopes. Unfortunately, for cutting-edge experiments in particle physics, the cyclotron simply can't give particles enough kinetic energy
For one thing, as a particle's speed approaches the speed of light, its path radius increases faster than its speed, and the time per revolution increases. A cyclotron can be modified to deal with this, but a more serious issue is the very large path radii of high energy particles, which would require the magnetic field to be applied over a very wide disc-shaped region. The electromagnet would have to be vast
## The Synchrotron
In a synchrotron, the particles go round and round in a circular path. Thus, no magnetic field is needed at other radii. Even better, the field can be applied at regular stations along the path rather than all along it:
![[Particle Accelerators 2024-04-15 22.17.57.excalidraw]]
All the same, the Super Proton Synchrotron at CERN has 744 path-bending electromagnets along its $7\pu{ km}$ circumference. In the SPS, the particles are given kinetic energy by electric fields in radio frequency cavities at two places in the circular path, every time they go round it. What is sacrificed in a synchrotron is the ability to produce high energy particles in a continuous stream. For the particles to remain in the same circular path as they gain kinetic energy, the magnetic field has to be increased continuously. The [[Magnetic Flux Density]] that is needed for particles that have done many circuits of the synchrotron would be too large for particles at earlier stages in the ride. The only thing to do is inject particles into the ring a batch at a time; in the SPS, typically around $10^{13}$ per batch, occupying less than the ring's circumference. A by-product of a synchrotron's operation is 'synchrotron radiation': photons of up to X-ray frequencies emitted by the charged particles as they are neglected by the electromagnets and undergo radial acceleration. Although extra power has to be supplied to the beam by the electric fields to compensate for this energy loss, the synchrotron radiation may be used for other experiments

#Physics #Magnets 