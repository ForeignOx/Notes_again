This is a predator prey model, and has an alternative to self-competition; it has a second population
For example let's have our prey be greenflies $x(t)$, and predators be ladybirds $y(t)$ what's the effect on $\frac{d x}{dt}$? How many of our greenflies are eaten? This is dependent on how many greenfly-ladybird interactions there are, which is represented by $xy$
Soooo
$$
\frac{d x}{dt} =ax-bxy
$$
The first term is infinite food, so $a$ is birth rate, then $b$ is the proportion of these interactions that lead to greenflies being eaten
Then for $y$?
$$
\frac{d y}{dt} =-cy+dxy
$$
As without food, $c$ of them die, then $d$ is the availability of food.
Note that $b\neq d$ necessarily, as a ladybird might have to eat many greenflies to reproduce
If you plot $x$ against $y$ you get a goofy egg shape, this means that it is periodic or something
## Parameter Reduction in Lotka-Volterra
One might ask however, are all the $a,b,c,d$ all necessary??
Let's non-dimensionalise:
$$
x=\hat{x}X,y=\hat{y}Y,t=\hat{t}T
$$
Where $\hat{x},\hat{y},\hat{t}$ are non dimensional and the capitals are units... The equations become:
$$
\frac{d \hat{x}}{d\hat{t}}  \frac{X}{T}=a\hat{x}X-b\hat{x}\hat{y}XY
$$
$$
\frac{d \hat{y}}{d\hat{t}}  \frac{Y}{T}=-c\hat{y}Y+d\hat{x}\hat{y}XY
$$
$$
\implies \frac{d \hat{x}}{d\hat{t}} =a\hat{x}T-b\hat{x}\hat{y}YT
$$
$$
\implies\frac{d \hat{y}}{d\hat{t}} =-c\hat{y}T+d\hat{x}\hat{y}XT
$$
Now we pick $T,X,Y$ to remove as many parameters as possible. Let's say $T=\frac{1}{a},Y=\frac{a}{b},X=\frac{c}{d}$, so we get
$$
\frac{d \hat{x}}{d\hat{t}} =\hat{x}-\hat{x}\hat{y}
$$
$$
\frac{d \hat{y}}{d\hat{t}} =\gamma(-\hat{y}+\hat{x}\hat{y})
$$
Where $\gamma=\frac{c}{a}$, and these equations are known as the non-dimensional Lotka-Volterra model, so there is only 1 independent parameter which is pretty cool, every other solution is a scaling in $X,Y$ or $T$ 
## Solutions
In the non-dimensional system, if we divide the second equation by the first we get:
$$
\frac{d y}{dx} =\frac{\gamma(-y+xy)}{x-xy}=\frac{\gamma y(-1+x)}{x(1-y)} 
$$
$$
\implies \int \frac{1-y}{y} \, dy=-\gamma \int \frac{1-x}{x} \, dx 
$$
$$
\implies \log y-y=-\gamma(\log x-x)+c  
$$
## Equilibria
We have equilibrium when
$$
\frac{d x}{dt} =\frac{d y}{dt} =0
$$
$$
\implies x(1-y)=0,  y(x-1)=0
$$
So $(0,0)$ and $(1,1)$ are the two equilibria. The first represents extinction, 