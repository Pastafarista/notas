---
id: 1716491728-una-funcin-es-continua-si-y-slo-si-la-preimagen-de-un-conjunto-abierto-es-abierta
aliases:
 - Una función es continua si y sólo si la preimagen de un conjunto abierto es abierta
---

#topología 

$\text{Si } f(x):X \rightarrow Y \text{ es continua} \implies \text{la preimagen de un conjunto abierto es abierta}$

Primero escogemos un [[1716491727-conjunto-abierto|Conjunto abierto]] de las imágenes $U \subset Y$
Si $V=f^{-1}(U)$, tenemos que demostrar que $V$ es abierto

Supongamos lo contrario, que la preimagen de un [[1716491727-conjunto-abierto|Conjunto abierto]] es un no abierto ($V \text{ no abierto}$)

1. Como $V$ no es abierto, tendrá al menos un [[1716491727-punto-fronterizo|Punto fronterizo]] $x \in V$, tal que cualquier entorno suyo tendrá puntos dentro y fuera de $V$. Que no sea [[1716491727-conjunto-abierto|abierto]] implica que existe este $x$ ya que no se cumple para todos sus puntos que todos los entornos de estos están completamente dentro del conjunto.

2. Construiremos una sucesión de puntos $x_i$ que converja a $x$ con los $x_i$ fuera de $V$, sus imágenes $f(x_i)$ convergerán a $f(x) \in U$ por el [[1716491727-teorema-de-continuidad-y-convergencia|Teorema de continuidad y convergencia]], pero ninguno de estos $f(x_i) \notin U$ ya que $x_i \notin V$ (Porque es su preimagen). Entonces $f(x) \in Fr(U)$ ¡¡¡Contradicción!!! ya que $U$ es abierto 

![[Una función es continua si y sólo si la preimagen de un conjunto abierto es abierta 2023-10-31 11.46.23.excalidraw]]


$\text{ Si la preimagen del abierto } U \text{ es abierta}$ $\implies \text{ la función es continua}$

Queremos demostrar que la función es continua en el punto x, empezamos eligiendo a la derecha una [[1716491727-bola-abierta|bola abierta]] centrada en $f(x)$, su preimagen $f^-1(x)$ es abierta y contiene a $x$

Entorno al punto $x$ hay una [[1716491727-bola-abierta|bola abierta]] dentro de la preimagen ($f^{-1}(B(f(x)))$), la imagen de esta bola está dentro de $B(f(x))$, por tanto se cumple que es una [[1716491727-funcin-continua|función continua]]

![[Una función es continua si y sólo si la preimagen de un conjunto abierto es abierta 2023-10-31 11.50.07.excalidraw]]