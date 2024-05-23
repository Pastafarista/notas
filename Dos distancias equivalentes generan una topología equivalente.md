#topología 

**Dos [[Distancia equivalente|distancias equivalentes]] generan una [[topología]] equivalente**

- Dos distancias $d_1,d_2$ son equivalentes si se cumple que $$C_1 \cdot d_1 \leq d_2 \leq C_2 \cdot d_1$$
- Si son equivalentes $\forall B_{\epsilon,d_2}(x) \exists B_{\epsilon \cdot C_1, d_1}(x):B_{\epsilon \cdot C_2, d_1}(x) \subset B_{\epsilon,d_2}(x)$

![[Dos distancias equivalentes generan una topología equivalente 2023-11-06 12.07.46.excalidraw]]

- En la [[topología inducida por distancia]], los [[Conjunto abierto|conjuntos abiertos]] serán aquellos cuyos puntos tendrán al menos una [[bola abierta]] completamente dentro del conjunto
- Si tenemos el conjunto $U$ abierto en la topología inducida por $d_2$ tal que $\forall x \in U$ $\exists \epsilon > 0 : B_{\epsilon,d_2}(x) \subset U$ entonces también $B_{\epsilon \cdot C_1, d_1}(x) \subset B_{\epsilon,d_2}(x) \subset U$