---
id: 1716824593-ejercicio-1-tema-4-ecuaciones-diferenciales
aliases:
  - Ejercicio 1 tema 4 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Calcula la exponencial de las siguiente matrices:

$$
A = \begin{pmatrix}
    2 & 0 \\
    0 & 3
\end{pmatrix}
\quad
B = \begin{pmatrix}
    2 & 0 \\
    3 & 1
\end{pmatrix}
\quad
C = \begin{pmatrix}
    1 & 2 \\
    0 & 1
\end{pmatrix}
$$

1. Calcula la exponencial de la matriz $A$.

La matriz $A$ es diagonal, por lo que podemos calcular la exponencial de la matriz $A$ como:

$$
e^{Ax} = P e^{Dx} P^{-1} = I e^{Dx} I^{-1} = e^{Dx}
$$

Por lo tanto, calculamos la exponencial de la matriz $A$:

$$
e^{Ax} = e^{Dx} = \begin{pmatrix}
    e^{2x} & 0 \\
    0 & e^{3x}
\end{pmatrix}
$$

2. Calcula la exponencial de la matriz $B$.

Vamos a diagonalizar la matriz $B$ para poder calcular su exponencial. Primero sacamos los valores propios de la matriz $B$:

$$
\begin{split}
    & \det(B - \lambda I) = 0 \iff\\
    & \iff \begin{vmatrix}
        2 - \lambda & 0 \\
        3 & 1 - \lambda
    \end{vmatrix} = (2 - \lambda)(1 - \lambda) = 0 \implies\\
    & \implies \lambda_1 = 2, \quad \lambda_2 = 1
\end{split}
$$

Ahora calculamos los vectores propios de la matriz $B$:

- Para $\lambda_1 = 2$:

$$
\begin{split}
    & S_{\lambda = 2} = \left(\begin{array}{cc|c}
        2-2 & 0 & 0 \\
        3 & 1-2 & 0
    \end{array}\right) = \{(x, 3x) : x \in \mathbb{R}\} \implies\\
    & \implies B_{S_{\lambda = 2}} = \begin{pmatrix}
        1\\
        3
    \end{pmatrix}
\end{split}
$$

- Para $\lambda_2 = 1$:

$$
\begin{split}
    & S_{\lambda = 1} = \left(\begin{array}{cc|c}
        2-1 & 0 & 0 \\
        3 & 1-1 & 0
    \end{array}\right) = \{(0, y) : y \in \mathbb{R}\} \implies\\
    & \implies B_{S_{\lambda = 1}} = \begin{pmatrix}
        0 \\
        1
    \end{pmatrix}
\end{split}
$$

Una vez tenemos los vectores propios podemos construir nuestra matriz de paso $P$:

$$
P = \begin{pmatrix}
	    1 & 0 \\
	    3 & 1
    \end{pmatrix}
$$

También será necesario calcular la [[1708971370-matriz-inversa|matriz inversa]] de $P$:

$$
\begin{split}
    & \left(\begin{array}{cc|cc}
        1 & 0 & 1 & 0 \\
        3 & 1 & 0 & 1
    \end{array}\right) \sim \left(\begin{array}{cc|cc}
        1 & 0 & 1 & 0 \\
        0 & 1 & -3 & 1
    \end{array}\right) \implies\\
    & P^{-1} = \begin{pmatrix}
        1 & 0 \\
        -3 & 1 
    \end{pmatrix}
\end{split}
$$

Ahora ya podemos calcular la exponencial de la matriz $B$:

$$
\begin{split}
    & e^{Bx} = P e^{Dx} P^{-1} = \begin{pmatrix}
        1 & 0 \\
        3 & 1
    \end{pmatrix} \begin{pmatrix}
        e^{2x} & 0 \\
        0 & e^{x}
    \end{pmatrix} \begin{pmatrix}
        1 & 0 \\
        -3 & 1
    \end{pmatrix} =\\
    & = \begin{pmatrix}
        e^{2x} & 0 \\
        3e^{2x} & e^{x}
    \end{pmatrix} \begin{pmatrix}
        1 & 0 \\
        -3 & 1
    \end{pmatrix} = \begin{pmatrix}
        e^{2x} & 0 \\
        3e^{2x}-3e^{x} & e^{x}
    \end{pmatrix}
\end{split}
$$

3. Calcula la exponencial de la matriz $C$.

Vamos a diagonalizar la matriz $C$ para poder calcular su exponencial. Primero sacamos los valores propios de la matriz $C$:

$$
\begin{split}
    & \begin{vmatrix}
        1 - \lambda & 2 \\
        0 & 1 - \lambda
    \end{vmatrix} = (1 - \lambda)^2 = 0 \implies\\
    & \implies \lambda = 1
\end{split}
$$

Calculamos el vector propio de la matriz $C$:

$$
\begin{split}
    & S_{\lambda = 1} = \left(\begin{array}{cc|c}
        1-1 & 2 & 0 \\
        0 & 1-1 & 0
    \end{array}\right) = \{(x, 0) : x \in \mathbb{R}\}
\end{split}
$$

Vemos que la matriz $C$ no es diagonalizable, por lo tanto calculamos la matriz de Jordan asociada a la matriz $C$. Para ello calculamos los dos bloques de Jordan asociados al autovalor $\lambda = 1$:

$$
\begin{split}
    & E_1(\lambda = 1) = (1, 0)\\
    & E_2(\lambda = 1) = Ker((C - I)^2) = Ker\left(\begin{pmatrix}
        0 & 2 \\
        0 & 0
    \end{pmatrix}\right)^2 = Ker(0) = \left(\{(1,0),(0,1)\}\right)
\end{split}
$$

Hacemos nuestro esquema de Jordan:

| $E_1(\lambda = 1)$ | $E_2(\lambda = 1)$ |
| ------------------ | ------------------ |
| 1                  | 2                  |
| $v_{2}$            | $v_{1}$            |

El vector $v_{2}$ será $(1,0)$ y el vector $v_{1}$ será un vector que pertenezca a $E_2$ y que no pertenezca a $E_1$, por lo que tomamos el vector $(0,1)$. La [[1716897460-matriz-de-jordan|matriz de Jordan]] sería:

$$
J = \begin{pmatrix}
    1 & 1 \\
    0 & 1
\end{pmatrix}
$$

Calculamos la exponencial de la matriz $C$:

$$
\begin{split}
    & Y = C_{1}v_{1}e^{x} + C_{2}(xv_{1} + v_{2})e^{x} =\\
    & C_{1}\begin{pmatrix}
        0 \\
        1
    \end{pmatrix}
    e^{x} + C_{2}\left(x\begin{pmatrix}
        1 \\
        0
    \end{pmatrix} + \begin{pmatrix}
        0 \\
        1
    \end{pmatrix}\right)e^{x}
\end{split}
$$

Sacamos el siguiente sistema de ecuaciones:

$$
Y_{SGEH} = \begin{split}
    & \begin{cases}
	    C_2xe^x = 0\\
	    C_1e^x + C_2e^x = 0
    \end{cases}
\end{split}
$$

Por lo tanto nuestra exponencial, será:

$$
e^{Cx} = \begin{pmatrix}
    x e^{x}  & 0\\
    e^{x}  & e^{x} 
\end{pmatrix}
$$
