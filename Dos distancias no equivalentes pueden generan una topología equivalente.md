#topología
## ¿Pueden dos [[Métrica]]'s generar la misma [[Topología]] sin que se cumple que sean [[Distancia equivalente]]?

- $d_1(X,Y)=|X - Y|$
- $d_2(X,Y)= \arctan |X - Y|$

Estas dos métricas no son equivalentes ya que no se cumple

$c |X - Y| \leq \arctan |X - Y| \leq \pi$

debido a que

$x = \frac{2\pi}{C}, \; y = 0$ lo incumple porque $C \cdot \frac{2\pi}{C} = 2\pi < \pi$ ¡¡¡Contradicción!!!

Y aunque no sean equivalentes, generan la misma topología ya que para cualquier bola abierta que cojamos podemos encontrar otra bola abierta dentro

$arctan(x - \epsilon) \geq x \implies arctan(x - \epsilon) = x - a, \; a > 0$

$arctan(x + \epsilon) \leq x \implies arctan(x + \epsilon) = x + b, \; b > 0$

Bolas de la $arctan$ = $(x-a, x+b)$
Bolas de $|x - y|$ = $(x - \epsilon, x + \epsilon)$

Hay que demostrar que en cualquier bola de la [[Topología inducida por distancia]] de la $arctan$ cabe en las bolas de la

![[Dos distancias no equivalentes generan una topología equivalente 2023-11-01 21.21.20.excalidraw]]
