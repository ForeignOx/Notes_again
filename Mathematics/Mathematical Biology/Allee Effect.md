Some guy realised that goldfih survive longer when there are more fih in the tank:
$$
\frac{d x}{dt} =-ax\left( 1-\frac{x}{K} \right)\left( 1-\frac{x}{A} \right)
$$
With $0<A<K$, which is a cubic in phase space:
```desmos-graph
A=3
K=5

y=-x*(1-x/K)*(1-x/A)
(0,2)|label:dx/dt|hidden
(6,0)|label:x|hidden
```
This is bistable, it goes stable, unstable, stable. In general stability always alternates (in 1)
It sensitive to initial conditions. $a$ scales time, but it makes no long term difference