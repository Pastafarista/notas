---
id: 1716905971-ejercicio-8-tema-4-ecuaciones-diferenciales
aliases:
  - Ejercicio 8 tema 4 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resuelve el siguiente sistema de ecuaciones diferenciales:

$$
\begin{cases}
    y_{1}' = -2y_{1} + y_{2}\\
    y_{2}' = -y_{1}
\end{cases}
$$

Sacamos la matriz de coeficientes:

$$
A = \begin{pmatrix}
    -2 & 1\\
    -1 & 0
\end{pmatrix}
$$

Calculamos los autovalores asociados a la matriz de coeficientes:

$$
\begin{split}
    & det(A-\lambda I) = 0 \Longleftrightarrow \\
    & \Longleftrightarrow det\left(\begin{pmatrix}
        -2-\lambda & 1\\
        -1 & -\lambda
    \end{pmatrix}\right) = 0  \implies\\
    & \implies \lambda_{1} = -1 \text{ (doble)}
\end{split}
$$

Calculamos los autovectores asociados a los autovalores:

- Para $\lambda_{1} = -1$:

$$
\begin{split}
    & S_{\lambda = -1} = \left( \begin{array}{cc|c}
        -2 - (-1) & 1 & 0\\
        -1 & -1 & 0
    \end{array}\right) \sim 
    \left( \begin{array}{cc|c}
        -1 & 1 & 0\\
        0 & 0 & 0
    \end{array}\right) = \{(x, x) : x \in \mathbb{R} \}
\end{split}
$$

Como vemos, la matriz no es diagonalizable, por lo tanto calcularemos el bloque de Jordan asociado a $\lambda_{1} = -1$:

$$
\begin{split}
    & E_{1}(\lambda = -1) = \{(x, x) : x \in \mathbb{R} \}\\
    & E_{2}(\lambda = -1) = Ker(A + I)^2 = Ker \begin{pmatrix}
        1 & 1\\
        -1 & 1
    \end{pmatrix}^2 = Ker \begin{pmatrix}
        0 & 0\\
        0 & 0
    \end{pmatrix} = \{(x, y) : x,y \in \mathbb{R}\}
\end{split}
$$

Necesitamos un $v_{2}$ que pertenezca a $E_2(\lambda = -1)$ y que no pertenezca a $E_1(\lambda = -1)$, por lo que tomamos $v_{2}=(1,0)$. Para encontrar $v_{1}$, tomamos $v_{1}=(A-(-1)I)v_{2} = (-1,-1)$.

Por lo tanto, ahora que tenemos nuestros vectores, la solución general del sistema de ecuaciones diferenciales es:

$$ 
\begin{split}
    & Y_{SGEH} =  C_{1}v_{1}e^{-x} + C_{2}(xv_{1} + v_{2})e^{-x} =\\
    & = C_{1}e^{-x}\begin{pmatrix}
        -1\\
        -1
    \end{pmatrix} + C_{2}xe^{-x}\begin{pmatrix}
        -1\\
        -1
    \end{pmatrix} + C_{2}e^{-x}\begin{pmatrix}
        1\\
        0
    \end{pmatrix}
\end{split}
$$

En forma de sistema de ecuaciones, la solución general es:

$$
Y_{SGEH} = \begin{cases}
    y_{1}(x) = -C_{1}e^{-x} + C_{2}(-x+1)e^{-x}\\
    y_{2}(x) = -C_{1}e^{-x} - C_{2}xe^{-x}
\end{cases}
$$
