---
id: 1716491727-teorema-de-banach
aliases:
 - Teorema de Banach
---

#topología

"Si $f:X \rightarrow Y$ es una [[1716491727-funcin-contractiva|Función contractiva]] en el [[1716491727-espacio-completo|Espacio completo]] $X$, entonces para cualquier $x_0$ la [[1716491727-sucesin-convergente|sucesión]] $x_n=f(x_{n-1})$ converge al punto $x$ y se da que $f(x)=x$. El [[1716491727-punto-fijo|Punto fijo]] es único" 

## Teorema Punto Fijo de Banach

Asumimos que estamos en un [[1716491727-espacio-completo|Espacio completo]] $\implies$ Estamos en un [[1716491727-espacio-mtrico|Espacio métrico]] $\implies \text{ existe una distancia}$ , y al ser un espacio completo tenemos que la [[1716491727-sucesin-de-cauchy|Sucesión de Cauchy]] siempre es una [[1716491727-sucesin-convergente|Sucesión convergente]]

También que tenemos una función $f$ que es [[1716491727-funcin-contractiva|Función contractiva]] $\implies$ $f$ es [[1716491727-funcin-continua|Función continua]]

Con todo esto el teorema de Banach asegura que esta función $f$ va a tener un único [[1716491727-punto-fijo|Punto fijo]]

## ¿Por qué solo un punto fijo?

$f \text{ contractiva} \implies f \text{ solo tiene un punto fijo}$

Supongamos que hay dos tal que $f(a) = a$ y $f(b) = b$

- hagamos $K \cdot d(a,b) \geq d(f(a), f(b)) \;$ con $1 > K > 0$, pero $d(a,b)=d(f(a),f(b))\implies K = 1$
- $K$ debe ser menor que 1 ¡¡¡Contradicción!!!, por lo tanto $f$ solo puede tener un punto fijo 

## Existencia del punto fijo

- Ahora demostraremos que $f$ debe de tener un punto fijo

$x_1 = f(x_0)$
$x_n = f(x_{n-1})$

Supongamos que esta sucesión es de Cauchy

Vamos a ver que pasa cuando tendemos al límite

$$lim_{n \rightarrow \infty} x_n = lim_{n \rightarrow \infty} \; f(x_{x_n - 1}) = f(x_n)$$

Vemos que en esta sucesión nos demuestra que existe al menos un punto fijo $x_n$ ya que en el infinito $x_n = f(x_n)$

## Demostremos que la sucesión es una [[1716491727-sucesin-de-cauchy|Sucesión de Cauchy]]

Supongamos que tenemos $(x_n, x_m) : m > n \;\; m,n \in \mathbb{N}$

Como la función es una  [[1716491727-funcin-contractiva|Función contractiva]] sabemos que:

$d(f(x_n),d(x_m)) \leq \alpha \cdot d(x_n,x_m)$

$x_1 = f(x_0) \;\; x_2 = f^2(x_0) = f(f(x_0)) \;\; x_n = f^n(x_0)$

$d(f(x_n),f(x_m)) \leq \alpha d(f^n(x_0), f^m(x_0)) \leq$ $\alpha^2 d(f^{n-1}(x_0), f^{m-1}(x_0)) \leq$ $\alpha^3 d(f^{n-2}(x_0),f^{m-2}(x_0)) \leq$ $... \; \; \leq \alpha^{n-1} \cdot d(x_0, x_{m-n}) \leq \alpha^n \cdot d(x_0, x_{m-n})$


Usando la [[1716491727-desigualdad-triangular|Desigualdad triangular]] y que es función contractiva (cuando hacemos el $\leq$)

$$ \begin{split} 
& \alpha^n d(x_0, x_{m-n}) \leq \alpha^{n}\cdot ((d(x_0, x_1) + d(x_1 , x_2) + ... + d(x_{m-n-1},x_{m-n})) \leq\\
& \leq \alpha^{n}(d(x_0,x_1) + \alpha d(x_0, x_1) + \alpha^2 d(x_0, x_1) + ... + \alpha^{m -n -1}d(x_0, x_1)) \leq\\
& \leq \alpha ^n (d(x_0,x_1))) \sum_{k=0}^{\infty} \alpha^k = \alpha^n \frac{1}{1 - \alpha} \cdot d(x_0, x_1) = \epsilon\end{split}$$

Como vemos se cumple que para cada $N$ existe un $\epsilon$ tal que $n,m > N, \;\; d(x_n,x_m) < \epsilon$