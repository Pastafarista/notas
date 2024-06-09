---
id: 1709035451-ejercicio-1-parcial-1-lgebra
aliases:
  - Ejercicio 1 parcial 2 examen final álgebra
  - Sea el siguiente sistema de ecuaciones
tags:
  - álgebra
---

# Sea el siguiente [[1709024526-sistema-de-ecuaciones-lineales|sistema de ecuaciones]]

$$\begin{cases}
    x + y + z = 2\\
    3x + y + z = 1\\
    x - y + 3z = -3\\
    4x + 2y = \alpha
\end{cases}$$

1. Discutir el sistema en función del parámetro $\alpha$.

Primero vamos a escribir el sistema en [[1709025451-expresin-matricial-de-un-sistema-de-ecuaciones|forma matricial]]

$$A^{*} = \left(\begin{array}{ccc|c}
    1 & 1 & 1 & 2\\
    3 & 1 & 1 & 1\\
    1 & -1 & 3 & -3\\
    4 & 2 & 0 & \alpha
\end{array}\right)$$

Ahora, utilizando el [[1709026069-mtodo-de-gauss-jordan|método de Gauss]] vamos a reducir la [[1709026281-matriz-ampliada|matriz ampliada]] a su [[1709020490-matriz-escalonada|forma escalonada]]

$$\begin{split}
    & \left(\begin{array}{ccc|c}
        1 & 1 & 1 & 2\\
        3 & 1 & 1 & 1\\
        1 & -1 & 3 & -3\\
        4 & 2 & 0 & \alpha
    \end{array}\right) \sim
    \left(\begin{array}{ccc|c}
        1 & 1 & 1 & 2\\
        0 & -2 & -2 & -5\\
        0 & -2 & 2 & -5\\
        0 & -2 & -4 & \alpha - 8
    \end{array}\right) \sim \\
    & \sim
    \left(\begin{array}{ccc|c}
        1 & 1 & 1 & 2\\
        0 & -2 & -2 & -5\\
        0 & 0 & 4 & 0\\
        0 & 0 & -2 & \alpha - 3
    \end{array}\right) \sim 
    \left(\begin{array}{ccc|c}
        1 & 1 & 1 & 2\\
        0 & -2 & -2 & -5\\
        0 & 0 & 4 & 0\\
        0 & 0 & 0 & \alpha - 3
    \end{array}\right)
\end{split}$$

La matriz escalonada que hemos obtenido es [[1708977581-matrices-equivalentes|equivalente]], por lo que tendrá el mismo rango que $A^{*}$, por lo tanto sabemos que si $\alpha \neq 3 \Longleftrightarrow rang(A^*) = 4$ y si $\alpha = 3 \Longleftrightarrow rang(A^*) = 3$

El rango de $A$ siempre es 3, ya que en su [[1709020490-matriz-escalonada|forma escalonada]] no tiene filas nulas.

Entonces, usando el [[1709028207-teorema-de-rouch-frbenius|teorema de Rouché-Fröbenius]] sabemos que el sistema es [[1709028361-sistema-compatible|compatible]] si sólo si el [[1708971315-rango-de-una-matriz|rango]] de $A$ es igual al rango de $A^{*}$, que solo ocurre si $\alpha = 3$. Además en este caso sería [[1709028422-sistema-compatible-determinado|sistema compatible determinado]] ya que el rango es igual al número de incógnitas.

$$\begin{cases}
	\text{si } \alpha = 3 \;\;\; S.C.D.\\
	\text{si } \alpha \neq 3 \;\;\; S.I.
\end{cases}$$

2. Resolver el sistema para los valores de $\alpha$ para los que sea [[1709028361-sistema-compatible|compatible]]

Para $\alpha = 3$ el sistema es:

$$
\begin{cases}
    x + y + z = 2\\
    -2y + -2z = -5\\
    4z = 0\\
\end{cases}
$$

De la tercera ecuación obtenemos que $z = 0$, sustituyendo en la segunda ecuación obtenemos que $y = \frac{5}{2}$, y sustituyendo en la primera ecuación obtenemos que $x = -\frac{1}{2}$

Por lo tanto, la solución del sistema para $\alpha = 3$ es:

$$
\begin{cases}
    x = -\frac{1}{2}\\
    y = \frac{5}{2}\\
    z = 0
\end{cases}
$$
