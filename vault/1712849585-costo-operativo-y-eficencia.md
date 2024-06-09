---
id: 1712849585-costo-operativo-y-eficencia
aliases:
  - Costo operativo y eficencia
tags:
  - cálculo-numérico
---

# Costo operativo y eficiencia

Nos quedaremos con el método que dando [[1707819341-errores|errores]] dentro de unos límites predeterminados, necesite el menor trabajo.

## Ejemplo con el método de Horner

Supongamos que queremos evaluar el polinomio $p(x) = a_0 + a_{1}x + a_{2}x^2 + a_{3}x^3 + a_{4}x^{4}$

El método convencional para calcular por ejemplo $p(2)$ sería:

```python
def p(x):
    x_2 = x*x
    x_3 = x*x_2
    x_4 = x*x_3

    return a_0 + a_1*x + a_2*x_2 + a_3*x_3 + a_4*x_4
```

En total se necesitan 7 multiplicaciones y 4 sumas.

El método de Horner consiste en reescribir el polinomio de la siguiente manera:

$$
p(x) = a_0 + x(a_1 + x(a_2 + x(a_3 + x(a_4))))
$$

De esta manera, para evaluar $p(2)$ se necesitan 4 multiplicaciones y 4 sumas.

```python
def p(x):
    return a_0 + x*(a_1 + x*(a_2 + x*(a_3 + x*a_4)))
```

En general vemos que para el método convencional necesitamos $N$ sumas/restas y $2N - 1$, y con el método de Horner serían $N$ sumas/restas y $N$ multiplicaciones