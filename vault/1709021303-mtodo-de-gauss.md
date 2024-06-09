---
id: 1709021303-mtodo-de-gauss
aliases:
  - Método de Gauss
  - Cálculo de matriz inversa
tags:
  - álgebra
---

# Método de Gauss

Si $A$ es una [[1708972968-matriz-cuadrada|matriz cuadrada]] de orden $n$ [[1708975789-matriz-regular|regular]], $A$ es [[1708977581-matrices-equivalentes|equivalente]] a la [[1708973072-matriz-identidad|matriz identidad]] (es decir, podemos llegar a la matriz identidad a través de [[1708977689-operaciones-elementales|operaciones elementales]] en los elementos de $A$)

## Ejemplo

$$\begin{split}
    & A = 
    \begin{pmatrix}
        1 & 3 & -2\\
        2 & 4 & 0\\
        3 & 5 & -1\\
    \end{pmatrix}\\

    &\\
    
    & \left(\begin{array}{ccc|ccc}
        1 & 3 & -2  & 1 & 0 & 0\\
        2 & 4 & 0 & 0 & 1 & 0\\
        3 & 5 & -1 & 0 & 0 & 1\\
    \end{array}\right) \sim
    \left(\begin{array}{ccc|ccc}
        1 & 3 & -2  & 1 & 0 & 0\\
        0 & -2 & 4 & -2 & 1 & 0\\
        0 & -4 & 5 & -3 & 0 & 1\\
    \end{array}\right) \sim\\ 
    & \left(\begin{array}{ccc|ccc}
        1 & 3 & -2  & 1 & 0 & 0\\
        0 & -2 & 4 & -2 & 1 & 0\\
        0 & 0 & -3 & -1 & 2 & 1\\
    \end{array}\right) \sim

    \left(\begin{array}{ccc|ccc}
        1 & 3 & -2 & 1 & 0 & 0\\
        0 & -6 & 12 & -6 & 3 & 0\\
        0 & 0 & -12 & 4 & -8 & 4\\
    \end{array}\right) \sim\\

    & \left(\begin{array}{ccc|ccc}
        1 & 3 & -2 & 1 & 0 & 0\\
        0 & -6 & 0 & -2 & -5 & 4\\
        0 & 0 & -12 & 4 & -8 & 4\\
    \end{array}\right) \sim

    \left(\begin{array}{ccc|ccc}
        -6 & -18 & 12 & -6 & 0 & 0\\
        0 & -6 & 0 & -2 & -5 & 4\\
        0 & 0 & -12 & 4 & -8 & 4\\
    \end{array}\right)\\

    & \left(\begin{array}{ccc|ccc}
        -6 & -18 & 0 & -2 & -8 & 4\\
        0 & -6 & 0 & -2 & -5 & 4\\
        0 & 0 & -12 & 4 & -8 & 4\\
    \end{array}\right) \sim

    \left(\begin{array}{ccc|ccc}
        -6 & 0 & 0 & 4 & 7 & -8\\
        0 & -6 & 0 & -2 & -5 & 4\\
        0 & 0 & -12 & 4 & -8 & 4\\
    \end{array}\right) \sim\\

   & \left(\begin{array}{ccc|ccc}
        1 & 0 & 0 & -\frac{2}{3} & -\frac{7}{6} & \frac{4}{3}\\
        0 & 1 & 0 & \frac{1}{3} & \frac{5}{6} & -\frac{2}{3}\\
        0 & 0 & 1 & -\frac{1}{3} & \frac{2}{3} & -\frac{1}{3}\\
    \end{array}\right) \implies A^{-1} =
    \begin{pmatrix}
        -\frac{2}{3} & -\frac{7}{6} & \frac{4}{3}\\
        \frac{1}{3} & \frac{5}{6} & -\frac{2}{3}\\
        -\frac{1}{3} & \frac{2}{3} & -\frac{1}{3}\\
    \end{pmatrix}
\end{split}$$
