---
id: 1716460391-laboratorio-7-clculo-numrico
aliases:
  - Laboratorio 7 cálculo numérico
  - Laboratorio 7
tags:
  - cálculo-numérico
---

# Laboratorio 7

## Problema 1: Reglas de cuadratura

Halle la [[1713865555-reglas-de-cuadratura|regla de cuadratura]] en el intervalo $[a,b]$ para $N=1$ y nodos $x_{0}=a$ y $x_{1}=b$

##### **Opción A.** utilizando  el [[1713873299-mtodo-interpolatorio|método interpolatorio]]. Escriba la [[1709641715-polinomio-interpolador-de-lagrange|recta de Lagrange]] en [[1716653781-forma-de-newton|forma de Newton]] e intégrela. ¿Cuál es el [[1713866424-grado-de-exactitud|grado de exactitud]] de la regla?

Primero calcularemos el [[1709641715-polinomio-interpolador-de-lagrange|polinomio interpolador de Lagrange]] en forma de Newton, comenzaremos calculando las [[1716653895-diferencia-dividida|diferencias divididas]]:

$$
\begin{split}
	& f[x_0] = x_0 = f(a)\\
	& f[x_0,x_1] = \frac{f[x_1]-f[x_0]}{x_1 - x_0} = \frac{f(b) - f(a)}{b - a}
\end{split}
$$

Ahora ya podemos construir el polinomio:

$$
P(x) = f[x_0] + f[x_0,x_1](x - x_0)  = f(a) + \frac{f(b) - f(a)}{b-a}(x - a)
$$

Para calcular la regla de cuadratura, integramos el polinomio:

$$
\begin{split}
	& \mathcal{I}_{2}(f) = \int_{a}^{b} P(x)dx = \int_{a}^{b} f(a) + \frac{f(b) - f(a)}{b-a}(x - a)dx =\\
	& f(a)\int_{a}^{b}dx + \frac{f(b)-f(a)}{b-a}\left(\int_{a}^{b}xdx - \int_{a}^{b}adx \right) =\\
	& = f(a)(b-a) + \frac{f(b) - f(a)}{b-a}\left( \frac{b^2 - a^2}{2} - a(b-a) \right) =\\
	& = f(a)(b-a) + \frac{(f(b)-f(a))(b-a)(b+a)}{2(b-a)} - \frac{(f(b)-f(a))a(b-a)}{b-a} =\\
	& = f(a)(b-a) + \frac{(f(b)-f(a))(b+a)}{2} -  a(f(b)-f(a)) = \\
	& = f(a)(b-a) + (f(b) - f(a))\left( \frac{b+a}{2} - a \right) = f(a)(b-a) + (f(b) - f(a))\frac{b-a}{2} =\\
	& = (b-a)\left( f(a) + \frac{f(b) - f(a)}{2} \right) = (b-a) \frac{f(a) + f(b)}{2}
\end{split}
$$

Vemos que si $f$ es lineal, se trata de la [[1713865721-regla-del-punto-medio|regla del punto medio]].

Calculemos su [[1713866424-grado-de-exactitud|grado de exactitud]]:

- Para $n=0$, los polinomios tienen la forma $f(x)=A$. Vemos que la integral y la regla coinciden, por lo que está última tendrá grado de exactitud mayor o igual que $0$.

$$
\begin{split}
	& \mathcal{I}(f) = \int_{a}^{b} f(x) dx = \int_{a}^{b} a dx = \left[ Ax \right]_{a}^{b} = A(b-a)\\
	& \mathcal{I}^{PM}(f) = (b-a)\frac{A + A}{2} = A (b-a)
\end{split}
$$

- Para $n=1$, los polinomios tienen la forma $f(x) = A + Bx$. Vemos que también coinciden y que el grado será mayor o igual a $1$.

$$
\begin{split}
	& \mathcal{I}(f)=\int_{a}^{b}A + Bxdx = \int_{a}^{b}A dx + \int_{a}^{b}Bxdx = \left[ Ax \right]_{a}^{b} + \left[ \frac{Bx^2}{2} \right]_{a}^{b} =\\
	& = A(b-a) + \frac{B}{2}(b^2 - a^2) \\
	& \mathcal{I}^{PM}(f) = (b-a) \frac{A + Ba + A Bb}{2} = A(b-a) + \frac{B(b+a)(b-a)}{2}=\\
	& = A(b-a) + \frac{B}{2}(b^2 - a^2)
\end{split}
$$
- Para $n=2$, probaremos con $f(x)=x^2$. Aquí ya vemos que no coinciden y que por lo tanto el grado de exactitud es $1$.

$$
\begin{split}
	& \mathcal{I}(f)= \int_{a}^{b} x^2 dx = \left[ \frac{x^3}{3} \right]_{a}^{b} = \frac{b^3 - a^3}{3}\\
	& \mathcal{I}^{PM}(f)=(b-a)\frac{b^2 - a^2}{2}	
\end{split}
$$

##### **Opción B.** utilizando el [[1713873299-mtodo-interpolatorio|método interpolatorio]]. Cálculo los pesos $\alpha_i$ utilizando los polinomios de la [[1716650816-forma-de-lagrange|base de Lagrange]]. ¿Cuál es el [[1713866424-grado-de-exactitud|grado de exactitud]] de la regla?

Tendremos dos elementos de la base de Lagrange, $l_0$ y $l_1$:

$$
\begin{split}
	& l_0 = \frac{x - x_1}{x_0 - x_1} = \frac{x - b}{a - b}\\
	& l_1 = \frac{x - x_0}{x_1 - x_0} = \frac{x-a}{b-a}
\end{split}
$$

Para nuestra regla de cuadratura, los pesos $\alpha_i = \int^{b}_{a} l_i(x) dx$:

$$
\begin{split}
	& \alpha_0 = \int_{a}^{b} l_0 dx = \int_{a}^{b}  \frac{x-b}{a-b}dx = \int_{a}^{b} \frac{x}{a-b} dx - \int_{a}^{b} \frac{b}{a-b}dx = \\
	& \left[ \frac{x^2}{2(a-b)} \right]_{a}^{b} - \left[ \frac{xb}{a-b} \right]_{a}^{b} = \frac{b^2 - a^2}{2a - 2b} - \frac{b^2 - ab}{a - b} =\\
	& \frac{b^2 - a^2 - 2b^2 + 2ab}{2a-2b} = \frac{-(a^2 + b^2 - 2ab)}{2a - 2b} =\\
	& -\frac{(a-b)^2}{2(a-b)} = -\frac{a-b}{2}
\end{split}
$$
$$
\begin{split}
	& \alpha_1 = \int_{a}^{b} l_1 dx = \int_{a}^{b} \frac{x-a}{b-a}dx = \int_b^{a} \frac{x}{b-a}dx - \int_{b}^{a} \frac{a}{b-a}dx =\\
	& \left[ \frac{x^2}{2(b-a)} \right]_{a}^{b} - \left[ \frac{xa}{b-a} \right]_{a}^{b} = \frac{b^2 - a^2}{2(b-a)} - \frac{ab - a^2}{b-a} =\\
	& \frac{b^2 - a^2 - 2ab + 2a^2}{2(b-a)} = \frac{a^2 + b^2 - 2ab}{2(b-a)} = \frac{(a-b)^2}{-2(a-b)}) =\\
	& = -\frac{a-b}{2}
\end{split}
$$
Ahora ya podemos construir nuestra regla de cuadratura:

$$
\begin{split}
	& \mathcal{I}_{N+1} = \sum_{i=0}^{N} \alpha_ix_i \iff\\
	& \mathcal{I}_{2} = -\frac{a-b}{2}(f(a)+f(b)) = \frac{b-a}{2}[f(a) + f(b)]
\end{split}
$$
Vemos que se trata de la [[1713865822-regla-del-trapecio|regla del trapecio]]

Ahora, comprobemos su [[1713866424-grado-de-exactitud|grado de exactitud]]:

- Para $n=0$ tenemos $f(x)=A$, vemos que el grado de exactitud será mayor o igual de $0$:

$$
\begin{split}
	& \mathcal{I}(f) = \int_{a}^{b} f(x)dx = \int_{a}^{b} Adx = \left[ Ax \right]_{a}^{b} = Ab - Aa\\
	& \mathcal{I}^{T}(f) = \frac{b-a}{2}[A + A] = A(b-a) = Ab - Aa
\end{split}
$$
- Para $n=1$ tenemos $f(x) = A + Bx$, vemos que el grado de exactitud será mayor o igual que $1$:

$$
\begin{split}
	& \mathcal{I}(f) = \int_{a}^{b}f(x)dx = \int_{a}^{b} A + Bx dx = \left[ Ax \right]_{a}^{b} + \left[ \frac{Bx^2}{2} \right]_{a}^{b} = A(b-a) + \frac{B}{2}(b^2 - a^2)\\
	& \mathcal{I}^{T}(f) = \frac{b-a}{2}(A + Ba + A + Bb) = \frac{b-a}{2}(2A + B(a+b)) = A(b-a) + \frac{B(b-a)(b+a)}{2} =\\
	& A(b-a) + \frac{B}{2}(b^2 - a^2)
\end{split}
$$

- Para $n=2$ tenemos $f(x)=x^2$, vemos que la regla de cuadratura difiere de la integral de $f$, por lo tanto podemos asegurar que el grado de exactitud de la regla de cuadratura es $1$.
$$
\begin{split}
	& \mathcal{I}(f) = \int_{a}^{b}x^2 dx = \left[ \frac{x^3}{3} \right]_{a}^{b} = \frac{b^3 - a^3}{3}\\
	& \mathcal{I}^{T}(f) = \frac{b-a}{2}(f(a)+f(b)) = \frac{b-a}{2}(a^2 + b^2)
\end{split}
$$
##### **Opción C.** utilizando el [[1713875089-mtodo-de-coeficientes-indeterminados-reglas-cuadratura|método de coeficientes indeterminados]] con $k=N$. Calcule los pesos $\alpha_i$ utilizando los polinomios de la base de Lagrange. ¿Cuál es el [[1713866424-grado-de-exactitud|grado de exactitud]] de la regla?

Vamos a encontrar los pesos $\alpha_i$. En nuestro caso $N=1$ por lo tanto tendremos que resolver el siguiente sistema de ecuaciones:

$$
\begin{cases}
    \alpha_0 + \alpha_1 = b - a\\
    \alpha_0a + \alpha_1b = \frac{b^2 - a^2}{2}
\end{cases}
$$

Lo resolveremos de forma matricial:

$$
\begin{split}
    & \left(\begin{array}{cc|c}
        1 & 1 & b - a\\
        a & b & \frac{b^2 - a^2}{2}
    \end{array}\right) \sim 
    \left(\begin{array}{cc|c}
        1 & 1 & b - a\\
        0 & b - a & \frac{b^2 - a^2}{2} - ab + a^2
    \end{array}\right)
\end{split}
$$

Ahora despejamos los pesos $\alpha_i$:

$$
\begin{split}
    & \begin{cases}
        \alpha_{0} + \alpha_{1} = b - a\\
        (b-a)\alpha_{1} = \frac{b^2 - a^2}{2} - ab + a^2 
    \end{cases} \iff
    \begin{cases}
        \alpha_{0} + \alpha_{1} = b - a\\
        (b-a)\alpha_{1} = \frac{a^2 + b^2 - 2ab}{2} = \frac{(b-a)^2}{2}
    \end{cases} \iff\\
    & \begin{cases}
        \alpha_{0} + \alpha_{1} = b - a\\
        \alpha_{1} = \frac{(b-a)}{2}
    \end{cases} \iff
    \begin{cases}
        \alpha_{0} = (b-a) - \frac{(b-a)}{2} = \frac{b-a}{2}\\
        \alpha_{1} = \frac{b-a}{2}
    \end{cases}
\end{split}
$$

Una vez tenemos los pesos, nuestra [[1713865555-reglas-de-cuadratura|regla de cuadratura]] será:

$$
\mathcal{I}_2 = \sum_{i=0}^N \alpha_i f(x_i) = \frac{b-a}{2}(f(a) + f(b))
$$

Se trata otra vez de la [[1713865822-regla-del-trapecio|regla del trapecio]], por lo tanto ya sabemos que su [[1713866424-grado-de-exactitud|grado de exactitud]] es de $1$.