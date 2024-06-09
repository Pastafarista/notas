---
id: 1710273221-ejercicio-2-examen-parcial-lgebra
aliases:
  - Ejercicio 3 examen parcial álgebra
tags:
  - álgebra
---

# Dado el plano pi

$$
\pi: 2x - y - z + 2 = 0
$$

1. Hallar la [[1710095210-ecuacin-continua-de-la-recta|ecuación continua]] de la [[1710070725-rectas-en-r|recta]] perpendicular a dicho plano y que pasa por el punto $(0,3,1)$

Como el [[1709799641-vector-fijo|vector]] normal del [[1710070957-planos-en-r|plano]] ya nos da una dirección perpendicular a él, podemos construir la recta en forma [[1710094947-ecuacin-vectorial-de-la-recta|vectorial]]:

$$
r = (0,3,1) + \lambda(2,-1,-1), \quad \lambda \in \mathbb{R}
$$

Como nos piden la [[1710095210-ecuacin-continua-de-la-recta|ecuación continua]], primero pasamos a forma [[1710095070-ecuaciones-paramtricas-de-la-recta|paramétrica]] y luego a forma continua:

$$
\begin{split}
    & x = 0 + 2\lambda\\
    & y = 3 - \lambda\\
    & z = 1 - \lambda
\end{split}
$$

Despejamos $\lambda$ de todas las ecuaciones:

$$
\begin{split}
    & \lambda = \frac{x}{2}\\
    & \lambda = 3 - y\\
    & \lambda = 1 - z
\end{split}
$$

Igualamos para obtener la [[1710095210-ecuacin-continua-de-la-recta|ecuación continua]] de la [[1710070725-rectas-en-r|recta]]:

$$
\frac{x}{2} = 3 - y = 1 - z
$$

![[ej3-parcial-álgebra.png]]

2. Hallar la [[1710092173-posicin-relativa-de-una-recta-y-un-plano|posición relativa]] y la [[1710093688-distancia-entre-una-recta-y-un-plano|distancia]] entre el [[1710070957-planos-en-r|plano]] $\pi$ y la [[1710070725-rectas-en-r|recta]]

$$
s \equiv
\begin{cases}
    x = 2 + 2\lambda\\
    y = 1 + 3\lambda\\
    z = \lambda
\end{cases}
$$

Como tenemos la recta en forma [[1710095070-ecuaciones-paramtricas-de-la-recta|paramétrica]] podemos sustituir directamente los valores de $x,y,z$ en el plano:

$$
\begin{split}
    & 2(2 + 2\lambda) - (1 + 3\lambda) - (\lambda) + 2 = 0 \iff\\
    & \iff 4 + 4\lambda - 1 - 3\lambda - \lambda + 2 = 0 \iff\\
    & \iff 4 - 1 + 2 + \lambda(4 - 3 - 1) = 0 \iff\\
    & \iff 5 = 0
\end{split}
$$

No sale que $5 = 0$, esto es porque se trata de un [[1709028539-sistema-incompatible|sistema incompatible]], por lo tanto la recta es paralela al plano.

Esto también se puede ver haciendo el [[1709801827-producto-escalar-de-dos-vectores|producto escalar]] del [[1709799641-vector-fijo|vector]] director de $s$ con el vector normal del plano: 

$$
<(2,3,1),(2,-1,-1)> = 2*2 + 3*(-1) + 1*(-1) = 4 - 3 - 1 = 0
$$

Como vemos, el resultado es $0$, por lo tanto el vector director de la recta es perpendicular al vector normal del plano, lo que significa que la recta es paralela al plano.

Finalmente, para hallar la [[1710093688-distancia-entre-una-recta-y-un-plano|distancia]] entre el [[1710070957-planos-en-r|plano]] y la [[1710070725-rectas-en-r|recta]] escogemos un punto de la recta y calculamos la [[1710093492-distancia-entre-un-punto-y-un-plano|distancia punto-plano]]:

$$
\begin{split}
    & (2,1,0) \in s\\
    & d(P,\pi)=\frac{|Ax_0+By_0+Cz_0+D|}{\sqrt{A^2 +B^{2} + C^{2}}} =\\
    & = \frac{|2\cdot2+(-1)\cdot1+(-1)\cdot0+2|}{\sqrt{2^2 +(-1)^{2} + (-1)^{2}}} =\\
    & = \frac{|4-1+2|}{\sqrt{4+1+1}} = \frac{|5|}{\sqrt{6}} = \frac{5}{\sqrt{6}} \approx 2.04
\end{split}
$$

![[ej2-2-parcial-álgebra.png]]
