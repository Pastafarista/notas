---
id: 1713122391-laboratorio-5-clculo-numrico
aliases:
  - Laboratorio 5 cálculo numérico
  - Laboratorio 5
tags:
  - cálculo-numérico
---

# Laboratorio 5

### Problema 1: Interpolación de Lagrange

Dadas las parejas de valores $(x, y)$: $(-1, -1), (2, 11), (-2, -9), (1, 3)$:

1. Halle el [[1709641715-polinomio-interpolador-de-lagrange|polinomio interpolador de Lagrange]] por [[1713020438-polinomio-de-lagrange-por-coeficientes-indeterminados|coeficientes indeterminados]].

- Utilizando que $P(x_i)=f(x_i$

$$
\begin{cases}
    a_{0} + a_{1}(-1) + a_{2}(-1)^{2} + a_{3}(-1)^{3} = -1\\
    a_{0} + a_{1}(2) + a_{2}(2)^{2} + a_{3}(2)^{3} = 11\\
    a_{0} + a_{1}(-2) + a_{2}(-2)^{2} + a_{3}(-2)^{3} = -9\\
    a_{0} + a_{1}(1) + a_{2}(1)^{2} + a_{3}(1)^{3} = 3
\end{cases}
$$

- De este sistema sacamos la matriz de Vandermonde

$$
\begin{split}
    & \left(\begin{array}{cccc|c}
        1 & -1 & 1 & -1 & -1\\
        1 & 2 & 4 & 8 & 11\\
        1 & -2 & 4 & -8 & -9\\
        1 & 1 & 1 & 1 & 3
    \end{array}\right) \sim 
    \left(\begin{array}{cccc|c}
        1 & -1 & 1 & -1 & -1\\
        0 & 3 & 3 & 9 & 12\\
        0 & -1 & 3 & -7 & -8\\
        0 & 2 & 0 & 2 & 4
    \end{array}\right) \sim\\
    & \left(\begin{array}{cccc|c}
        1 & -1 & 1 & -1 & -1\\
        0 & -1 & 3 & -7 & -8\\
        0 & 3 & 3 & 9 & 12\\
        0 & 2 & 0 & 2 & 4
    \end{array}\right) \sim
    \left(\begin{array}{cccc|c}
        1 & -1 & 1 & -1 & -1\\
        0 & -1 & 3 & -7 & -8\\
        0 & 0 & 12 & -12 & -12\\
        0 & 0 & 6 & -12 & -12
    \end{array}\right) \sim\\
    & \left(\begin{array}{cccc|c}
        1 & -1 & 1 & -1 & -1\\
        0 & -1 & 3 & -7 & -8\\
        0 & 0 & 1 & -1 & -1\\
        0 & 0 & 1 & -2 & -2
    \end{array}\right) \sim
    \left(\begin{array}{cccc|c}
        1 & -1 & 1 & -1 & -1\\
        0 & -1 & 3 & -7 & -8\\
        0 & 0 & 1 & -1 & -1\\
        0 & 0 & 0 & -1 & -1
    \end{array}\right)
\end{split}
$$

- Una vez tenemos la matriz escalonada, podemos despejar los coeficientes

$$
\begin{split}
    & -a_{3} = -1 \Rightarrow a_{3} = 1\\
    & a_{2} - a_{3} = -1 \Rightarrow a_{2} = 0\\
    & -a_{1} + 3a_{2} - 7a_{3} = -8 \implies a_{1} = 1\\
    & a_{0} - a_{1} + a_{2} - a_{3} = -1 \implies a_{0} = 1
\end{split}
$$

- Por lo tanto, el polinomio interpolador de Lagrange por coeficientes indeterminados es:

$$
P(x) =  x^3 + x + 1
$$

2. Halle el polinomio interpolador de Lagrange en [[1713020577-polinomio-de-lagrange-por-forma-de-lagrange|forma de Lagrange]] (NO lo reexprese en potencias de $x$).

- Primero vamos a calcular los elementos de la base de Lagrange:

$$
\begin{split}
    & l_{0}(x) = \frac{(x-2)(x+2)(x-1)}{(-1-2)(-1+2)(-1-1)} = \frac{(x-2)(x+2)(x-1)}{6}\\
    & l_{1}(x) = \frac{(x+1)(x+2)(x-1)}{(2+1)(2+2)(2-1)} = \frac{(x+1)(x+2)(x-1)}{12}\\
    & l_{2}(x) = \frac{(x+1)(x-2)(x-1)}{(-2+1)(-2-2)(-2-1)} = \frac{(x+1)(x-2)(x-1)}{-12}\\
    & l_{3}(x) = \frac{(x+1)(x+2)(x-2)}{(1+1)(1+2)(1-2)} = \frac{(x+1)(x+2)(x-2)}{-6}
\end{split}
$$

- Entonces, el polinomio interpolador de Lagrange en forma de Lagrange es:

$$
\begin{split}
	& P(x) = f(-1)l_{0}(x) + f(2)l_{1}(x) + f(-2)l_{2}(x) + f(1)l_{3}(x) =\\
	& = -1 \cdot \frac{(x-2)(x+2)(x-1)}{6} + 11 \cdot \frac{(x+1)(x+2)(x-1)}{12} -\\
	& 9 \cdot \frac{(x+1)(x-2)(x-1)}{-12} + 3 \cdot \frac{(x+1)(x+2)(x-2)}{-6} \iff\\
    & P(x) = -\frac{(x-2)(x+2)(x-1)}{6} + \frac{11(x+1)(x+2)(x-1)}{12} +\\
    & \frac{3(x+1)(x-2)(x-1)}{4} - \frac{(x+1)(x+2)(x-2)}{2}
\end{split}
$$

3. Halle el polinomio interpolador de Lagrange en forma de Newton, tomando las abscisas en el orden en el que aparecen más arriba (NO lo reexprese en potencias de $x$).

- Vamos a calcular los coeficientes de Newton mediante la tabla de coeficientes divididos:

$$
\begin{split}
	& \begin{array}{|c|c|c|c|c|}
		\hline
		x_{0} & f[x_{0}]\\
		\hline
		x_{1} & f[x_{1}] & f[x_{0}, x_{1}]\\
		\hline
		x_{2} & f[x_{2}] & f[x_{1}, x_{2}] & f[x_{0}, x_{1}, x_{2}]\\
		\hline
		x_{3} & f[x_{3}] & f[x_{2}, x_{3}] & f[x_{1}, x_{2}, x_{3}] & f[x_{0}, x_{1}, x_{2}, x_{3}]\\
		\hline
	\end{array}\\
	&\\
	& \text{Sustituyendo:} \\
	&\\
	& \begin{array}{|c|c|c|c|c|}
		\hline
		-1 & f[-1]\\
		\hline
		2 & f[2] & f[-1, 2]\\
		\hline
		-2 & f[-2] & f[2, -2] & f[-1, 2, -2]\\
		\hline
        1 & f[1] & f[-2, 1] & f[2, -2, 1] & f[-1, 2, -2, 1]\\
		\hline
	\end{array}
\end{split}
$$

- Calculamos los coeficientes:

$$
\begin{split}
    & f[-1] = -1, f[2] = 11, f[-2] = -9, f[1] = 3\\
    & f[-1, 2] = \frac{f[2] - f[-1]}{2-(-1)} = \frac{11 - (-1)}{2+1} = 4\\
    & f[2, -2] = \frac{f[-2] - f[2]}{-2-2} = \frac{-9 - 11}{-2-2} = 5\\
    & f[-2, 1] = \frac{f[1] - f[-2]}{1-(-2)} = \frac{3 - (-9)}{1+2} = 4\\
    & f[-1, 2, -2] = \frac{f[2, -2] - f[-1, 2]}{-2-(-1)} = \frac{5 - 4}{-2+1} = -1\\
    & f[2, -2, 1] = \frac{f[-2, 1] - f[2, -2]}{1-2} = \frac{4 - 5}{1-2} = 1\\
    & f[-1, 2, -2, 1] = \frac{f[2, -2, 1] - f[-1, 2, -2]}{1-(-1)} = \frac{1 - (-1)}{1+1} = 1
\end{split}
$$

- Entonces, el polinomio interpolador de Lagrange en forma de Newton es:

$$
\begin{split}
    & P(x) = f[-1] + f[-1, 2](x+1) + f[-1, 2, -2](x+1)(x-2) +\\
    & f[-1, 2, -2, 1](x+1)(x-2)(x+2) \iff\\
    & P(x) = -1 + 4(x+1) - (x+1)(x-2) + (x+1)(x-2)(x+2)
\end{split}
$$

4. Halle el polinomio interpolador de Lagrange en forma de Newton, tomando las abscisas en el orden natural $-2,-1,1,2$ (NO lo reexprese en potencias de $x$).

- Vamos a calcular los coeficientes de Newton mediante la tabla de coeficientes divididos:

$$
\begin{split}
    & \begin{array}{|c|c|c|c|c|}
        \hline
        x_{0} & f[x_{0}]\\
        \hline
        x_{1} & f[x_{1}] & f[x_{0}, x_{1}]\\
        \hline
        x_{2} & f[x_{2}] & f[x_{1}, x_{2}] & f[x_{0}, x_{1}, x_{2}]\\
        \hline
        x_{3} & f[x_{3}] & f[x_{2}, x_{3}] & f[x_{1}, x_{2}, x_{3}] & f[x_{0}, x_{1}, x_{2}, x_{3}]\\
        \hline
    \end{array}\\
    &\\
    & \text{Sustituyendo:} \\
    &\\
    & \begin{array}{|c|c|c|c|c|}
        \hline
        -2 & f[-2]\\
        \hline
        -1 & f[-1] & f[-2, -1]\\
        \hline
        1 & f[1] & f[-1, 1] & f[-2, -1, 1]\\
        \hline
        2 & f[2] & f[1, 2] & f[-1, 1, 2] & f[-2, -1, 1, 2]\\
        \hline
    \end{array}
\end{split}
$$

- Algunos coeficientes ya los conocemos, por lo que solo calculamos los que faltan:

$$
\begin{split}
    & f[-2, -1] = \frac{f[-1] - f[-2]}{-1-(-2)} = \frac{-1 - (-9)}{-1+2} = 8\\
    & f[-1, 1] = \frac{f[1] - f[-1]}{1-(-1)} = \frac{3 - (-1)}{1+1} = 2\\
    & f[1, 2] = \frac{f[2] - f[1]}{2-1} = \frac{11 - 3}{2-1} = 8\\
    & f[-1, 1, 2] = \frac{f[1, 2] - f[-1, 1]}{2-(-1)} = \frac{8 - 2}{2+1} = 2\\
    & f[-2, -1, 1] = \frac{f[-1, 1] - f[-2, -1]}{1-(-2)} = \frac{2 - 8}{1+2} = -2\\
\end{split}
$$

- Entonces, el polinomio interpolador de Lagrange en forma de Newton es:

$$
\begin{split}
    & P(x) = f[-2] + f[-2, -1](x+2) + f[-2, -1, 1](x+2)(x+1) +\\
    & f[-2, -1, 1, 2](x+2)(x+1)(x-1) \iff\\
    & P(x) = -9 + 8(x+2) - 2(x+2)(x+1) + (x+2)(x+1)(x-1)
\end{split}
$$

5. Evalúe las cuatro expresiones halladas en el punto $x=0$. Comente.

$$
\begin{split}
    & P_{1}(0) = 0^3 + 0 + 1 = 1\\
    &P_{2}(0) = -\frac{(0-2)(0+2)(0-1)}{6} + \frac{11(0+1)(0+2)(0-1)}{12} +\\
    & \frac{3(0+1)(0-2)(0-1)}{4} - \frac{(0+1)(0+2)(0-2)}{2} = 1\\
    & P_{3}(0) = -1 + 4(0+1) - (0+1)(0-2) + (0+1)(0-2)(0+2) = 1\\
    & P_{4}(0) = -9 + 8(0+2) - 2(0+2)(0+1) + (0+2)(0+1)(0-1) = 1
\end{split}
$$

Vemos que todos los polinomios nos dan el mismo resultado en $x=0$, esto ocurre debido a que son el mismo polinomio expresados de formas diferentes. Todos los métodos conducen al mismo polinomio.

### Problema 2: Cotas del Error

Se van a tabular la función coseno (con el argumento medido en grados y no en radianes) en nodos equiespaciados para luego efectuar interpolación lineal en la misma entre nodos inmediatamente inferior e inmediatamente superior al ángulo deseado. Se desean errores menores de $5 \times 10^{-6}$. ¿Bastará con tabular de grado en grado?

- Como el coseno está medido en grados y no radianes la función que vamos a interpolar es:

$$
f(x) = \cos\left(\frac{2\pi}{360}x\right)
$$

- Como la interpolación la hacemos respecto de dos nodos, $N=1$ y por lo tanto su derivada $f^{N+1}$ es:

$$
\begin{split}
    & f'(x) = -\frac{2\pi}{360}\sin\left(\frac{2\pi}{360}x\right)\\
    & f''(x) = -\left( \frac{2\pi}{360}  \right)^{2} \cos\left(\frac{2\pi}{360}x\right)
\end{split}
$$

Entonces, la cota $K_{N+1}$ de $|f^{(N+1)}(x)|$ es:

$$
\begin{split}
    & |f''(x)| = \left| -\left(\frac{2\pi}{360}\right)^2 \sin \left(\frac{2\pi}{360}x\right) \right| \leq \left(\frac{2\pi}{360}\right)^2 \approx 0.0003\\
    & K_{2} \approx 0.0003
\end{split}
$$

El ángulo deseado estará entre los nodos $x_{0}$ y $x_{0} + 1$ entonces tenemos que:

$$
\begin{split}
    & |f(x) - P(x)| \leq \frac{|x-x_{0}|\cdot|x-x_{0}-1|K_{2}}{2!}
\end{split}
$$

El máximo valor que podemos tener será en el punto medio entre $x_{0}$ y $x_{0} + 1$ que es $x = \frac{2 x_{0} + 1}{2} = x_{0} + \frac{1}{2}$:

$$
\begin{split}
    & |f(x) - P(x)| \leq \frac{|x_{0} + \frac{1}{2} - x_{0}| \cdot  |x_{0} + \frac{1}{2} - x_{0} - 1|}{2} \cdot K_{2}\\
    & = \frac{K_{2}}{8} \approx 0.000038077 > 5 \times 10^{-6}
\end{split}
$$

Por lo tanto, no bastará con tabular de grado en grado.

### Problema 3: Base de Lagrange

Sean $l_{0}(x),\ldots, l_{N}(x)$ los polinomios de base de Lagrange para interpolar en $N+1$ abscisas dos a dos distintas $x_{0},\ldots, x_{N}$. Sin efectuar ningún cálculo, pruebe que $l_{0}(x) + \ldots + l_{N}(x)$ es el polinomio constante $1$.

- Si definimos el polinomio de grado $\le N$:

$$
P(x) = \left(\sum_{i=0}^{N} l_{i}(x) \right) - 1
$$

- Entonces, $P(x)$ tiene $N+1$ raíces distintas, lo que implica que $P(x)$ es el polinomio nulo (teorema de D'Alembert). Por lo tanto, $\sum_{i=0}^{N} l_{i}(x) = 1$
