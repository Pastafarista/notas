---
id: 1715155585-laboratorio-8-clculo-numrico
aliases:
  - Laboratorio 8 cálculo numérico
  - Laboratorio 8
tags:
  - cálculo-numérico
---

# Laboratorio 8

1. Problema 1: Regla de cuadratura I

Halle la única [[1713865555-reglas-de-cuadratura|regla]] de [[1713866424-grado-de-exactitud|grado de exactitud]] $\ge 3$ en el intervalo $[-1,1]$ que usa los nodos equiespaciados $-1,-\frac{1}{3},\frac{1}{3},1$ utilizando el [[1713873299-mtodo-interpolatorio|método interpolatorio]].

- La regla de cuadratura que queremos hallar tendrá la forma:

$$
\sum_{i=0}^{N} \alpha_i f(x_i)
$$

- Nuestros pesos $\alpha_i$ se pueden hallar con la integral de los pesos de la [[1713020577-polinomio-de-lagrange-por-forma-de-lagrange|forma de Lagrange]]:

$$
\begin{split}
    & \alpha_i = \int_{a}^{b} l_i(x)dx =\\
    & = \int_{-1}^{1} \frac{(x - x_{0}) \dots (x - x_{i-1})(x - x_{i+1})\dots (x - x_{N})}{(x_i - x_{0}) \dots (x_i - x_{i-1})(x_i - x_{i+1})\dots (x_{i} - x_{N})}dx\\
\end{split}
$$

- Calculamos los pesos $\alpha_i$:

Para $i = 0$:

$$
\begin{split}
    & \alpha_{0} = \int_{-1}^{1} \frac{(x + \frac{1}{3})(x - \frac{1}{3})(x - 1)}{(-1 + \frac{1}{3})(-1 - \frac{1}{3})(-1 - 1)}dx =\\
    & \int_{-1}^{1} \frac{(x^2 - \frac{1}{9})(x-1)}{(-\frac{2}{3})(-\frac{4}{3})(-2)}dx = \int_{-1}^{1} \frac{x^3 - x^2 - \frac{x}{9} + \frac{1}{9}}{-\frac{16}{9}}dx =\\
    & = -\frac{9}{16}\left( \int_{-1}^{1}x^3 dx - \int_{-1}^{1} x^2dx - \frac{1}{9}\int_{-1}^{1} x dx + \frac{1}{9}\int_{-1}^{1}dx \right) =\\
    & = -\frac{9}{16} \left( \left[\frac{x^4}{4}\right]_{-1}^{1} - \left[ \frac{x^3}{3} \right]_{-1}^{1} - \frac{1}{9}\left[ \frac{x^2}{2} \right]_{-1}^{1} +\frac{1}{9}[x]_{-1}^{1} \right) =\\
    & = -\frac{9}{16}\left( 0 - \frac{2}{3} - 0 + \frac{2}{9} \right) = \left( -\frac{9}{16} \right)\left( -\frac{4}{9} \right) = \frac{1}{4}
\end{split}
$$

Para $i = 1$:

$$
\begin{split}
    & \alpha_{1} = \int_{-1}^{1} \frac{(x + 1)(x - \frac{1}{3})(x - 1)}{(-\frac{1}{3} + 1)(-\frac{1}{3} - \frac{1}{3})(-\frac{1}{3} - 1)}dx =\\
    & = \int_{-1}^{1} \frac{(x^2 - 1)(x- \frac{1}{3})}{(\frac{2}{3})(-\frac{2}{3})(-\frac{4}{3})}dx = \int_{-1}^{1} \frac{x^3 - \frac{x^2}{3} -x + \frac{1}{3}}{\frac{16}{27}}dx=\\
    & = \frac{27}{16} \left( \int_{-1}^{1} x^3 dx - \frac{1}{3}\int_{-1}^{1}x^2dx - \int_{-1}^{1}xdx + \frac{1}{3}\int_{-1}^{1}dx \right)=\\
    &=\frac{27}{16}\left( \left[ \frac{x^4}{4} \right]_{-1}^{1} - \frac{1}{3} \left[ \frac{x^3}{3} \right]_{-1}^{1} - \left[ \frac{x^2}{2} \right]_{-1}^{1} + \frac{1}{3}\left[ x \right]_{-1}^{1} \right) =\\
    & = \frac{27}{16} \left( 0 - \frac{2}{9} - 0 + \frac{2}{3} \right) = \frac{27}{16} \cdot \frac{4}{9} = \frac{3}{4}
\end{split}
$$

Para $i=2$:

$$
\begin{split}
    & \alpha_{2} = \int_{-1}^{1} \frac{(x + 1)(x + \frac{1}{3})(x - 1)}{(\frac{1}{3} + 1)(\frac{1}{3} + \frac{1}{3})(\frac{1}{3} - 1)}dx =\\
    & = \int_{-1}^{1} \frac{(x^2 - 1)(x + \frac{1}{3})}{\frac{4}{3} \cdot \frac{2}{3} \cdot \left(-\frac{2}{3}\right)}dx = \\
    & = \int_{-1}^{1} \frac{x^3 + \frac{x^2}{3} - x - \frac{1}{3}}{-\frac{16}{27}}dx =\\
    & = -\frac{27}{16}\left( \int_{-1}^{1} x^3 dx + \frac{1}{3} \int_{-1}^{1} x^2 dx - \int_{-1}^{1} x dx - \frac{1}{3} \int_{-1}^{1} dx  \right ) =\\
    & = -\frac{27}{16} \left( \left[ \frac{x^4}{4} \right]_{-1}^{1} + \frac{1}{3} \left[ \frac{x^3}{3} \right]_{-1}^{1} - \left[ \frac{x^2}{2} \right]_{-1}^{1} - \frac{1}{3} \left[ x \right]_{-1}^{1} \right) =\\
    & = -\frac{27}{16} \left( 0 + \frac{2}{9} + 0 - \frac{2}{3} \right) = \left(-\frac{27}{16}\right) \cdot \left(-\frac{4}{9}\right) = \frac{3}{4}
\end{split}
$$

Para $i=3$:

$$
\begin{split}
    & \alpha_{3} = \int_{-1}^{1} \frac{(x + 1)(x + \frac{1}{3})(x - \frac{1}{3})}{(1 + 1)(1 + \frac{1}{3})(1 - \frac{1}{3})}dx =\\
    & = \int_{-1}^{1} \frac{(x^2 - \frac{1}{9})(x+1)}{2 \cdot \frac{4}{3} \cdot \frac{2}{3}}dx =\\
    & = \int_{-1}^{1} \frac{x^3 + x^2 - \frac{x}{9} - \frac{1}{9}}{\frac{16}{9}}dx =\\
    & = \frac{9}{16} \left( \int_{-1}^{1} x^3 dx + \int_{-1}^{1} x^2 dx - \frac{1}{9} \int_{-1}^{1} x dx - \frac{1}{9} \int_{-1}^{1} dx \right) =\\
    & = \frac{9}{16} \left( \left[ \frac{x^4}{4} \right]_{-1}^{1} + \left[ \frac{x^3}{3} \right]_{-1}^{1} - \frac{1}{9} \left[ \frac{x^2}{2} \right]_{-1}^{1} - \frac{1}{9} \left[ x \right]_{-1}^{1} \right) =\\
    & = \frac{9}{16} \left( 0 + \frac{2}{3} - 0 - \frac{2}{9} \right) = \frac{9}{16} \cdot \frac{4}{9} = \frac{1}{4}
\end{split}
$$

Ahora que tenemos los pesos $\alpha_i$ podemos calcular la regla de cuadratura:

$$
\begin{split}
    & \int_{-1}^{1} f(x)dx \approx \frac{1}{4}f(-1) + \frac{3}{4}f\left(-\frac{1}{3}\right) + \frac{3}{4}f\left(\frac{1}{3}\right) + \frac{1}{4}f(1)\\
\end{split}
$$

Vamos a ver el [[1713866424-grado-de-exactitud|grado de exactitud]] de nuestra [[1713865555-reglas-de-cuadratura|regla de cuadratura]]

Para un polinomio de grado $0$ de la forma $P(x)=A$ vemos que el grado de exactitud es $\ge 0$

$$
\begin{split}
	& \mathcal{I}_{4}(f) = \frac{A}{4} + \frac{3A}{4} + \frac{3A}{4} + \frac{A}{4} = 2A\\
	& \mathcal{I}(f) = \int_{-1}^{1}Adx = \left[ Ax\right]_{-1}^{1} = 2A
\end{split}
$$

Para un polinomio de grado 1 de la forma $P(x)= A + Bx$ vemos que el grado de exactitud es $\ge 1$ 

$$
\begin{split}
	& \mathcal{I}_4(f) = \frac{1}{4}(A-B) + \frac{3}{4}\left(A - \frac{B}{3}\right) + \frac{3}{4}\left(A + \frac{B}{3} \right) + \frac{1}{4}(A + B) =\\
	& = A \left( 2\cdot \frac{1}{4} + 2\cdot\frac{3}{4} \right) + B\left( -\frac{1}{4} - \frac{1}{4} + \frac{1}{4} + \frac{1}{4} \right) = 2A\\
	& \mathcal{I}(f) = \int_{-1}^{1} A + Bx \;dx = \left[ Ax \right]_{-1}^{1} + \left[ \frac{Bx^2}{4} \right]_{-1}^{1} = 2A
\end{split}
$$

Para un polinomio de grado 2 de la forma $P(x)= A + Bx + Cx^2$ vemos que el grado de exactitud es $\ge 2$

$$
\begin{split}
    & \mathcal{I}_4(f) = \frac{1}{4}(A - B + C) + \frac{3}{4}\left(A - \frac{B}{3} + \frac{C}{9}\right) + \frac{3}{4}\left(A + \frac{B}{3} + \frac{C}{9}\right)\\
    & + \frac{1}{4}(A + B + C) = A\left( \frac{1}{4} + \frac{3}{4} + \frac{3}{4} + \frac{1}{4} \right ) + B \left( -\frac{1}{4} - \frac{1}{4} + \frac{1}{4} + \frac{1}{4} \right) +\\
    & + C \left( \frac{1}{4} + \frac{1}{12} + \frac{1}{12} + \frac{1}{4} \right) = 2A + \frac{2C}{3} \\
    & \mathcal{I}(f) = \int_{-1}^{1} A + Bx + Cx^2 dx = \left[ Ax \right]_{-1}^{1} + \left[ \frac{Bx^2}{2} \right]_{-1}^{1} + \left[ \frac{Cx^3}{3} \right]_{-1}^{1} =\\
    & = 2A + \frac{2C}{3}
\end{split}
$$

Para un polinomio de grado 3 de la forma $P(x)= A + Bx + Cx^2 + Dx^3$ vemos que el grado de exactitud es $\ge 3$

$$
\begin{split}
    & \mathcal{I}_4(f) = \frac{1}{4}(A - B + C - D) + \frac{3}{4}\left(A - \frac{B}{3} + \frac{C}{9} - \frac{D}{27}\right)+\\
    &+ \frac{3}{4}\left(A + \frac{B}{3} + \frac{C}{9} + \frac{D}{27}\right) + \frac{1}{4}(A + B + C + D) =\\
    & = A \left( \frac{1}{4} + \frac{3}{4} + \frac{3}{4} + \frac{1}{4} \right) + B \left( -\frac{1}{4} - \frac{1}{4} + \frac{1}{4} + \frac{1}{4} \right) +\\
    & + C \left( \frac{1}{4} + \frac{1}{12} + \frac{1}{12} + \frac{1}{4} \right) + D \left( -\frac{1}{4} - \frac{1}{36} + \frac{1}{36} + \frac{1}{4} \right) =\\
    & = 2A + \frac{2C}{3}\\
    & \mathcal{I}(f) = \int_{-1}^{1} A + Bx + Cx^2 + Dx^3 dx =\\
    & = \left[ Ax \right]_{-1}^{1} + \left[ \frac{Bx^2}{2} \right]_{-1}^{1} + \left[ \frac{Cx^3}{3} \right]_{-1}^{1} + \left[ \frac{Dx^4}{4} \right]_{-1}^{1} =\\
    & = 2A + \frac{2C}{3}
\end{split}
$$

2. Sea $N\ge 0$ un entero arbitrario pero fijo en lo que sigue. Se conocen los valores $f(x^{*}), f'(x^{*}), \ldots , f^{N)}(x^{*})$ y se desea calcular aproximadamente:

$$
\int_{x^{*}-h}^{x^{*}+h} f(x)dx \quad \text{para} \quad h>0
$$

Obtenga la regla de [[1713866424-grado-de-exactitud|grado de exactitud]] máximo y determine tal grado.

 *Pista: Utiliza el [[1716663342-polinomio-interpolador-de-taylor|desarrollo de Taylor]] de $f(x)$ en torno a $x^{*}$.*

 El polinomio de Taylor en torno a $x^{*}$ de $f(x)$ de grado $N$ es:

 $$
 \begin{split}
    & P(x) = f(x^{*}) + f'(x^{*})(x - x^{*}) + \frac{f''(x^{*})}{2!}(x - x^{*})^2 + \ldots + \frac{f^{(N)}(x^{*})}{N!}(x - x^{*})^N\\
 \end{split}
 $$

 Si lo integramos, aproximaremos la integral de $f(x)$ en el intervalo $[x^{*}-h, x^{*}+h]$:

 $$
S \begin{split}
    & \int_{x^{*}-h}^{x^{*}+h} f(x)dx \approx \int_{x^{*}-h}^{x^{*}+h} P(x)dx =\\
    & =\int_{x^{*}-h}^{x^{*}+h} f(x^{*})dx + \int_{x^{*}-h}^{x^{*}+h} f'(x^{*})(x - x^{*})dx +\\
    & + \int_{x^{*}-h}^{x^{*}+h} \frac{f''(x^{*})}{2!}(x - x^{*})^2dx + \ldots + \int_{x^{*}-h}^{x^{*}+h} \frac{f^{(N)}(x^{*})}{N!}(x - x^{*})^Ndx =\\
    & = f(x^{*})\int_{x^{*}-h}^{x^{*}+h} dx + f'(x^{*})\int_{x^{*}-h}^{x^{*}+h} (x - x^{*})dx +\\
    & + \frac{f''(x^{*})}{2!}\int_{x^{*}-h}^{x^{*}+h} (x - x^{*})^2dx + \ldots + \frac{f^{(N)}(x^{*})}{N!}\int_{x^{*}-h}^{x^{*}+h} (x - x^{*})^Ndx =\\
    & = f(x^{*})\left[ x \right]_{x^{*}-h}^{x^{*}+h} + f'(x^{*})\left[ \frac{(x - x^{*})^{2}}{2} \right]_{x^{*}-h}^{x^{*}+h} + \frac{f''(x^{*})}{2!}\left[ \frac{(x-x^{*})^{3}}{3} \right]_{x^{*}-h}^{x^{*}+h} +\\
    & + \ldots + \frac{f^{(N)}(x^{*})}{N!}\left[ \frac{(x-x^{*})^{N+1}}{N+1} \right]_{x^{*}-h}^{x^{*}+h} =\\
    & = f(x^{*})\left[ x^{*} + h - x^{*} + h \right] + f'(x^{*})\left[ \frac{(x^{*} + h - x^{*})^{2}}{2} - \frac{(x^{*} - h - x^{*})^{2}}{2} \right] +\\
    & + \frac{f''(x^{*})}{2!}\left[ \frac{(x^{*} + h - x^{*})^{3}}{3} - \frac{(x^{*} - h - x^{*})^{3}}{3} \right] +\\
    & + \ldots + \frac{f^{(N)}(x^{*})}{N!}\left[ \frac{(x^{*} + h - x^{*})^{N+1}}{N+1} - \frac{(x^{*} - h - x^{*})^{N+1}}{N+1} \right] =\\
    & = f(x^{*})(h + h) + f'(x^{*})\left[ \frac{h^2}{2} - \frac{h^2}{2} \right] + \frac{f''(x^{*})}{2!}\left[ \frac{h^3}{3} + \frac{h^3}{3} \right] +\\
    & + \ldots + \frac{f^{(N)}(x^{*})}{N!}\left[ \frac{h^{N+1}}{N+1} - \frac{(-h)^{N+1}}{N+1} \right] =\\
    & = 2hf(x^{*}) + 0 + \frac{h^3}{3}f''(x^{*}) + \ldots + 2\frac{h^{N+1}}{(N+1)N!}f^{(N)}(x^{*}) \quad \text{ para N par}
 \end{split}
 $$

 Ahora que ya tenemos la [[1713865555-reglas-de-cuadratura|regla de cuadratura]], vamos a ver el grado de exactitud de la regla, usaremos $N=4$ para simplificar los cálculos.

 - Para un polinomio de grado $0$ de la forma $P(x) = A$ vemos que el grado de exactitud es $\ge 0$

 $$
 \begin{split}
    & \mathcal{I}^{Taylor}(f) = 2h\cdot f(x^{*}) + \frac{h^3}{3}f''(x^{*}) + 2\frac{h^{5}}{5!}f^{4)}(x^{*}) = 2A \cdot h\\
    & \mathcal{I}(f) = \int_{x^{*}-h}^{x^{*}+h} Adx = \left[ Ax \right]_{x^{*}-h}^{x^{*}+h} = 2Ah
 \end{split}
 $$

 - Para un polinomio de grado $1$ de la forma $P(x) = A + Bx$ vemos que el grado de exactitud es $\ge 1$

 $$
 \begin{split}
    & \mathcal{I}^{Taylor}(f) = 2h\cdot f(x^{*}) + \frac{h^3}{3}f''(x^{*}) + 2\frac{h^{5}}{5!}f^{4)}(x^{*}) = 2A \cdot h =\\
    & = 2Ah + 2Bhx^{*}\\
    & \mathcal{I}(f) = \int_{x^{*}-h}^{x^{*}+h} A + Bx \;dx = \left[ Ax + \frac{Bx^2}{2} \right]_{x^{*}-h}^{x^{*}+h} =\\
    & = 2Ah + 2Bhx^{*}
 \end{split}
 $$

Para un polinomio de grado $2$ de la forma $P(x) = A + Bx + Cx^2$ vemos que el grado de exactitud es $\ge 2$

$$
\begin{split}
    & \mathcal{I}^{Taylor}(f) = 2h\cdot f(x^{*}) + \frac{h^3}{3}f''(x^{*}) + 2\frac{h^{5}}{5!}f^{IV)}(x^{*}) = \\
    & = 2h \cdot (A + Bx^{*} + C(x^{*})^2) + \frac{h^3}{3} \cdot 2C\\ 
    & \mathcal{I}(f) = \int_{x^{*}-h}^{x^{*}+h} A + Bx + Cx^2 \;dx = \left[ Ax + \frac{Bx^2}{2} + \frac{Cx^3}{3} \right]_{x^{*}-h}^{x^{*}+h} =\\ 
    & = 2Ah + 2Bhx^{*} + \frac{2Ch^{3}}{3} + 2Ch(x^{*})^2\\
\end{split}
$$

En general, nuestra regla de cuadratura coincidirá cuando aproximamos un polinomio $\le N$, por lo tanto el [[1713866424-grado-de-exactitud|grado de exactitud]] es $\ge N$. Más concretamente:

- Cuando $N$ es par, como la derivada $N+1$ se anula, por lo tanto el grado de exactitud es $N+1$
- Cuando $N$ es impar, esto no ocurre, por lo que el grado de exactitud es $N$

3. Problema 3: Regla de cuadratura III

Para cuadrar funciones en el intervalo acotado $[a,b]$ se va a usar una [[1713865555-reglas-de-cuadratura|regla de cuadratura]] de la forma $Af(\mu) + Bf(b)$ donde $A,B,\mu$ son números reales independientes de $f$. Determínelos para lograr que el grado de exactitud sea los mayor posible.

- Para un polinomio de grado $0$ de la forma $P(x) = A'$:

$$
\begin{split}
    & \mathcal{I}'(f) = Af(\mu) + Bf(b) = A\cdot A' + A'\cdot B = A'(A + B) \\
    & \mathcal{I}(f) = \int_{a}^{b} A'dx = A'(b - a)\\
\end{split}
$$

Para que el grado de exactitud sea $\ge 0$ necesitamos que $A'(A + B) = A'(b - a)$, por lo que $A + B = b - a$

- Para un polinomio de grado $1$ de la forma $P(x) = A' + B'x$:

$$
\begin{split}
    & \mathcal{I}'(f) = Af(\mu) + Bf(b) = A(A' + B'\mu) + B(A' + B'b) =\\
    & = A'A + AB'\mu + BA' + BB'b = A'(A+B)+B'(B\cdot b + A \cdot \mu)\\
    & \mathcal{I}(f) = \int_{a}^{b} A' + B'xdx = A'(b - a) + \frac{B'(b^2 - a^2)}{2}
\end{split}
$$

- Para un polinomio de grado $2$ de la forma $P(x) = A' + B'x + C'x^2$:

$$
\begin{split}
    & \mathcal{I}'(f) = Af(\mu) + Bf(b) = A(A' + B'\mu + C'\mu^2) + B(A' + B'b + C'b^2) =\\
    & A'(A + B) + B'(Bb + A\mu) + C'(A\mu^2 + B b^2)\\
    & \mathcal{I}(f) = \int_{a}^{b} A' + B'x + C'x^2dx = A'(b - a) + \frac{B'(b^2 - a^2)}{2} + \frac{C'(b^3 - a^3)}{3}
\end{split}
$$

Por lo tanto se nos quedaría el siguiente sistema:

$$
\begin{split}
    & \begin{cases}
        A'(A+B) = A'(b - a)\\
        A'(A+B) + B'(Bb + A\mu) = A'(b - a) + \frac{B'(b^2 - a^2)}{2}\\
        A'(A+B) + B'(Bb + A\mu) + C'(A\mu^2 + B b^2) = A'(b - a) +\\
        \frac{B'(b^2 - a^2)}{2} + \frac{C'(b^3 - a^3)}{3}
    \end{cases}
\end{split}
$$

Si restamos algunos términos:

$$
\begin{split}
    & \begin{cases}
        A'(A+B) = A'(b - a)\\
        B'(Bb + A\mu) = \frac{B'(b^2 - a^2)}{2}\\
        C'(A\mu^2 + B b^2) = \frac{C'(b^3 - a^3)}{3}
    \end{cases} \implies
    \begin{cases}
        A + B = b - a\\
        Bb + A\mu = \frac{b^2 - a^2}{2}\\
        A\mu^2 + Bb^2 = \frac{b^3 - a^3}{3}
    \end{cases}
\end{split}
$$

Se nos presenta la misma estructura que el [[1713875089-mtodo-de-coeficientes-indeterminados-reglas-cuadratura|método de coeficientes indeterminados]], en nuestro caso tendríamos dos nodos de interpolación $x_{0}=\mu, x_{1}=b$ (uno de los nodos es el extremo del intervalo) y los pesos $\alpha_{0}=A, \alpha_{1}=B$. Como tenemos dos nodos, nos bastará con dos ecuaciones para resolver el sistema.

$$
\begin{split}
    & \begin{cases}
        A + B = b - a\\
        Bb + A\mu = \frac{b^2 - a^2}{2}
    \end{cases} \implies\\
    & \begin{cases}
        A = b - a - B\\
        Bb + (b - a - B)\mu = \frac{b^2 - a^2}{2}
    \end{cases} \implies\\
    & B(b - \mu) + (b-a)\mu = \frac{b^2 - a^2}{2} \implies\\
    & B = \frac{\frac{b^2 - a^2}{2} - (b-a)\mu}{b - \mu} = \frac{b^2 - a^2 - 2(b-a)\mu}{2(b - \mu)}\\
    & A = b - a - \frac{b^2 - a^2 - 2(b-a)\mu}{2(b - \mu)} = \\
    & = \frac{2(b-a)(b-\mu) - b^2 + a^2 + 2b \mu  - 2a \mu }{2(b - \mu)} =\\
    & = \frac{2b^2 - 2b \mu  - 2ab + 2a \mu  - b^2 + a^2 + 2b \mu  - 2 a \mu }{2(b - \mu)} =\\
    & = \frac{a^2 + b^2 - 2ab}{2(b - \mu)} = \frac{(b - a)^2}{2(b - \mu)}
\end{split}
$$

Por lo tanto, los pesos $A, B$ son:

$$
\begin{split}
    & A = \frac{(b - a)^2}{2(b - \mu)}\\
    & B = \frac{(b-a)(b+a-2 \mu )}{2(b - \mu)}
\end{split}
$$

Para determinar el valor de $\mu$ podemos usar la tercera ecuación:

$$
\begin{split}
    & A\mu^2 + Bb^2 = \frac{b^3 - a^3}{3} \implies\\
    & \frac{(b-a)^2}{2(b - \mu)}\mu^2 + \frac{(b-a)(b+a-2 \mu )}{2(b - \mu)}b^2 = \frac{b^3 - a^3}{3} \implies\\
    & \mu = \frac{2a + b}{3}
\end{split}
$$

Entonces, los pesos $A, B$ ahora son:

$$
\begin{split}
    & A = \frac{(b - a)^2}{2(b - \frac{2a + b}{3})} = \frac{3(b-a)}{4}\\
    & B = \frac{(b-a)(b+a-2 \cdot \frac{2a + b}{3} )}{2(b - \frac{2a + b}{3})} =\\
    & = \frac{b-a}{4}
\end{split}
$$

Por lo tanto la solución es:

$$
\begin{split}
    & A = \frac{3(b-a)}{4}\\
    & B = \frac{b-a}{4}\\
    & \mu = \frac{2a + b}{3}
\end{split}
$$

