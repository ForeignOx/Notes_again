## For $n \in \mathbb{R}^+$ what can be said about $n^{2}$?
If $0<n<1$ then by multiplying by $n$:
$$
0<n^{2}<n<1
$$
$$
\implies 0<n^{2}<1
$$
If $n>1$ then by multiplying by $n$:
$$
n^{2}>n>1
$$
$$
\implies n^{2}>1
$$

## For $n \in \mathbb{R}^+$, what can be said about $n$?
If $0<n^{2}<1$ then:
$$
n^{2}<1
$$
$$
\implies n^{2}-1<0
$$
$$
\implies (n-1)(n+1)<0
$$
as $n+1>0$:
$$
\implies n-1<0
$$
$$
\implies 0<n<1
$$

If $n^{2}>1$ then:
$$
n^{2}-1>0
$$
$$
\implies (n-1)(n+1)>0
$$
as $n+1>0$:
$$
\implies n-1>0
$$
$$
\implies n>1
$$
## Given $a,n \in\mathbb{R}^+$
$$
n>\sqrt{ a }\iff n^{2}>a
$$
$$
n<\sqrt{ a }\iff n^{2}<a
$$
### Proof:
If $n>\sqrt{ a }$:
$$
n^{2}>n\sqrt{ a }>\sqrt{ a }\sqrt{ a }=a
$$
$$
\implies n^{2}>a
$$
If $n^{2}>a$:
$$
n^{2}-a>0
$$
$$
\implies(n+\sqrt{ a })(n-\sqrt{ a })>0
$$
As $n+\sqrt{ a }>0$:
$$
n-\sqrt{ a }>0
$$
$$
\implies n>\sqrt{ a }
$$
If $n<\sqrt{ a }$, by multiplying by $\sqrt{ a }$, we get:
$$
n\sqrt{ a }<a
$$
As $n^{2}<n\sqrt{ a }$:
$$
n^{2}<a
$$
If $n^{2}<a$:
$$
n^{2}-a<0
$$
$$
\implies (n-\sqrt{ a })(n+\sqrt{ a })<0
$$
Since $n+\sqrt{ a }>0$
$$
n-\sqrt{ a }<0
$$
$$
\implies n<\sqrt{ a }
$$
## Given that $x,a \in\mathbb{R}$ and $b\in\mathbb{R}^+$, prove that $|x-a|<b \iff a-b<x<a+b$


## Given that $\varepsilon \in\mathbb{R}^+$ and $n\in\mathbb{N}$ prove that $n> \frac{1}{\sqrt{ \varepsilon }}\implies \frac{1}{n^{2}}<\varepsilon$ 
If $n> \frac{1}{\sqrt{ \varepsilon }}$, since $\varepsilon>0\implies \sqrt{ \varepsilon }>0$
$$
n\sqrt{ \varepsilon }>1
$$
$$
\implies \sqrt{ \varepsilon }> \frac{1}{n}
$$
$$
\implies \varepsilon< \frac{1}{n^{2}}
$$
Due to the proof above
## Given that $\epsilon \in \mathbb{R}^+$ and $n\in\mathbb{N}$, prove that $n> \frac{1}{\varepsilon^{2}}\implies \frac{1}{\sqrt{ n }}<\varepsilon$
If $n> \frac{1}{\varepsilon^{2}}$, $\varepsilon^{2}>0$
$$
n\varepsilon^{2}>1
$$
$$
\implies \varepsilon^{2}> \frac{1}{n}
$$
$$
\implies \varepsilon>\frac{1}{\sqrt{ n }}
$$
As required
## Given that $\epsilon \in\mathbb{R}^+$ and $n\in\mathbb{N}$ prove that $n>\frac{1}{\varepsilon}\implies \frac{n}{n^{2}+5}<\varepsilon$
If $n>\frac{1}{\varepsilon}$, since $\varepsilon>0$, $n>0$
$$
n\varepsilon>1
$$
$$
\implies \varepsilon>\frac{1}{n}
$$
Consider
$$
\frac{1}{n}-\frac{n}{n^{2}+5}=\frac{n^{2}+5-n^{2}}{n(n^{2}+5)}=\frac{5}{n(n^{2}+5)}>0
$$
Since $5>0,n>0,n^{2}+5>0$
$$
\implies \frac{1}{n}>\frac{n}{n^{2}+5}
$$
$$
\implies \varepsilon>\frac{1}{n}>\frac{n}{n^{2}+5}
$$
$$
\therefore \frac{n}{n^{2}+5}<\varepsilon
$$
As required
## Given that $\epsilon \in\mathbb{R}^+$ and $n\in\mathbb{N}$ prove that if $n>\frac{1}{2\varepsilon}$ and $n>10$ then $\frac{1}{3n-10}<\varepsilon$ 
If $n>\frac{1}{2\varepsilon}$, since $\varepsilon>0$, $n>10$
$$
2n\varepsilon>1
$$
$$
\implies \varepsilon>\frac{1}{2n}
$$
Consider
$$
\frac{1}{2n}-\frac{1}{3n-10}=\frac{3n-10-2n}{2n(3n-10)}=\frac{n-10}{2n(3n-10)}>0
$$

Since $n>10, 3n>10$ 
$$
\implies \frac{1}{2n}>\frac{1}{3n-10}
$$
$$
\therefore \varepsilon>\frac{1}{2n}>\frac{1}{3n-10}
$$

$$
\implies \frac{1}{3n-10}<\varepsilon
$$
As required
## Given that $\varepsilon \in\mathbb{R}^+$ and $n\in\mathbb{N}$ prove that $n>\frac{7}{\varepsilon}\implies | \frac{4n}{2n+7}-2|<\varepsilon$
If $n>\frac{7}{\epsilon}$, since $\varepsilon>0$ and $n>0$
$$
\varepsilon n>7
$$
$$
\implies \varepsilon>\frac{7}{n}
$$
Consider
$$
\frac{4n}{2n+7}-2=\frac{4n-2(2n+7)}{2n+7}=\frac{4n-4n-14}{2n+7}=-\frac{14}{2n+7}<0
$$
Since $2n+7>0$
$$
\implies \left| \frac{4n}{2n+7}-2\right|=\frac{14}{2n+7}
$$
Consider
$$
\frac{7}{n}-\frac{14}{2n+7}=\frac{7(2n+7)-14n}{n(2n+7)}=\frac{14n+49-14n}{n(2n+7)}=\frac{49}{n(2n+7)}>0
$$

$$
\implies \frac{7}{n}>\frac{14}{2n+7}=\left| \frac{4n}{2n+7}-2\right|
$$
$$
\implies \varepsilon>\frac{7}{n}>\left| \frac{4n}{2n+7}-2\right|
$$
$$
\therefore \left| \frac{4n}{2n+7}-2\right|<\varepsilon
$$

#Mathematics #Analysis 