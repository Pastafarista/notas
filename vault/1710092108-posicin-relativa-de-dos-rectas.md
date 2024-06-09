---
id: 1710092108-posicin-relativa-de-dos-rectas
aliases:
  - Posición relativa de dos rectas
tags:
  - álgebra
---

# Posición relativa de dos rectas

Dadas dos [[1710070725-rectas-en-r|rectas]] $r_1$ y $r_2$ expresadas como la intersección de dos [[1710070957-planos-en-r|planos]] $\pi_1$ y $\pi_2$ y $\pi_3$ y $\pi_4$ respectivamente, si $M$ es la [[1708971486-matriz|matriz]] de los coeficientes de estos planos y $M^{*}$ es la matriz ampliada:

$$
\begin{split}
    & \text{Si } rang(M) = rang(M^{*}) = 2 \Rightarrow r_1 \text{ y } r_2 \text{ las rectas son coincidentes}\\
    & \text{Si } rang(M) = rang(M^{*}) = 3 \Rightarrow r_1 \text{ y } r_2 \text{ se cortan en un punto}\\
    & \text{Si } rang(M) = 2 \text{ y } rang(M^{*}) = 3 \Rightarrow r_1 \text{ y } r_2 \text{ son rectas paralelas}\\
    & \text{Si } rang(M) = 3 y rang(M^{*}) = 4 \Rightarrow r_1 \text{ y } r_2 \text{ se cruzan en el espacio}
\end{split}
$$
