---
id: 1716663320-mtodo-del-desarrollo-de-taylor
aliases:
  - Método del desarrollo de Taylor
tags:
  - cálculo-numérico
---

# Método del desarrollo de Taylor

En general el método de desarrollo de Taylor pide:

1. Desarrollar en [[1716663342-polinomio-interpolador-de-taylor|Taylor]] las ordenadas $f(x_i)$. El punto en torno al cual se efectúa el desarrollo de Taylor puede ser uno de los nodos o cualquier otro punto que conduzca a simplificaciones en el cálculo; el punto medio $c=\frac{a+b}{2}$ del intervalo $[a,b]$ suele ser particularmente util.
2. Desarrollar en Taylor el integrando $f(x)$ en torno al mismo punto e integrar término a término el desarrollo.
3. Imponer que los términos de ambos desarrollos vayan coincidicendo hasta deonde sea posible.

En general, el [[1713866424-grado-de-exactitud|grado de exactitud]]de el método del desarrollo de Taylor es $\ge N$ para un polinomio de Taylor grado $N$.
