---
id: 1709040880-ejercicio-6-examen-parcial-lgebra
aliases:
  - Ejercicio 6 examen parcial álgebra
  - Hallar la matriz $X$ que cumple la ecuación $AX - B = A$, siendo
tags:
  - álgebra
---

# Ejercicio 6 examen parcial álgebra

Hallar la matriz $X$ que cumple la ecuación $AX - B = A$, siendo

$$A = \begin{pmatrix}
    2 & 1\\
    0 & 1
\end{pmatrix} \text{ y } B =
\begin{pmatrix}
    3 & 3\\
    1 & 1
\end{pmatrix}$$

Vamos a resolver la [[1709025451-expresin-matricial-de-un-sistema-de-ecuaciones|ecuación matricial]]:

$$AX - B = A \Longleftrightarrow AX = A + B$$

Primeros vamos a calcular la [[1708971370-matriz-inversa|inversa]] de $A$ con el [[1709021303-mtodo-de-gauss|método de Gauss]]

$$\begin{split}
    & \left(\begin{array}{cc|cc}
        2 & 1 & 1 & 0\\
        0 & 1 & 0 & 1
    \end{array}\right) \sim
    \left(\begin{array}{cc|cc}
        2 & 0 & 1 & -1\\
        0 & 1 & 0 & 1
    \end{array}\right) \sim\\
    & \left(\begin{array}{cc|cc}
        1 & 0 & \frac{1}{2} & -\frac{1}{2}\\
        0 & 1 & 0 & 1
    \end{array}\right) \implies A^{-1} = \begin{pmatrix}
        \frac{1}{2} & -\frac{1}{2}\\
        0 & 1
    \end{pmatrix}
\end{split}$$

Ahora con la inversa de $A$ vamos a resolver la ecuación:

$$AX = A + B \Longleftrightarrow A^{-1}AX = A^{-1}(A + B) \Longleftrightarrow IX = I + A^{-1}B$$

Calculamos $I + A^{-1}B$

$$\begin{split}
    & I + A^{-1}B = \begin{pmatrix}
        1 & 0\\
        0 & 1
    \end{pmatrix} + \begin{pmatrix}
        \frac{1}{2} & -\frac{1}{2}\\
        0 & 1
    \end{pmatrix}\begin{pmatrix}
        3 & 3\\
        1 & 1
    \end{pmatrix} =\\
    & \begin{pmatrix}
        1 & 0\\
        0 & 1
    \end{pmatrix} + \begin{pmatrix}
        \frac{3}{2} - \frac{1}{2} & \frac{3}{2} - \frac{1}{2}\\
        0 + 1 & 0 + 1
    \end{pmatrix} = \begin{pmatrix}
        2 & 1\\
        1 & 2
    \end{pmatrix}
\end{split}$$

Por lo que la matriz $X$ que cumple la ecuación es:

$$\begin{split}
    & IX = X =
    \begin{pmatrix}
        2 & 1\\
        1 & 2
    \end{pmatrix}
\end{split}$$

