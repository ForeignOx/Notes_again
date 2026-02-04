The capacitance, $C$, of a [[Capacitor]] is the constant ratio of [[Electric Charge|charge]] on either plate divided by the [[Potential Difference]] between the plates:
$$
C=\frac{Q}{V}
$$
Capacitance has the unit $\pu{ CV-1=F }$, the farad
If a [[Batteries|battery]] is connected across a capacitor, some electrons are removed from one plate and transferred by the battery to the other. The plates gain equal and opposite charges (on facing surfaces). This 'charging' stops when the potential difference between the plates is equal to the [[Emf]] of the battery
![[Capacitance 2024-03-22 09.23.38.excalidraw]]
If we disconnect the battery, the charges are isolated on the plates, maintaining a potential difference between the plates. We can investigate how the charge ($\pm Q$) on the capacitor plates is related to the potential difference, $V$, and we find that the charge stored on either plate is proportional to the potential difference. So we can write:
$$
Q=CV
$$
## Capacitance of a parallel plate capacitor
We can design a capacitor to have a certain capacitance using a formula which holds so long as there is a capacitor with a vacuum of air between its plates (as long as their separation, $d$ is much less than their side length, $\sqrt{ A }$)
![[Capacitance 2024-03-22 09.32.57.excalidraw]]
It is:
$$
C=\frac{\epsilon_{0}A}{d}
$$
Where $\epsilon_{0}$ is the permittivity of free space. Note that $A$ is the area of a single surface of either plate
The formula for a parallel plate capacitor with dielectric is:
$$
C=\frac{\epsilon_{0}\epsilon_{r}A}{D}
$$
Where $\epsilon_{r}$ is a factor taking account of the dielectric
## Capacitors in parallel
![[Capacitance 2024-03-22 09.48.51.excalidraw]]
Each capacitor has the same potential difference, $V$, across it. The charges on the plates of $C_{1}$ and $C_{2}$ are therefore $\pm C_{1}V$ and $\pm C_{2}V$. So the charge that flows through the wires $X$ and $Y$ is:
$$
Q=C_{1}V+C_{2}V=(C_{1}+C_{2})V
$$
We can therefore see that capacitors in parallel sum their capacitances. This makes sense as you can think of it as making a larger capacitor with the two capacitors (assuming the value of $d$ remains constant)
## Capacitors in series
![[Capacitance 2024-03-22 10.01.42.excalidraw]]
When a potential difference, $V$ is applied, each capacitor's plates gain equal and opposite charges. These charges are the same for both capacitors because the island plates (the plates that are connected together) are insulated from everything else and must have a total charge of 0 (assuming neither capacitor had charge before connection). Because potential differences in series add, 
$$
V=V_{1}+V_{2}=\frac{Q}{C_{1}}+\frac{Q}{C_{2}}
$$
$$
\implies \frac{1}{C}=\frac{V}{Q}=\frac{1}{C_{1}}+\frac{1}{C_{2}}
$$
If there are more than two capacitors, we simply go on adding reciprocals
## Capacitance of a concentric sphere capacitor
A battery connected briefly between two concentric spherical metal shells (hollow spheres) will transfer electrons from one shell to the other. Equal and opposite charges will therefore coat the facing surfaces of the shells, and there will be a [[Electric Fields|field]] in the gap as shown in the diagram below
![[Capacitance 2024-03-26 18.36.29.excalidraw]]

The [[Electric Field Strength]]  in the gap, at a distance $r$ from the centre will simply be
$$
E=\frac{Q}{4\pi\epsilon_{0}r^{2}}
$$
radially outwards. This is entirely due to the charged inner sphere; the charged outer sphere contributes nothing, as the gap is part of the space inside it. Now suppose that the gap width $d$ is much less than the radius of the inner sphere, that is, $d\ll r$. We can then take the field as approximately constant across the gap and given by the above equation. Using $E=-\frac{dV}{dx}$, the potential difference between the shells is simply:
$$
|\Delta V|=\frac{Q}{4\pi\epsilon_{0}r^{2}}d=\frac{Q}{\epsilon_{0}A}d
$$
Where $A$ is the surface area of the inner shell, and almost that of the outer shell, from the definition of capacitance:
$$
C=\frac{Q}{|\Delta V|}=\frac{\epsilon_{0}A}{d}
$$
Which is the same result as with a parallel plate capacitor, as expected since $r\gg d$

#Physics #Capacitance #Equation