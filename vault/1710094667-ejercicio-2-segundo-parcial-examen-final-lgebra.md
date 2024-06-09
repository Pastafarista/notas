---
id: 1710094667-ejercicio-2-segundo-parcial-examen-final-lgebra
aliases:
  - Ejercicio 2 segundo parcial examen final álgebra
tags:
  - álgebra
---

# Establecer la posición relativa entre las rectas r y s. Calcular el punto o puntos de corte si es posible.

$$
\begin{split}
    & r:
    \begin{cases}
        & 3x + 2y + z + 4 = 0\\
        & 4x + 2z + 2 = 0
    \end{cases}\\

    & s:
    \begin{cases}
        & x = 4\lambda + 3\\
        & y = 2\lambda + 1\\
        & z = -3\lambda - 2
    \end{cases}

\end{split}
$$

Como tenemos una [[1710070725-rectas-en-r|recta]] en forma de [[1710095265-recta-como-interseccin-de-planos|intersección de dos planos]] y otra en forma [[1710095070-ecuaciones-paramtricas-de-la-recta|paramétrica]], podemos sustituir $x,y \text{ y } z$ de la recta $s$ en los planos de la recta $r$:

$$
\begin{split}
    & 3(4\lambda + 3) + 2(2\lambda + 1) + (-3\lambda - 2) + 4 = 0\\
    & 4(4\lambda + 3) + 2(-3\lambda - 2) + 2 = 0
\end{split}
$$

Resolviendo el sistema de ecuaciones:

$$
\begin{split}
    & 3(4\lambda + 3) + 2(2\lambda + 1) + (-3\lambda - 2) + 4 = 0 \iff\\
    & \iff 12\lambda + 9 + 4\lambda + 2 - 3\lambda - 2 + 4 = 0 \iff\\
    & \iff 13\lambda + 13 = 0 \iff \lambda = -1\\
    & 4(4\lambda + 3) + 2(-3\lambda - 2) + 2 = 0 \iff\\
    & \iff 16\lambda + 12 - 6\lambda - 4 + 2 = 0 \iff\\
    & \iff 10\lambda + 10 = 0 \iff \lambda = -1
\end{split}
$$

Ahora que tenemos el valor de $\lambda$, podemos sustituirlo en las ecuaciones paramétricas de la recta $s$:

$$
\begin{split}
    & x = 4(-1) + 3 = -1\\
    & y = 2(-1) + 1 = -1\\
    & z = -3(-1) - 2 = 1
\end{split}
$$

Por lo tanto, las rectas $r$ y $s$ se cortan en el punto $P(-1,-1,1)$.

## Forma alternativa

Otra forma de resolver el ejercicio es pasar la recta $s$ a forma de [[1710095265-recta-como-interseccin-de-planos|intersección de planos]] y resolver el sistema de ecuaciones resultante.

Para pasar la recta $s$ a forma de intersección de planos, primero deberemos pasarla a forma [[1710095210-ecuacin-continua-de-la-recta|continua]]. Para ello, despejamos $\lambda$ de las ecuaciones paramétricas:

$$
\begin{split}
    & x = 4\lambda + 3 \iff \lambda = \frac{x - 3}{4}\\
    & y = 2\lambda + 1 \iff \lambda = \frac{y - 1}{2}\\
    & z = -3\lambda - 2 \iff \lambda = \frac{z + 2}{-3}
\end{split}
$$

Igualamos las ecuaciones de $\lambda$:

$$
\frac{x - 3}{4} = \frac{y - 1}{2} = \frac{z + 2}{-3}
$$

Una vez que tenemos la recta $s$ en forma continua, podemos construir los planos que la contienen.

$$
\begin{split}
    & \frac{x - 3}{4} = \frac{y - 1}{2} \iff 2x - 6 = 4y - 4 \iff 2x - 4y - 2 = 0\\
    & \frac{x-3}{4} = \frac{z+2}{-3} \iff -3x + 9 = 4z + 8 \iff 3x+4z-1=0
\end{split}
$$

Por lo tanto, la recta $s$ se puede expresar como:

$$
s: 
\begin{cases}
    & 2x - 4y - 2 = 0\\
    & 3x + 4z - 1 = 0
\end{cases}
$$

Ahora que tenemos los 4 planos nuestra matriz $M$ es:

$$
M = \begin{pmatrix}
    2 & -4 & 0\\
    3 & 0 & 4\\
    3 & 2 & 1\\
    4 & 0 & 2
\end{pmatrix}
$$

Y la matriz ampliada $M^{*}$ es:

$$
M^{*} = \begin{pmatrix}
    2 & -4 & 0 & 2\\
    3 & 0 & 4 & 1\\
    3 & 2 & 1 & -4\\
    4 & 0 & 2 & -2
\end{pmatrix}
$$

Escalonamos la matriz $M^{*}$:

$$
\begin{split}
	& \begin{pmatrix}
	    2 & -4 & 0 & 2\\
	    3 & 0 & 4 & 1\\
	    3 & 2 & 1 & -4\\
	    4 & 0 & 2 & -2
	\end{pmatrix}

	\xrightarrow{F_2 - \frac{3}{2}F_1}
	\begin{pmatrix}
	    2 & -4 & 0 & 2\\
	    0 & 6 & 4 & -2\\
	    3 & 2 & 1 & -4\\
	    4 & 0 & 2 & -2
	\end{pmatrix}
	
	\xrightarrow{F_3 - \frac{3}{2}F_1}
	\begin{pmatrix}
	    2 & -4 & 0 & 2\\
	    0 & 6 & 4 & -2\\
	    0 & 8 & 1 & -7\\
	    4 & 0 & 2 & -2
	\end{pmatrix}\\

	& \xrightarrow{F_4 - 2F_1}
	\begin{pmatrix}
	    2 & -4 & 0 & 2\\
	    0 & 6 & 4 & -2\\
	    0 & 8 & 1 & -7\\
	    0 & 8 & 2 & -6
	\end{pmatrix}
	
	\xrightarrow{F_3 - \frac{4}{3}F_2}
	\begin{pmatrix}
	    2 & -4 & 0 & 2\\
	    0 & 6 & 4 & -2\\
	    0 & 0 & -\frac{13}{3} & -\frac{13}{3}\\
	    0 & 8 & 2 & -6
	\end{pmatrix}\\
	
	& \xrightarrow{F_4 - \frac{4}{3}F_2}
	\begin{pmatrix}
	    2 & -4 & 0 & 2\\
	    0 & 6 & 4 & -2\\
	    0 & 0 & -\frac{13}{3} & -\frac{13}{3}\\
	    0 & 0 & -\frac{10}{3} & -\frac{10}{3}
	\end{pmatrix}
	
	\xrightarrow{F_4 - \frac{10}{13}F_3}
	\begin{pmatrix}
	    2 & -4 & 0 & 2\\
	    0 & 6 & 4 & -2\\
	    0 & 0 & -\frac{13}{3} & -\frac{13}{3}\\
	    0 & 0 & 0 & 0
	\end{pmatrix}
\end{split}
$$

Como vemos $rang(M)=rang(M^{*})=3$, utilizando [[1710092108-posicin-relativa-de-dos-rectas|los apuntes]], vemos que las rectas se cortan en un punto.

Para ver cual es el punto de corte, simplemente resolvemos el sistema escalonado:

$$
\begin{split}
    & -\frac{13}{3}z = -\frac{13}{3} \iff z = 1\\
    & 6y + 4z = -2 \iff 6y + 4 = -2 \iff 6y = -6 \iff y = -1\\
    & 2x - 4y = 2 \iff 2x + 4 = 2 \iff 2x = -2 \iff x = -1
\end{split}
$$

Por lo tanto, las rectas $r$ y $s$ se cortan en el punto $P(-1,-1,1)$.

![[ej2-examen-final-parcial-2.png]]
