---
id: 1716491727-dos-distancias-equivalentes-generan-una-topologa-equivalente
aliases:
 - Dos distancias equivalentes generan una topología equivalente
---

#topología 

**Dos [[1716491727-distancia-equivalente|distancias equivalentes]] generan una [[1716491728-topologa|Topología]] equivalente**

- Dos distancias $d_1,d_2$ son equivalentes si se cumple que $$C_1 \cdot d_1 \leq d_2 \leq C_2 \cdot d_1$$
- Si son equivalentes $\forall B_{\epsilon,d_2}(x) \exists B_{\epsilon \cdot C_1, d_1}(x):B_{\epsilon \cdot C_2, d_1}(x) \subset B_{\epsilon,d_2}(x)$

![[Dos distancias equivalentes generan una topología equivalente 2023-11-06 12.07.46.excalidraw]]

- En la [[1716491728-topologa-inducida-por-distancia|Topología inducida por distancia]], los [[1716491727-conjunto-abierto|conjuntos abiertos]] serán aquellos cuyos puntos tendrán al menos una [[1716491727-bola-abierta|Bola Abierta]] completamente dentro del conjunto
- Si tenemos el conjunto $U$ abierto en la topología inducida por $d_2$ tal que $\forall x \in U$ $\exists \epsilon > 0 : B_{\epsilon,d_2}(x) \subset U$ entonces también $B_{\epsilon \cdot C_1, d_1}(x) \subset B_{\epsilon,d_2}(x) \subset U$