---
id: 1707132005-ejercicico-2-ecuaciones-diferenciales-primer-orden
aliases:
  - Ejercicico 2 ecuaciones diferenciales primer orden
  - Resuelve las siguientes ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resuelve las siguientes [[1706869334-ecuacin-diferencial|ecuaciones diferenciales]]

1. $y' = cos(3x) + 5$

$$
\begin{split}
   & \frac{dy}{dx} = \cos(3x) + 5 \implies \int dy = \int (\cos(3x) + 5) d x \implies \\
   & \implies y = \frac{1}{3} \sin(3x) + 5x + C
\end{split}
$$

2. $\frac{1}{x}y' = e^x$

$$
\begin{split}
    & \frac{1}{x} \frac{d y}{d x} = e^x \implies \int d y = \int x e^x d x \implies \\
    & \implies \begin{cases} & u = x \implies d u = d x \\ & dv = e^x dx \implies v = e^x \end{cases} \implies \\
    & \implies y = x e^x - \int e^x d x \implies y = x e^x - e^x + C \implies y = e^x(x-1) + C
\end{split}
$$
