---
id: 1716491727-ejercicio-grupo-fundamental
aliases:
 - Ejercicio grupo fundamental
---

#topología 

## Averiguar el [[1716491727-grupo-fundamental|Grupo fundamental]] de $\mathbb{R}^3 \setminus S^1$

- Los [[1716491727-lazo|lazos]] no son [[1716491727-lazos-equivalentes|equivalentes]] si uno se engancha a la circunferencia y el otro no
- Tampoco si dan una cantidad de vueltas distintas
- $\pi_1 (\mathbb{R}^3 \setminus S^1,x_0) \sim \mathbb{Z}$

## Averiguar el grupo fundamental del toro

- Sabemos que el toro se forma con $S^1 \times S^1$, para nuestra suerte el grupo fundamental será

$$\pi_1(S^1 \times S^1) = \pi_1(S^1) \times \pi_1(S^1) = \mathbb{Z} \times \mathbb{Z}$$

## Calcular el grupo fundamental del cilindro $S^1 \times [0;1]$

- Sabiendo que el grupo fundamental del segmento es el grupo trivial $\{e\}:$
$$\pi_1(S^1 \times [0,1]) = \mathbb{Z} \times \{e\} = \mathbb{Z}$$

## Calcular el grupo fundamental del cono

- El cono sin la base es homeomorfo al plano, por lo tanto $$\pi_1(C) = \{e\}$$
- Si consideramos también la base, como el cono con base es homeomorfo a una esfera:

  $\pi_1 (C) = \{e\}$

## Averiguar el grupo fundamental de $S^2 \setminus \{0,1\}$

- Como $C$ es [[1716491727-conjuntos-homeomorfos|homeomorfo]] al cilindro, entonces:

$$\pi_1 (C) = \mathbb{Z}$$

## Calcular los grupos fundamentales

1. $\pi_1(\mathbb{R}^2 \setminus \{(0,0)\}) = \mathbb{Z}$

- Como el plano sin un punto es [[1716491727-conjuntos-homeomorfos|homeomorfo]] al cilindro entonces sus grupos fundamentales serán los mismos

2. $\pi_1(\mathbb{R}^2 \setminus \{(0,0), (1,0)\})$

- Es lo que vimos en la pizarra con los lazos y los dos puntos
- El grupo fundamental es $\mathbb{Z} \ast \mathbb{Z}$

3. $\pi_1 (\mathbb{R}^2 \setminus \{(0,0), (1,0), (2,0)\})$

- Podemos formar este conjunto como la unión de el semiplano si un punto con el otro semiplano sin un punto y con la franja sin un punto, usando el [[1716491727-teorema-de-seifertvan-kampen|Teorema de Seifert-van Kampen]]:

$$\pi_1 (U_1 \cup U_2  \cup U_3) = \mathbb{Z} \ast \mathbb{Z} \ast \mathbb{Z}$$