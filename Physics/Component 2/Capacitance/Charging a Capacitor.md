We suppose that the [[Capacitor]] has no [[Electric Charge|charge]] on its plates initially, but that, at time $t=0$, the switch is closed, so that a fixed [[Potential Difference]], $V_{0}$ is applied across the $RC$ combination. At any time after $t=0$, the potential differences across $R$ and $C$ add up to $V_{0}$. Essentially:
$$
V_{C}+V_{R}=V_{0}=\frac{Q}{C}+IR
$$
The capacitor is charging, so the [[Electric Current|current]], which is the rate of flow of charge is positive:
$$
I=\frac{dQ}{dt}
$$
We know that $V_{0}=\frac{Q_{0}}{C}$, so we have the differential equation:
$$
R\frac{d Q}{dt} +\frac{Q}{C}=\frac{Q_{0}}{C}
$$
This can be solved using an [[Integrating Factor]]:
$$
\frac{d Q}{dt} +\frac{1}{RC}Q=\frac{Q_{0}}{RC}
$$
$$
\implies I=e^{ \int 1/RC \, dt  }=e^{ t/RC }
$$
$$
\implies Q=\frac{1}{e^{ t/RC }} \int \frac{Q_{0}}{RC}e^{ t/RC } \, dx 
$$
$$
\implies Q= e^{ -t/RC }(Q_{0}e^{ t/RC }+c)
$$
$$
\implies Q=Q_{0}\left( 1+\frac{c}{Q_{0}} e^{ -t/RC } \right)
$$
At $t=0$, $Q=0$, so we can see:
$$
Q_{0}=-c e^{ -0/RC }=-c
$$
Substituting this into the original equation we get:
$$
Q=Q_{0}(1-e^{ -t/RC })
$$
Using $Q=CV$ and $Q_{0}=CV_{0}$, where $V_{0}$ is the potential difference at $t=0$, we can say:
$$
CV=CV_{0}(1-e^{ -t/RC })
$$
$$
\implies V=V_{0}(1-e^{ t/RC })
$$
Using $V=IR$ and $V_{0}=I_{0}R$, where $I_{0}$ is the current at $t=0$, we can say:
$$
IR=I_{0}R(1-e^{ -t/RC })
$$
$$
\implies I = I_{0}(1-e^{ -t/RC })
$$

#Physics #Capacitance #Equation