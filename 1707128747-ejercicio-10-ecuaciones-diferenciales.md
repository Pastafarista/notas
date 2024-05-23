---
id: 1707128747-ejercicio-10-ecuaciones-diferenciales
aliases:
  - Ejercicio 10 ecuaciones diferenciales
  - Sabiendo que la solución general de la ecuación diferencial $x^2 y' sen(y) = 1$ está dada por la relación $cos(y)=\frac{1]{x} + C$, caclula la solución particular que tiende al valor $\frac{\pi}{2}$ cuando $x$ tiende al infinito.
  - Sabiendo que la solución general de la ecuación diferencial $x^2 y' sen(y) = 1$ está dada por la relación $cos(y)=\frac{1]{x} + C$, calcula la solución particular que tiende al valor $\frac{\pi}{2}$ cuando $x$ tiende al infinito.
tags:
  - ecuaciones-diferenciales
---

# Sabiendo que la [[1707058998-solucin-de-una-ecuacin-diferencial-ordinaria|solución general]] de la [[1706869334-ecuacin-diferencial|ecuación diferencial]] $x^2 y' sen(y) = 1$ está dada por la relación $cos(y)=\frac{1}{x} + C$, calcula la solución particular que tiende al valor $\frac{\pi}{2}$ cuando $x$ tiende al infinito.

$$
\begin{split}
    & x^2 y' sen(y) = 1\\
    & \text{S.G.: } cos(y) = \frac{1}{x} + C \implies -y' sen(y) = -\frac{1}{x^2} \implies \\
    & \implies y' sen(y) = \frac{1}{x^2} \implies x^2 y' sen(y) = 1\\
    & cos(y) = \frac{1}{x} + C \implies cos(\frac{\pi}{2}) = \frac{1}{\infty} + C \implies 0 = 0 + C \implies C = 0 \implies\\
    & \implies cos(y) = \frac{1}{x} \implies y = arccos(\frac{1}{x}) \implies \lim_{x \rightarrow \infty} y = \lim_{x \rightarrow \infty} arccos(\frac{1}{x} + C) = \frac{\pi}{2} \implies C = 0\\
\end{split}
$$
