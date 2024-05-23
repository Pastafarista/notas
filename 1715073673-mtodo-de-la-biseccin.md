---
id: 1715073673-mtodo-de-la-biseccin
aliases:
  - Método de la bisección
tags:
  - cálculo-numérico
---

# Método de la bisección

Sea $f$ definida y [[Función continua|continua]] en un intervalo [[Conjunto cerrado|cerrado]] y acotado $I_{0}=[a,b]$ y tal que $f(a)\cdot f(b)<0$.

Por el teorema de Bolzano, existe $c \in  (a,b)$ tal que $f(c) = 0$

$$
\begin{split}
    & x_{0} = \frac{a+b}{2}\\
    & a) \quad f(x_{0})=0 \implies x_{0} \text{ ¡Perfecto!}\\
	    & b) \quad f(x_{0}) > 0 \text{ o } f(x_{0}) < 0 \implies f(x_{0})\cdot f(a) < 0 \text{ o } f(x_{0})\cdot f(b) < 0 \implies\\
	    & \implies I_{1} = [a,x_{0}] \text{ o } I_{1} = [x_{0},b]\\
    & \text{Itero el proceso con } I_{1}
\end{split}
$$
