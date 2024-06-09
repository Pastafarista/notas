---
id: 1716491727-teorema-de-continuidad-y-convergencia
aliases:
 - Teorema de continuidad y convergencia
---

#topología

Sea $f:(X_1, d_1) \rightarrow (X_2, d_2)$ una función entre [[1716491727-espacio-mtrico|Espacio métrico]]'s la función $f$ es una [[1716491727-funcin-continua|Función continua]] en $x\in X$ si y sólo si para toda [[1716491727-sucesin-convergente|Sucesión convergente]] $x_n$ convergiendo a $x$ se cumple que $f(x_n)$ converge a $f(x)$

## Demostración:

$\implies$ Si es [[1716491727-funcin-continua|continua]], [[1716491727-sucesin-convergente|converge]]

- Si $f$ es continua en $x$ $\forall \epsilon > 0  \; \exists \delta > 0:f(B_{\delta}(x))\subset B_{\epsilon}(f(x))$
- La sucesión $x_n$ converge a $x$, por tanto a partir de algún momento todos los elementos estarán dentro de la [[1716491727-bola-abierta|bola]] $B_{\delta}(x)$. Pero su imagen está en $B_{\epsilon}(f(x))$. Esto significa que la imagen de la sucesión converge a $f(x)$ ya que existe la bola $B_\epsilon(f(x))$ la cual contiene a todos los $f(x_n)$  

![[Teorema de continuidad y convergencia 2023-11-02 18.08.39.excalidraw]]

$\impliedby$ Si [[1716491727-sucesin-convergente|converge]], es [[1716491727-funcin-continua|continua]]

- Supongamos lo contrario:
$$\exists \epsilon > 0 \; \forall \delta > 0:f(B_\delta(x))\not\subset B_\epsilon(f(x))$$
- Consideremos $\delta = \frac{1}{n}$ y una sucesión $x_n$ que converja a $x$ y cuyas imágenes $f(x_n)$ no estén en $B_\epsilon(f(x))$ 
- Como todos los puntos de la bola abierta $B_\delta$ no pueden estar dentro de una bola $B_{\epsilon}$ resulta que la sucesión $f(x_n)$ no puede converger a $f(x)$. ¡¡¡Contradicción!!!

![[Teorema de continuidad y convergencia 2023-11-02 18.16.20.excalidraw]]