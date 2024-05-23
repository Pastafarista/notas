---
id: 1709026069-mtodo-de-gauss-jordan
aliases:
  - Método de Gauss-Jordan
tags: []
---

# Método de Gauss-Jordan

- Consiste en transformar la [[1709026281-matriz-ampliada|matriz ampliada]] del [[1709024526-sistema-de-ecuaciones-lineales|sistema de ecuaciones]] a una [[1709020490-matriz-escalonada|matriz escalonada]] mediante [[1708977689-operaciones-elementales|operaciones elementales]].

## Ejemplo

Dado el sistema:

$$\begin{cases}
    x + y + 2z = 9\\
    3x + 6y - 5z = 0\\
    2x + 4y - 3z = 1
\end{cases}$$

Pasamos el sistema a su [[1709025451-expresin-matricial-de-un-sistema-de-ecuaciones|forma matricial]] y aplicamos el método de Gauss-Jordan:

$$\begin{split}
    & \left(\begin{array}{ccc|c}
        1 & 1 & 2 & 9\\
        3 & 6 & -5 & 0\\
        2 & 4 & -3 & 1
    \end{array}\right) \sim 
    \left(\begin{array}{ccc|c}
        1 & 1 & 2 & 9\\
        0 & 3 & -11 & -27\\
        0 & 2 & -7 & -17
    \end{array}\right) \sim\\
    & \left(\begin{array}{ccc|c}
        1 & 1 & 2 & 9\\
        0 & 6 & -22 & -54\\
        0 & -6 & 21 & 51
    \end{array}\right) \sim
    \left(\begin{array}{ccc|c}
        1 & 1 & 2 & 9\\
        0 & 6 & -22 & -54\\
        0 & 0 & -1 & -3
    \end{array}\right)\\
\end{split}$$

Ahora tenemos la [[1709020490-matriz-escalonada|matriz escalonada]], por lo que podemos despejar las incógnitas:

$$\begin{split}
    & \begin{cases}
        x + y + 2z = 9\\
        6y - 22z = -54\\
        -z = -3
    \end{cases} \Rightarrow
    \begin{cases}
        x + y + 2z = 9\\
        y = 2\\
        z = 3
    \end{cases}
\end{split}$$

Por lo tanto, la solución del sistema es:

$$\begin{cases}
    x = 1\\
    y = 2\\
    z = 3
\end{cases}$$
