We'll suppose that the [[Capacitor]] has been charged in advance and that, at time $t=0$, a resistor is connected across it. At any time after that, we know that the [[Potential Difference]] across the resistor is equal to the potential difference across the capacitor, therefore
$$
IR=\frac{Q}{C}
$$
We shall rely on the resistor obeying [[Ohm's Law]], so that $R$, like $C$, is a constant. The [[Electric Current|current]], $I$ is the rate of flow of [[Electric Charge|charge]], in other words, the rate at which the negative plate loses negative charge and the positive plate loses positive charge, so:
$$
I=-\frac{dQ}{dt}
$$
Substituting this into the previous equation and dividing both sides by $-R$, we get:
$$
\frac{dQ}{dt}=-\frac{Q}{RC}
$$
$RC$ is called the time constant, $\tau$ of the circuit, and is a measure of how quickly the charge decays
This is a first order linear differential equation, which can be solved using separation of variables:
$$
\frac{1}{Q}\frac{d Q}{dt} =-\frac{1}{RC}
$$
$$
\implies \int \frac{1}{Q}  \, dQ =\int -\frac{1}{RC} \, dt 
$$

$$
\implies \ln\left( \frac{1}{c}Q \right)=-\frac{t}{RC}
$$
$$
\implies Q=c e^{ -t/RC }
$$
When $t=0$, the charge, $Q$, must take its initial value, $Q_{0}$, hence:
$$
Q=Q_{0}e^{ -t/RC }
$$
This is exponential decay
Using $Q=CV$ and $Q_{0}=CV_{0}$, where $V_{0}$ is the potential difference at $t=0$, we can say:
$$
CV=CV_{0}e^{ -t/RC }
$$
$$
\implies V=V_{0}e^{ -t/RC }
$$
Using $V=IR$ and $V_{0}=I_{0}R$, where $I_{0}$ is the current at $t=0$, we can say:
$$
IR=I_{0}Re^{ -t/RC }
$$
$$
\implies I=I_{0}e^{ -t/RC }
$$

#Physics #Capacitance #Equation