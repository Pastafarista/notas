---
id: 1715962394-teorema-fundamental-de-la-aritmtica
aliases:
  - Teorema fundamental de la aritmética
tags:
  - matemática-discreta-II
---

# Teorema fundamental de la aritmética

## Enunciado

- Cualquier número entero positivo tiene una única descomposición en números primos finitos.

$$
n = p_{1}^{\alpha_{1}}p_{2}^{\alpha_{2}} \ldots p_{k}^{\alpha_{k}} 
$$

## Demostración

- Si nuestro número $n$ no tiene divisores distintos de $n$ y $1$, entonces es primo y ya está descompuesto.
- Si tiene algún divisor, lo dividimos por él. El nuevo número obtenido es menor que el original, por tanto, el proceso de la división será finito, y obtendremos todos los divisores primos.

Para demostrar la unicidad, usaremos el **descenso infinito**

- De todos los números que tienen dos descomposiciones eligiéremos el más pequeño $n$.
- En las descomposiciones los factores primos son distintos (¿por qué?)
- Porque dividiéndolo entre un factor común, obtendríamos otro número con dos descomposiciones distintas menor que el anterior
- Entonces, $n=p\cdot P = q\cdot Q$, donde $P \neq q\cdot k$ y $Q \neq p\cdot k$. Construiremos ahora un número más pequeño que $n$ con la misma propiedad
- En nuevo número será $n' = n - pq$
- $n' = p(P - q)$, donde $P-q = q \cdot k$ y $n' = q(Q - p)$, donde $Q-p = p \cdot k$
- El nuevo número tiene dos descomposiciones y es menor que $n$. Contradicción. Por tanto, no puede haber dos descomposiciones distintas.
