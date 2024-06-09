---
id: 1713867804-teorema-de-manolo
aliases:
  - Teorema de manolo
tags:
  - cálculo-numérico
---

# Teorema de manolo

Sea $\mathcal{I}_{N+1} = \alpha_{0}f(x_{0}) + \ldots + \alpha_Nf(x_N)$ una [[1713865555-reglas-de-cuadratura|reglas de cuadratura]] que integra exactamente las funciones constantes. Entonces, el [[1713866424-grado-de-exactitud|grado de exactitud]] es $M$ si y solo si la regla $\mathcal{I}_{N+1}$ no da error al cuadrar las funciones ${1,x,x^2,x^3,\ldots,x^{M}}$ y da error al cuadrar $x^{M+1}$.

Grado de exactitud de $\mathcal{I}_{N+1}(f)$ es $M \iff \mathcal{I}(1) = \mathcal{I}_{N+1}(1),\ldots , \mathcal{I}_{N+1}(x^{4}) = I_{N+1}(x^{4})$ y $\mathcal{I} (x^{M+1}) \neq \mathcal{I}_{N+1}(x^{M+1})$.

$\impliedby$

$$
\begin{split}
    & f = A + Bx + Cx^2 + \ldots + Kx^M\\
    & \mathcal{I}_{N+1} ?= \mathcal{I}(f) = \int_{a}^{b} A + Bx + Cx^2 + \ldots dx =\\
    & = \int_{a}^{b} A dx + \int_{a}^{b} Bx dx + \ldots + \int_{a}^{b} Kx^M dx =\\
    & = A I_{N+1}(1) + B I_{N+1}(x) + \ldots + K I_{N+1}(x^M)\\
    & I_{N+1}(x^{i}) = \alpha_{0}x_{0}^{i} + \ldots + \alpha_{N}x_{N}^{i} = \sum_{j=0}^{N} \alpha_{j}x_{j}^{i}\\
    & f = A_{0} + A_{1}x + A_{2}x^2 + \ldots + A_{M}x^M\\
    & \mathcal{I}(f) = \int_{a}^{b} \sum_{i=0}^{M} A_{i}x^{i} dx = \sum_{i=0}^{M} A_{i} \int_{a}^{b} x^{i} dx =\\
    & = \sum_{i=0}^{M} A_{i} I(x^{i}) = \sum_{i=0}^{M} A_{i} I_{N+1}(x^{i}) = ? \mathcal{I}_{N+1}(f)\\
    & \mathcal{I}_{N+1}(f) = \alpha_{0}f(x_{0}) + \ldots + \alpha_{N}f(x_{N}) = \sum_{j=0}^{N} \alpha_{j}f(x_{j}) =\\
    & = \sum_{j=0}^{M}A_i \sum_{j=0}^{N} \alpha_{j}x_{j}^i =\\
    & = \sum_{j=0}^{N} \sum_{i=0}^{M} A_{i} \alpha_{j}x_{j}^i =\\
    & = \sum_{j=0}^{N} \alpha_j \sum_{i=0}^{M} A_i x_{j}^i =\\
    & = \sum_{j=0}^{N} \alpha_j f(x) = \mathcal{I}_{N+1}(f)
\end{split}
$$

Un polinomio de grado $M+1$ y para, $x^{M+1}$ no se cumple por hipótesis.

$\implies$

$$
\begin{split}
    & \mathcal{I}_{N+1}(f) \text{ cuadra } f = A + Bx + Cx^2 + \ldots + Kx^M\\
    & 1, ..., x^{M} \text{ son polinomio de grado } \le M \text{ luego } \mathcal{I}_{N+1}(x^{j} ) = \mathcal{I}(x^{j}) \quad \forall j = 0,1,\ldots,M\\ 
\end{split}
$$

Para $\mathcal{I}_{N+1}(f)$ no cuadra $f(x) = A + Bx + Cx^2 + \ldots + Kx^{M+1}$:

- Supongamos por reducción al absurdo que $\mathcal{I}_{N+1}(f)$ cuadra, entonces:

$$
\begin{split}
    & \mathcal{I}_{N+1}(1) + \mathcal{I}(x) + 0\mathcal{I}(x^2) + \ldots + 1\mathcal{I}(x^{M+1}) =\\
    & = \mathcal{I}_{N+1}(x^{M+1}) = \mathcal{I}_{N+1}(f)\\
    & 1, x, x^2, \ldots , x^{M} \text{ son de grado } \le M \text{ luego:}\\
    & \mathcal{I}_{N+1}(1) = \mathcal{I}(1)\\
    & \vdots\\
    & \mathcal{I}_{N+1}(x^{M}) = \mathcal{I}(M)\\
\end{split}
$$

G.E $M \implies \exists A_{0},\ldots ,A_{M+1}$, con $A_{M+1}\neq 0$, tales que $f = A_{0} + A_{1}x + \ldots + A_Mx^{M} + A_{M+1}x^{M+1}$ (no cuadra).

$$
\mathcal{I}_{N+1}(x^{M+1}) \neq \mathcal{I}(x^{M+1})
$$

Suponemos, por reducción al absurdo que, $\mathcal{I}(x^{M+1})=\mathcal{I}(x^{M+1} )$ con $f = g + A_{M+1}x^{M+1}$

$$
\begin{split}
    & \mathcal{I}_{N+1}(f) = \mathcal{I}_{N+1} (g + A_{M+1}x^{M+1}) = \mathcal{I}_{N+1}(g) + A_{M+1}\mathcal{I}_{N+1}(x^{M+1}) =\\
    & = \mathcal{I}(g) + A_{M+1}\mathcal{I}(x^{M+1}) = \int_{a}^{b} g(x)dx + A_{M+1}\int_{a}^{b} x^{M+1}dx =\\
    & = \int_{a}^{b} g(x) + A_{M+1}x^{M+1}dx = \mathcal{I}(f)
\end{split}
$$

$\mathcal{I}_{N+1}(f) = \mathcal{I}(f)$ es un absurdo, luego $\mathcal{I}_{N+1}(x^{M+1}) \neq \mathcal{I}(x^{M+1})$.
