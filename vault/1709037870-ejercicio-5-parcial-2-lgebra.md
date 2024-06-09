---
id: 1709037870-ejercicio-5-parcial-2-lgebra
aliases:
  - Ejercicio 5 parcial 1 examen final álgebra
  - Dada la matriz
tags: []
---

# Dada la matriz

$$A = \begin{pmatrix}
    1 & 2 & 0\\
    0 & -1 & 0\\
    0 & 0 & 1\\
\end{pmatrix}$$

1. Calcular $A^{-101}$

Primero vamos a calcular la [[1708971370-matriz-inversa|matriz inversa]] de $A$, para ello utilizaremos el [[1709021303-mtodo-de-gauss|método de Gauss]]

$$\begin{split}
    & \left(\begin{array}{ccc|ccc}
        1 & 2 & 0 & 1 & 0 & 0\\
        0 & -1 & 0 & 0 & 1 & 0\\
        0 & 0 & 1 & 0 & 0 & 1
    \end{array}\right) \sim
    \left(\begin{array}{ccc|ccc}
        1 & 0 & 0 & 1 & 2 & 0\\
        0 & 1 & 0 & 0 & -1 & 0\\
        0 & 0 & 1 & 0 & 0 & 1
    \end{array}\right)
\end{split}$$

Vemos que $A^{-1} = A$, ahora vamos a ver que ocurre cuando [[1708972369-producto-de-matrices|elevamos]] $A$ al cuadrado:

$$A^2 = A \cdot A = \begin{pmatrix}
    1 & 2 & 0\\
    0 & -1 & 0\\
    0 & 0 & 1\\
\end{pmatrix} \cdot
\begin{pmatrix}
    1 & 2 & 0\\
    0 & -1 & 0\\
    0 & 0 & 1\\
\end{pmatrix} =
\begin{pmatrix}
    1 & 0 & 0\\
    0 & 1 & 0\\
    0 & 0 & 1\\
\end{pmatrix} = I$$


Como nos da la [[1708973072-matriz-identidad|matriz identidad]] ya sabemos que cualquier potencia par será la identidad y cualquier potencia impar será $A$, por lo que $A^{101} = A$

Ahora como $A = A^{-1}$, entonces $A^{-101} = A^{101} = A$

2. Hallar la [[1708971486-matriz|matriz]] $X$ tal que $AX - B = B$, siendo $$B =
\begin{pmatrix}
    -1\\
    2\\
    1
\end{pmatrix}$$

Vamos a resolver la [[1709025451-expresin-matricial-de-un-sistema-de-ecuaciones|ecuación matricial]]

$$AX - B = B \Longleftrightarrow AX = 2B$$

$$\begin{split}
    & \begin{pmatrix}
        1 & 2 & 0\\
        0 & -1 & 0\\
        0 & 0 & 1\\
    \end{pmatrix} \cdot \begin{pmatrix}
        x_1\\
        x_2\\
        x_3
    \end{pmatrix} = 2 \cdot \begin{pmatrix}
        -1\\
        2\\
        1
    \end{pmatrix} \Longleftrightarrow\\
    & \begin{pmatrix}
        x_1 + 2x_2\\
        -x_2\\
        x_3
    \end{pmatrix} = \begin{pmatrix}
        -2\\
        4\\
        2
    \end{pmatrix} \implies \begin{cases}
        x_1 + 2x_2 = -2\\
        -x_2 = 4\\
        x_3 = 2
    \end{cases} \implies \\
    & \implies \begin{cases}
        x_1 = -10\\
        x_2 = -4\\
        x_3 = 2
    \end{cases}
    \implies X = \begin{pmatrix}
        -10\\
        -4\\
        2
    \end{pmatrix}
\end{split}$$

