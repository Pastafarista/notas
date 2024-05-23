#topología

- $\pi_1(X,x_0)$ es el grupo de [[lazo|lazos]] con base en $x_0$
- Cada lazo $\alpha$ con base en $y_0$ se puede [[Lazos equivalentes|convertir]] en un lazo con base en $x_0$ añadiendo el [[Espacio conexo por caminos|camino]] $f:[0,1] \rightarrow X:f(0)=x_0, \; f(1)=y_0$ al principio y el camino inverso $y_0 \rightarrow x_0$ al final
$$
\alpha'(t)=
\begin{cases}
	& f(3t), \;\; 0 \leq t \leq \frac{1}{3} \\
	& \alpha(3t - 1), \;\; \frac{1}{3} < t \leq \frac{2}{3} \\
	& f^{-1}(3t - 2), \;\; \frac{2}{3} < t \leq 1
\end{cases}
$$