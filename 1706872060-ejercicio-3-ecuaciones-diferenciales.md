---
id: 1706872060-ejercicio-3-ecuaciones-diferenciales
aliases:
  - Ejercicio 3 ecuaciones diferenciales
  - Comprueba que las funciones dadas son solución de sus correspondientes ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Comprueba que las funciones dadas son [[1707058998-solucin-de-una-ecuacin-diferencial-ordinaria|solución]] de sus correspondientes [[1706869334-ecuacin-diferencial|ecuaciones diferenciales]]

1. ${y = x + e^{-x}}$ para la ecuación ${y' + y = x + 1}$

$$
\begin{split}
    & y'=1-e^{-x} \\
    & y' + y = x + 1 \Longleftrightarrow 1-e^{-x} + x + e^{-x} = x + 1 \Longleftrightarrow 1+x = x+1\\
\end{split}
$$

2. ${y = 2e^{3x} - 5e^{4x}}$ para la ecuación ${y'' - 7y' + 12y = 0}$

$$
\begin{split}
    & y' = 6e^{3x} - 20e^{4x} \\
    & y'' = 18e^{3x} - 80e^{4x} \\
    & y'' - 7y' + 12y = \\
    & 18e^{3x} - 80e^{4x} - 42e^{3x} + 140e^{4x} + 24e^{3x} - 60e^{4x} = \\
    & = (18e^{3x} - 42e^{3x} + 24e^{3x}) + (140e^{4x} - 80e^{4x} - 60e^{4x}) = 0 
\end{split}
$$

3. ${y = e^x(2x + 1)}$ para la ecuación ${y'' = 2y' - y}$

$$
\begin{split}
    & y' = e^x(2x + 1) + 2e^x \\
    & y'' = e^x(2x + 1) + 2e^x + 2e^x(2x + 1) + 2e^x \\
    & 2y' - y = 2(e^x(2x + 1) + 2e^x) - e^x(2x + 1) =\\
    & = 2e^x(2x + 1) + 4e^x - e^x(2x + 1) =\\
    & = 2e^x(2x + 1) + 4e^x - 2e^x(2x + 1) = 4e^x = y'' = 2y' - y = 4e^x
\end{split}
$$

4. ${x(t) = sen(t) + cos(t)}$ para la ecuación ${xcos(t) + xsen(t) = 1}$

$$
\begin{split}
    & xcos(t) + xsen(t) = (sen(t) + cos(t))cos(t) + (sen(t) + cos(t))sen(t) =\\
    & = sen(t)cos(t) + cos^2(t) + sen^2(t) + sen(t)cos(t) =\\
    & = sen(t)cos(t) + 1 + sen(t)cos(t) = 1
\end{split}
$$
