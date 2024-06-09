---
id: 1712761188-aritmtica-en-coma-flotante
aliases:
  - Aritmética en coma flotante
tags:
  - cálculo-numérico
---

# Aritmética en coma flotante

Como consecuencia de la representación en [[1712760222-errores-en-la-representacin-de-los-nmeros-reales-en-el-ordenador|coma flotante]], la aritmética del ordenador es diferente de la 'verdadera'. Veamos algunos ejemplos.

## Resta

Consideremos un sistema rudimentario de mantisa de dos cifras en base 10. 

- En este sistema la mejor aproximación del número $\frac{15\pi }{34}$ es $1.4 \times 10^{0}$ (con error aproximado del $1 \%$)
- El número $\sqrt{2}$ se aproxima a $1.4 \times 10^{0} $

Si en el ordenador restamos estos dos números obtenemos $0$, cantidad errónea por completo a la aproximación $\frac{15\pi }{34} - \sqrt{2} \approx 0.0282$ (que en el sistema de dos cifras se podría aproximar a $2.8 \times 10^{-2}$ con un error del $1 \%$)

En general, al restar dos números de coma flotante que sean aproximaciones de número muy cercanos, se obtiene un error muy grande. Conviene entonces formular los algoritmos de manera que se eviten sustraer cantidades casi iguales.

## Falta de asociatividad en la aritmética en coma flotante

- Si tenemos $x = 10^{20}, \; y = -10^{20} \; \text{y} \; z=1$, entonces en el ordenador se cumple que $(x+y)+z = 1$ y $x+(y+z) = 0$.

## Ejemplo en python

Consideremos $a = 1, \; b=12345678987, \; c=1$. Entonces para calcular $ax^2 + bx + c = 0$ en python obtenemos:

$$
    x_1 = \frac{-b - \sqrt{b^2 - 4ac}}{2a} \approx -12345678986, \quad \quad x_2 = \frac{-b + \sqrt{b^2 - 4ac}}{2a} \approx 0
$$

Sabemos que de esas fórmulas se sabe que:

$$
y_1 = \frac{2c}{-b - \sqrt{b^2 - 4ac}} \approx 0, \quad \quad y_2 = \frac{2c}{-b + \sqrt{b^2 - 4ac}} = \text{ error}
$$

El error ocurre ya que por el límite de la mantisa, el valor de $-b + \sqrt{b^2 - 4ac}$ es aproximadamente $0$.

