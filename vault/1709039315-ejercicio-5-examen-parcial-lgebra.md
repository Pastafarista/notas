---
id: 1709039315-ejercicio-5-examen-parcial-lgebra
aliases:
  - Ejercicio 5 examen parcial álgebra
  - Dada la matriz
tags:
  - álgebra
---

# Dada la matriz

$$A = \begin{pmatrix}
    0 & 1 & 0\\
    1 & 0 & 0\\
    0 & 1 & 0\\
\end{pmatrix}$$

1. Calcular $A^{23}$

Comprobemos que ocurre cuando [[1708972369-producto-de-matrices|elevamos]] $A$ al cuadrado:

$$A^2 = A \cdot A = \begin{pmatrix}
    0 & 1 & 0\\
    1 & 0 & 0\\
    0 & 1 & 0\\
\end{pmatrix} \cdot
\begin{pmatrix}
    0 & 1 & 0\\
    1 & 0 & 0\\
    0 & 1 & 0\\
\end{pmatrix} =
\begin{pmatrix}
    1 & 0 & 0\\
    0 & 1 & 0\\
    1 & 0 & 0\\
\end{pmatrix}$$

Sigamos con la siguiente potencia, $A^3$

$$A^3 = A \cdot A^2 = \begin{pmatrix}
    0 & 1 & 0\\
    1 & 0 & 0\\
    0 & 1 & 0\\
\end{pmatrix} \cdot
\begin{pmatrix}
    1 & 0 & 0\\
    0 & 1 & 0\\
    1 & 0 & 0\\
\end{pmatrix} =
\begin{pmatrix}
    0 & 1 & 0\\
    1 & 0 & 0\\
    0 & 1 & 0\\
\end{pmatrix}$$

Como vemos, $A^3 = A$, por lo que cualquier potencia impar será $A$ y cualquier potencia par será $A^2$. Por lo tanto, $A^{23} = A^3 = A$

2. Calcular para qué valores de $\alpha$ la [[1708971486-matriz|matriz]] $B = A + \alpha I$ tiene [[1708971315-rango-de-una-matriz|rango]] máximo.

Primero vamos a calcular $B$:

$$\begin{split}
    & B = A + \alpha I = \begin{pmatrix}
        0 & 1 & 0\\
        1 & 0 & 0\\
        0 & 1 & 0\\
    \end{pmatrix} + \alpha \begin{pmatrix}
        1 & 0 & 0\\
        0 & 1 & 0\\
        0 & 0 & 1\\
    \end{pmatrix} =\\
    & = \begin{pmatrix}
        1 + \alpha & 1 & 0\\
        1 & 1 + \alpha & 0\\
        0 & 1 & 1 + \alpha\\
\end{pmatrix}
\end{split}$$

Sabemos que el rango de $B$ será máximo si el [[1708976016-determinante|determinante]] de $B$ es distinto de 0.

$$\begin{split}
    & \det(B) = \begin{vmatrix}
        1 + \alpha & 1 & 0\\
        1 & 1 + \alpha & 0\\
        0 & 1 & 1 + \alpha\\
    \end{vmatrix} =\\
    & = (1 + \alpha) \begin{vmatrix}
        1 + \alpha & 1\\
        1 & 1 + \alpha\\
    \end{vmatrix} = (1 + \alpha) ((1 + \alpha)^2 - 1) =\\
    &(1 + \alpha)((1 + \alpha) - 1)((1 + \alpha) + 1) = (1 + \alpha)\alpha(\alpha + 2)
\end{split}$$

Entonces tenemos que $det(B) = 0$ si $\alpha \in \{-2,-1,0\}$, por lo que el [[1708971315-rango-de-una-matriz|rango]] será máximo para $x \in \mathbb{R} \setminus \{-2,-1,0\}$
