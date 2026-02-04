Molecules have a specific shape with specific angles, the reason this is the case is because bonds repel each other equally because bonds contain electrons. This means bonds will want to be as far apart as possible.
Lone pairs next to bond pairs repel more than 2 bond pairs together, 2 lone pairs repel even further. Generally, every lone pair reduces the remaining bond angle by $2.5^{\circ}$
## Without lone pairs
This is the table which dictates the general shapes:

| Coordination Number | Shape | Bond Angle(s) |
| ---- | ---- | ---- |
| 2 | Linear | $180^{\circ}$ |
| 3 | Trigonal Planar | $120^{\circ}$ |
| 4 | Tetrahedral | $109.5^{\circ}$ |
| 5 | Trigonal Bipyramid | $120^{\circ},90^{\circ}$ |
| 6 | Octahedral | $90^{\circ}$ |
Note that lone pairs count towards coordination number
### Shapes
Linear:

```tikz
\usepackage{chemfig}
\begin{document}
\chemfig{A-X-A}
\end{document}
```
Trigonal Planar:
```tikz
\usepackage{chemfig}
\begin{document}
\chemfig{A>[:30]X(>:[:150]A)-A}
\end{document}
```
Tetrahedral:
```tikz
\usepackage{chemfig}
\begin{document}
\chemfig{A>[:60]X(>:[:210]A)(-[:90]A)-[:-30]A}
\end{document}
```
Trigonal Bipyramid:
```tikz
\usepackage{chemfig}
\begin{document}
\chemfig{A>[:30]X(>:[:150]A)(-[:90]A)(-[:-90]A)-A}
\end{document}
```
Octahedral:
```tikz
\usepackage{chemfig}
\begin{document}
\chemfig{A>[:30]X(>:[:150]A)(>:[:30]A)(-[:90]A)(<[:-30]A)-[:-90]A}
\end{document}
```
## With lone pairs
This is the table which dictates the general shapes:

| Number of Bond Pairs and Lone Pairs | Shape | Example |
| ---- | ---- | ---- |
| BP = 3, LP = 1 | Pyramidal | $\ce{ NH_{3} }$ |
| BP = 2, LP = 2 | Bent | $\ce{ H_{2}O }$ |
| BP = 3, LP = 2 | Trigonal Planar | $\ce{ ClF_{3} }$ |
| BP = 4, LP = 2 | Square Planar | $\ce{ XeF_{4} }$ |

#Chemistry #Physical #Bonding 