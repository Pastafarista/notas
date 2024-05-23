---
id: 1716491727-la-mtrica-integral-y-la-del-supremo-no-generan-los-mismos-abiertos
aliases:
 - La métrica integral y la del supremo no generan los mismos abiertos
---


Contraejemplo: $U = \{f(x) > 0\}$ es un abierto en la [[1716491727-mtrica-del-supremo|Métrica del supremo]] y no en la [[1716491727-mtrica-integral|Métrica Integral]]

## Demostrar que no son [[1716491727-distancia-equivalente|Distancia equivalente]]

- Tenemos que construir ejemplos de funciones $f,g$ tales que 
$$\forall c < 1 \; \exists f,g : cd_0(f,g) > d_1(f,g) < d_0(f,g)$$

$$ \text{Sea la función } f(x) = 0 \text{ y la función } g(x) = \begin{cases} & 1 \text{ si } x \in [0, \frac{1}{c+1}]\\ & 0 \text{ si } x \notin [0, \frac{1}{c+1}]\end{cases}$$

Calcula $cd_0(f,g)$(la [[1716491727-mtrica-del-supremo|Métrica del supremo]]) y $d_1(f,g)$(la [[1716491727-mtrica-integral|Métrica Integral]])