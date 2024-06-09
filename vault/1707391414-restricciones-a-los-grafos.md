---
id: 1707391414-restricciones-a-los-grafos
aliases:
  - Restricciones a los grafos
  - Demostrar que si un grafo plano tiene al menos 2 aristas, se cumple
tags:
  - matemática-discreta-II
---

# Demostrar que si un [[1706978566-grafo-plano|grafo plano]] tiene al menos 2 aristas, se cumple

$$A \leq 3V-6$$

## Demostración

- Aplicando la [[1716491727-caracterstica-de-euler|característica de Euler]] $V - A + C = 2$, $A = V + C - 2$ ahora $2A \geq 3C, \; C \leq 2/3A,$ de ahí $A \leq V + \frac{2}{3}A - 2$

- Con esto ya demostramos que $K_5$ no es plano

