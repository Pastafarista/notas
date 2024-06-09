---
id: 1712760222-errores-en-la-representacin-de-los-nmeros-reales-en-el-ordenador
aliases:
  - Errores en la representación de los números reales en el ordenador
  - Coma flotante
tags:
  - cálculo-numérico
---

# Errores en la representación de los números reales en el ordenador

La forma más sencilla de manejar un número real es por su desarrollo decimal.

$$
\frac{3}{8} = 0.375, \;\; -\frac{11}{5} = -2.2
$$

Si el desarrollo es infinito se puede truncar o redondear.

$$
\frac{1}{3} = 0.3333 \;\; \pi = 3.14159
$$

Pero el formato decimal es muy incomodo para números muy grandes o muy pequeños.

$$
\begin{split}
    & \text{El número de avogadro es } 602213670000000000000000\\

    & \text{La masa de un protón en gramos es } 0.0000000000000000000000000000016726\ldots 
\end{split}
$$

En estos casos se usa la notación científica.

$$
1.6726 \times 10^{-27}
$$

Los ordenadores usan internamente esta representación, que se llama de punto flotante.

## Formato de punto flotante

Un problema del formato científico es que tanto $60.221367 \times 10^{22}$ como $0.60221367 \times 10^{24}$ son reprentaciones del número de Avogadro. Para evitar esto se usa un formato normalizado, en el que si el nñumero no es cero, su primera cifra no nula aparezca inmediatamente a la izquierda del punto decimal.

Con esta normalización, el número de Avogadro se representa como $6.0221367 \times 10^{23}$.

La parte $6.0221367$ se llama mantisa y el exponente $23$.

El número $0$ es especial ya que para él la mantisa y el exponente no están definidos.

## Errores en la representación

Para representar un número real en coma flotante tendríamos que tener una mantisa infinita, lo que no es posible. Por lo tanto, siempre existirá un error en la representación.
