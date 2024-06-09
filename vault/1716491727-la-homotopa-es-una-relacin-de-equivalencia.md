---
id: 1716491727-la-homotopa-es-una-relacin-de-equivalencia
aliases:
 - La homotopía es una relación de equivalencia
---

---
id: La homotopía es una relación de equivalencia
aliases:
  - La homotopía es una Relación de equivalencia.
tags: []
---

#topología 

## La [[1716491727-homotopa|Homotopía]] es una [[1716491727-relacin-de-equivalencia|Relación de equivalencia]].

1. $\alpha \sim \alpha$

- tenemos que demostrar que existe una aplicación que convierte un *"paseo"* en si mismo

$$h(t,s) = \alpha(t)$$

2. $\alpha \sim \beta \Longleftrightarrow \beta \sim \alpha$

- Si $h:h(t,0)=\alpha(t), h(t,1) = \beta(t)$. ¿Cómo definimos $h^{-1}:\beta \rightarrow \alpha$?

- Queremos que $h^{-1}(t,1) = \alpha(t)$ y $h^{-1}(t,0) = \beta(t)$

$$h^{-1}(t,x) = h(t,1-x)$$

3. $\alpha \sim \beta$ y $\beta \sim \gamma \Longleftrightarrow \alpha \sim \gamma$

- Si $h_1(t,0) = \alpha(t), \; h_1(t,1) = \beta(t), \; h_2(t,0) = \beta(t), \; h_2(t,1) = \gamma(t)$. ¿Cómo definimos $h_3:\alpha \rightarrow \gamma$?

$$h_3(t,s) = \begin{cases}
	& h_1(t,2s) \;\;\; 0 \leq s \leq \frac{1}{2}\\
	& h_2(t,2s-1) \;\;\; \frac{1}{2} \leq s \leq 1
\end{cases}$$
