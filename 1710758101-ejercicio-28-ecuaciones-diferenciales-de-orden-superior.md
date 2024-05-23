---
id: 1710758101-ejercicio-28-ecuaciones-diferenciales-de-orden-superior
aliases:
  - Ejercicio 28 ecuaciones diferenciales de orden superior
tags:
  - ecuaciones-diferenciales
---

# Resuelve la ecuación $x^2y'' + 8xy' + 10y = \frac{\ln (x)}{x}$ mediante el método de variación de constantes


$$
\begin{split}
    & x^2y'' 8xy' + 10y = \frac{\ln (x)}{x} \implies y'' + \frac{8}{x}y' + \frac{10}{x^2}y = \frac{\ln (x)}{x^3 }
\end{split}
$$

1. SGEH:

$$
\begin{split}
    & \begin{cases}
        & x^2y'' + 8xy' + 10y = 0\\
        & y = x^{m} \implies y' = mx^{m-1} \implies y''  = m(m-1)x^{m-2} 
    \end{cases} \implies\\
& x^2m(m-1)x^{m-2} + 8x(m)s^{m-1} + 10x^{m} = 0 \implies\\
    & \implies x^{m}(m^2 - m + 8m + 10) = 0 \implies m^2 + 7m + 10 = 0 \implies \begin{cases} m_1 = -2 \\ m_2 = -5 \end{cases} \implies\\ 
    & \implies Y_{SGEH} = C_1x^{-2} + C_2x^{-5}
\end{split}
$$

2. SGEC / SPEC:

$$
\begin{split}
    & y = C_{1}(x)x^{-2x} + C_{2}(x)x^{-5}\\
    & \begin{cases}
        & C_{1}'(x)y_{1}(x) + C_{2}'(x)y_{2}(x)=0\\
        & C_{1}'(x)y_{1}'(x) + C_{2}'(x)y_2'(x) = s(x)
    \end{cases} \implies\\
    & \begin{cases}
        & C_{1}'(x)x^{-2} + C_{2}'(x)x^{-5} = 0\\
        & -2C_{1}'(x)x^{-3}- 5 C_{2}'(x)x^{-6} = \frac{\ln (x)}{x^3 } 
    \end{cases} \implies\\
    & \implies \begin{cases}
        & C_{1}'(x) + C_{2}'(x)x^{-3} = 0\\
        & -2C_{1}'(x) - 5C_{2}'(x)x^{-3} = \ln (x) 
    \end{cases}\\
    & C_{1}'(x) = \frac{\begin{vmatrix} 0 & x^{-3}\\ \ln(x) & -5x^{-3}  \end{vmatrix}}{\begin{vmatrix} 1 & x^{-3}\\ -2 & -5x^{-3}   \end{vmatrix}} = \frac{\frac{-\ln (x)}{x^{3} }}{\frac{-5}{x^3 } + \frac{2}{x^3 }} = \frac{1}{3}\ln (x) \implies\\
    & \implies C_{1}(x) = \frac{1}{3} \int  \ln (x)dx = \begin{cases}
    & u = \ln (x) \implies du = \frac{1}{x}dx\\
    & dv = dx \implies v = x
    \end{cases} =\\
    & \frac{1}{3}\left( x\ln (x) - \int x \frac{1}{x} dx \right) = \frac{1}{3} x\ln (x) - x + C_{1}\\
    & C_{2}'(x) = \frac{\begin{vmatrix} 1 & 0\\ -2 \ln (x)\end{vmatrix}}{\begin{vmatrix} 1 & x^{-3}\\ -2 & -5x^{-3}   \end{vmatrix}} = \frac{\ln (x)}{\frac{-5}{x^3 } + \frac{2}{x^3 } } = -\frac{x^3 }{3}\ln (x)\implies\\
    & \implies C_{2}(x) = -\frac{1}{3}\int x^3 \ln (x)dx = \begin{cases} & u = \ln(x) \implies du = \frac{1}{x}dx\\ & dv = x^3 dx \implies v = \frac{x^{4} }{4} \end{cases} =\\
    & = -\frac{1}{3}\left( \frac{x^{4} }{4}\ln (x) - \int \frac{1}{x} \frac{x^{4} }{4}dx \right) = -\frac{1}{12}\left( x^{4}\ln (x) - \frac{x^{4} }{4}  \right) + C_{2}\\
    & y = C_{1}(x) x^{-2} + C_{2}(x)x^{-5} =\\
    & = \left( \frac{1}{3}x\ln (x)- \frac{1}{3}x + C_{1} \right) x^{-2} + \left( -\frac{1}{12}x^{4} \ln (x) + \frac{1}{48}x^{4} + C_{2}   \right) x^{-5} =\\
    & = C_{1}x^{-2} + C_{2}x^{-5} + \frac{1}{4x}\ln (x) - \frac{5}{16x}\\
    & SGEH \equiv C_{1}x^{-2} + C_{2}x^{-5}\\
    & SPEC \equiv \frac{1}{4x}\ln (x) - \frac{5}{16x}
\end{split}
$$
