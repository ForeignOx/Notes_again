When resistors are connected in series in order to divide up the [[Potential Difference]] we make a potential dividor
![[Potential Dividers 2024-03-18 22.17.53.excalidraw]]
We know from [[Ohm's Law]] that:
$$
V_{1}=IR_{1}
$$
$$
V_{2}=IR_{2}
$$
$$
\vdots
$$
$$
V_{n}=IR_{n}
$$
And hence
$$
V_\text{total}=I(R_{1}+R_{2}+\dots+R_{n})=IR_\text{total}
$$
By division, $\frac{V_{1}}{V_{2}}=\frac{R_{1}}{R_{2}}$ and so on, hence:
$$
\frac{V_{1}}{V_\text{total}}=\frac{R_{1}}{R_\text{total}}
$$
$$
\frac{V_{2}}{V_\text{total}}=\frac{R_{2}}{R_\text{total}}
$$
$$
\vdots
$$
$$
\frac{V_{n}}{V_\text{total}}=\frac{R_{n}}{R_\text{total}}
$$
So the ratio of potential differences is the ration of [[Resistance|resistances]] across which the potential differences would be measured
## Using a Potential Divider to give a desired Potential Difference
![[Potential Dividers 2024-03-18 22.39.44.excalidraw]]
If we place an input potential difference, $V_\text{in}$ across two resistors, we can obtain an output potential difference, and if we select the resistors correctly, we can have any output voltage we like (as long as $V_\text{out}\leq V_\text{in}$) since:
$$
\frac{V_\text{out}}{V_\text{in}}=\frac{R_{2}}{R_{1}+R_{2}}
$$
$$
\implies V_\text{out} =\frac{R_{2}V_\text{in}}{R_{1}+R_{2}}
$$
If we make one of the resistors a thermistor or an LDR, then we can make sensor circuits

#Physics #DC 