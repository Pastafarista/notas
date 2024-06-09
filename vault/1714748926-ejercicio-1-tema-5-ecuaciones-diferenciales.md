---
id: 1714748926-ejercicio-1-tema-5-ecuaciones-diferenciales
aliases:
  - Ejercicio 1 tema 5 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Determina los [[1714749330-punto-crtico-de-un-sistema-autnomo|puntos críticos]] del siguiente [[1714749015-sistema-de-ecuaciones-difereciales-autnomo#sistema-de-ecuaciones-difereciales-autnomo|sistema autónomo]]

$$
\begin{cases}
    & x' = x(100 - x - y) \\
    & y' = 5y(60 - y - 0.2x)
\end{cases}
$$

Hay que resolver el sistema de ecuaciones:

$$
\begin{cases}
    & x(100 - x - y) = 0 \\
    & 5y(60 - y - 0.2x) = 0
\end{cases}
$$

La solución $y=0,x=0$ resulta obvia. Para encontrar el resto de soluciones, se resuelven las ecuaciones:

$$
\begin{cases}
    & 100 - x - y = 0 \\
    & 60 - y - 0.2x = 0
\end{cases} \implies \begin{cases}
    & x = 50\\
    & y = 50
\end{cases}
$$

También hay que considerar los puntos en las que una de las incógnitas se anula:

$$
\begin{cases}
    & x = 0 \\
    & 60 - y = 0
\end{cases} \implies y = 60
$$

$$
\begin{cases}
    & 100 - x = 0 \\
    & y = 0
\end{cases} \implies x = 100
$$

Por lo tanto, los puntos críticos son $(0,0)$, $(50,50)$, $(0,60)$ y $(100,0)$.

