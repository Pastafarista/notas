---
id: 1710093096-posicin-relativa-de-tres-planos
aliases:
  - Posición relativa de tres planos
tags:
  - álgebra
---

# Posición relativa de tres planos

Dados los [[1710070957-planos-en-r|planos]] $\pi_1=a_1x+b_1y+c_1z+d_1=0$, $\pi_2 = a_2x + b_2y + c_2z + d_2 = 0$ y $\pi_3 = a_3x + b_3y + c_3z + d_3 = 0$

Si $M$ es la [[1708971486-matriz|matriz]] de los coeficientes y $M^{*}$ es la matriz ampliada:

$$
\begin{split}
    & \text{Si } rang(M) = rang(M^{*}) = 3 \Rightarrow \pi_1, \pi_2 \text{ y } \pi_3 \text{ se cortan en un punto}\\
    & \text{Si } rang(M) = rang(M^{*}) = 2 \Rightarrow \pi_1, \pi_2 \text{ y } \pi_3 \text{ se cortan en una recta}\\
    & \text{Si } rang(M) = rang(M^{*}) = 1 \Rightarrow \pi_1, \pi_2 \text{ y } \pi_3 \text{ son planos coincidentes}\\
    & \text{Si } rang(M) = 1 \text{ y } rang(M^{*}) = 2 \Rightarrow \pi_1, \pi_2 \text{ y } \pi_3 \text{ son planos paralelos o hay dos coincidentes y un tercero paralelo a ellos}\\
    & \text{Si } rang(M)=2 \text{ y } rang(M^{*})=3 \Rightarrow \pi_1, \pi_2 \text{ y } \pi_3 \text{ son 3 planos que se cortan dos a dos o son dos planos paralelos y uno que se corta con ellos}
\end{split}
$$
