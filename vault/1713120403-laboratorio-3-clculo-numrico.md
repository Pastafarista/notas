---
id: 1713120403-laboratorio-3-clculo-numrico
aliases:
  - Laboratorio 3 cálculo numérico
  - Laboratorio 3
tags:
  - cálculo-numérico
---

# Laboratorio 3

### Problema 1: Raíces de ecuaciones.

1. Se necesita resolver la ecuación

$$
y^3 + 2xy + x^{8} = 1 
$$

donde $y$ es la incógnita y $x$ es un parámetro de pequeño valor absoluto. Cuando $x = 0$ la ecuación tiene solución $y=1$. Suponga que existe una función $y = \phi(x)$ con $\phi(0)=1$ que permite calcular una solución como función del parámetro. Halle el polinomio de Taylor de grado $\le  2$ de $\phi(x)$ en $x=0$ haciendo $y=1 + \alpha x +\beta x^2 + \ldots$, y sustituyendo en la ecuación para determinar $\alpha$ y $\beta$.

$$
\begin{split}
	& y = 1 + \alpha x + \beta x^2\\
	& (1 + \alpha x + \beta x^2)^3 + 2x(1 + \alpha x + \beta x^2) + x^8 = 1 =\\
    & 3\alpha^2x^2 + 3\beta x^2 + 3\alpha + 1 + 2x +2\alpha x^2 + 2 \beta x^3 +x^{8} = 1 
\end{split}
$$

Quitamos los términos que tienen exponentes mayores a 2 y obtenemos

$$
x^2(3\alpha^2 + 2\alpha + 3\beta) + x(3\alpha + 2) = 0
$$

$$
\begin{cases}
    & 3\alpha + 2 = 0\\
    & 3\alpha^2 + 2\alpha + 3\beta = 0
\end{cases} \implies \alpha = -\frac{2}{3} \quad \beta = 0
$$

Entonces, nuestro polinomio de Taylor es:

$$
P(x) = 1 - \frac{2}{3}x
$$

2. Vuelva a hallar ese mismo polinomio poniendo

$$
\phi (x)^3 + 2x\phi (x) + x^{8} = 1 
$$

y derivando reiteradamente con respecto a $x$

$$
\begin{split}
    & f(x) = \phi (x)^3 + 2x\phi (x) + x^{8} - 1\\
    & f'(x) = 3\phi (x)^2\phi'(x) + 2\phi (x) + 2x\phi'(x) + 8x^7\\
    & f''(x) = 6\phi (x)\phi'(x)^2 + 3\phi (x)^2\phi''(x) + 2\phi'(x) + 2\phi'(x) + 8\cdot 7x^6\\
\end{split}
$$

Si sustituimos $x=0$ en $f(x)$, $f'(x)$ y $f''(x)$, obtenemos

$$
\begin{cases}
    & f(0) = 0\\
    & f'(0) = 3\alpha + 2\\
    & f''(0) = 6 \alpha^2 + 6\beta + 4\alpha 
\end{cases}
$$

Entonces, nuestro polinomio de Taylor de f(x) es:

$$
P(x) = (3\alpha + 2)x + \frac{1}{2}(6\alpha^2 + 6\beta + 4\alpha)x^2
$$

Si igualamos este polinomio a 0, obtenemos el sistema de ecuacionesantes mencionado. Resolviendo el sistema, obtenemos $\alpha = -\frac{2}{3}$ y $\beta = 0$.

$$
P(x) = 1 - \frac{2}{3}x
$$

3. Use el polinomio encontrado para obtener aproximadamente una raíz de la ecuación primero cuando $x=0.1$ y luego cuando $x=0.01$. Sustituya las aproximaciones encontradas en el primer miembro de la ecuación y comente.

Si $x=0.1$ entonces la ecuación es

$$
y_{3} + 2(0.1)y + 0.1^{8} = 1
$$

La solución estimada es

$$
y = 1 - \frac{2}{3}(0.1) = \frac{14}{15} \approx 0.9333
$$

Sustituyendo en la ecuación, obtenemos

$$
\begin{split}
    & \left(\frac{14}{15}\right)^3 + 2(0.1)\left(\frac{14}{15}\right) + 0.1^{8} \approx 0.9988
\end{split}
$$

Con $x=0.01$ la ecuación es

$$
y_{3} + 2(0.01)y + 0.01^{8} = 1
$$

La solución estimada es

$$
y = 1 - \frac{2}{3}(0.01) = \frac{149}{150} \approx 0.9933
$$

Sustituyendo en la ecuación, obtenemos

$$
\begin{split}
    & \left(\frac{149}{150}\right)^3 + 2(0.01)\left(\frac{149}{150}\right) + 0.01^{8} \approx 0.999999
\end{split}
$$

Vemos que para valores pequeños absolutos de $x$, la aproximación es bastante buena.
