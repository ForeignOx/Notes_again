The Hall effect gave the first indication that the [[Motor Effect]] force on a [[Electric Current|current]]-carrying metal [[Electrical Conductors|conductor]] arises from forces on negative charge carriers moving inside it. The Hall effect results from the magnetic field exerting a force towards one side of the conductor on the carriers. Although the effect occurs in metals, it is much greater in semiconductors, such as silicon. The thinner the specimen, the larger the effect. Thin pieces of semiconductor used to show the Hall effect are often called 'Hall wafers'. We shall first consider a wafer made of silicon doped (alloyed) with a small amount of phosphorus. This material is called an 'n type' semiconductor
![[Hall Effect 2024-04-16 18.14.56.excalidraw]]
A circuit is set up to send a current lengthways through the wafer. With no applied magnetic field, there should be no [[Potential Difference]] between points exactly opposite each other on the side faces, so the voltmeter should read 0. When a magnetic field is applied in the direction shown, across the whole of the wafer - not difficult, because the area of its largest face may well be less than that enclosed by a centimetre squared. The voltmeter indicates a small potential difference, $V_\text{H}$ with the left-hand face at a higher potential. This is just what we'd expect if free electrons in the wafer had been deflected in accordance with [[Fleming's Left Hand Motor Rule]], remembering their negative charge
If we repeat the experiment with a wafer made of a p-type semiconductor such as silicon doped with indium, we find that the Hall voltage is the other way round. The right-hand face is at a more positive potential than the left hand. We infer that the mobile charge carriers in this wafer are predominantly the positive holes, and are deflected again in accordance with the left-hand rule
Within a small fraction of a second applying $B$, the side faces of the wafer acquire charge, and there will be a transverse [[Electric Fields|electric field]], $E$, inside the wafer. This will present further build-up of charge by producing a force to the left on the free electrons, equal and opposite to the magnetic force. Thus:
$$
(\pm e)E=(\pm e)vB
$$
$$
\implies E=Bv
$$
This is the '[[Crossed Electric and Magnetic Fields in a Vacuum|crossed fields]]' condition for the charge carriers, with drift speed $v$, to pass undeflected through the wafer. The magnitude of the Hall voltage, $V_\text{H}$, measured between points separated by the width $w$, of the wafer with width-ways electric field strength, $E$, is:
$$
V_{H}=Ew=Bvw
$$
It helps to re-express $v$ in terms of the current through the wafer, using $I=nAve$. $A$ is the cross-sectional area of the conductor normal to the current direction, that is the area, $wt$ of the small face. So:
$$
v=\frac{I}{nwte}
$$
$$
\implies V_\text{H}=\frac{BIw}{nwte}=\frac{BI}{nte}
$$
In which $n$ is the free electron or hole concentration and $t$ is the thickness of the wafer
Note these features of the equation:
- $V_\text{H}$ is proportional to $B$, the [[Magnetic Flux Density]]. A hall wafer, mounted in a 'probe', with a connecting cable to an external current supply and voltmeter, provides a practical way of measuring $B$, even when it varies significantly over distances of few $\pu{ mm}$. Measuring the force on a current-carrying wire isn't practicable in such cases
- The smaller the thickness, $t$ of the wafer and the smaller the free electron concentration, $n$, the larger $V_\text{H}$. This is because, for a given current, $I$, decreasing either of these factors increases the [[Drift Velocity|drift speed]], $v$, and therefore the magnetic force on each charge carrier
- The factor $\frac{1}{ne}$ is called the 'Hall coefficient'. It contains the quantities determined by the wafer material. It is sometimes negative if the predominant charge carriers are negative

#Physics #Magnets #Equation 
