The potential difference, $V$ between two points $X$ and $Y$ is the [[Work]] done, i.e. the loss of electrical potential energy per unit charge passing between $X$ and $Y$. It has unit volt, $\pu{ V =JC-1}$
![[Potential Difference 2024-03-24 21.27.05.excalidraw]]
$X$ is said to be at a higher potential if the voltmeter gives a positive reading
## Potential Difference in Parallel Circuits
![[Potential Difference 2024-03-18 20.11.57.excalidraw]]
Since voltmeters read a difference in potential, the two voltmeters in the above diagram must read the same value as, even though they are around different components, they also measure the potential difference across the rest of the circuit, which is identical. The essentially means that when components are in parallel, the potential differences are equal. More fundamentally, potential differences arise from forces on free electrons due to distributions of [[Electric Charge|charge]] brought about by the [[Batteries|battery]]. The forces do work on free electrons going from one point to another. The amount of work is independent of the route taken between the points
## Potential Difference in Series Circuits
![[Potential Difference 2024-03-18 20.35.00.excalidraw]]
Finally consider potential differences across components in series, for an electron going from $Y$ to $X$, the work done on it as it goes through either the lower resistor or the filament lamp is $eV_{2}$, and as it goes through the top resistor is $eV_{1}$, so the total amount of work as it goes from $Y$ to $X$ is $(eV_{1}+eV_{2})$, but it is also $eV_{3}$, so $eV_{1}+eV_{2}=eV_{3}$, dividing through by $e$:
$$
V_{1}+V_{2}=V_{3}
$$
Hence potential differences in series add together
## Potential Difference of a Power supply
Using the [[Internal Resistance]] relationship and $I=\frac{V}{R}$ we can calculate the potential difference of a power supply:
$$
V=E-Ir=E-\frac{V}{R}r
$$
$$
\implies V=\frac{ER}{R+r}
$$
## Potential Difference in an [[Electric Fields|Electric Field]]
The potential difference, $\Delta V$, between two points, $A$ and $B$ in an electric field is the work done per unit charge ($\frac{W}{q}$) by the field on a test charge, $q$, going from $A$ to $B$. If $\frac{W}{q}>0$, $A$ is at the higher potential. 
Suppose that a test charge, $q$ is displaced by $\delta x$. from $A$ to $B$ in the direction of a [[Uniform Electric Field]]. It loses [[Electrical Potential Energy]] (EPE) equal to the work done on it by the field. So:
$$
\text{Change in EPE of }q = -(\text{force on }q\times\delta x)
$$
Dividing both sides by $q$:
$$
\delta V=-E\delta x
$$
In which $E=\frac{\text{force on }q}{q}=$ electric field strength in $x$ direction, and $\delta V=\frac{\text{change in EPE of }q}{q}=$ potential difference between $A$ and $B$, so essentially:
$$
E=-\frac{dV}{dx}
$$
There are a few things to note:
- $\delta V$, like $E$, is defined so as not to depend on the magnitude or sign of the test charge, $q$, (as long as $q$ isn't too large)
- We would have reached the same value for $\delta V$ by taking $q$ on any route between $A$ and $B$. For example, the work done on $q$, divided by $q$, in going from $A$ to $C$ would also be $E\delta x$, because only the displacement component, $\delta x$, in the direction of $E$ counts. No further work is done in going from $C$ to $B$. We say that the potential difference between two points in an electric field due to static charges is path-independent

#Physics #Resistance #Definition