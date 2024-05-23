---
id: 1716491727-ejercicio-1-espacios-conexos
aliases:
 - Ejercicio 1 Espacios Conexos
---

#topología  

## Considera $A = \{ [0;1] \times \{ \frac{1}{n} \}, n \in \mathbb{N}\} \cup \{0\} \times (0,1)$ en $\mathbb{R}^2$

1. Dibújalo

![[Ejercicio 1 Espacios Conexos 2023-12-20 10.43.09.excalidraw]]

2. Buscar su [[1716491727-clausura|Clausura]]

Su clausura sería: $$\{[0,1] \times \{\frac{1}{n} \}, n \in \mathbb{N}\} \cup  \{ \{0\} \times [0,1] \} \cup \{[0,1] \times \{0\}\}$$
- Los puntos $(0,0)$ y $(0,1)$ son frontera y por eso los añadimos a la clausura, y el segmento $[0,1] \times 0$ también es frontera ya que los otros segmentos se aproximan pero nunca llegan a tocarlo y por lo tanto todo punto del segmento tendrá puntos de los otros que se aproximan en sus entornos

3. ¿Es [[1716491727-espacios-conexos|conexo]]?

No es conexo ya que podemos definir $$f(x) = \begin{cases} 
& 0 \;\;\; \text{ si } \; 0 \leq x \leq 1, \; y =1\\
& 1 \;\;\; \text{en caso contrario} \;\, 
\end{cases}$$

5. ¿Es [[1716491727-espacio-conexo-por-caminos|conexo por caminos]]?

No es conexo por caminos ya que no hay ningún camino que una $[0,1] \times \{1\}$ con $\{0\} \times (0,1)$