#topología 

## ¿Cuántos elementos tiene una [[Bola Abierta|bola]] de radio 1 en torno a palabra "mola"?

- Con la [[Métrica de Hamming]]

1. Si es una [[Bola Abierta]]

$B_1(\text{"mola"}) = \{y \in X : d(\text{"mola"}, y) < 1\}$

Como se trata de la [[Métrica de Hamming]], $d(\text{"mola"},y) < 1 \Longleftrightarrow d(\text{"mola"}, y) = 0$

Esto solo se cumple cuando las dos cadenas son iguales, por lo que en la [[Bola Abierta]] de radio 1 en la distancia hamming centrado en "mola" solo está el elemento "mola"

2. Si es una [[Bola Cerrada]]

$\overline{B_{1}(\text{"mola"})}=\{y \in X:d(\text{"mola"}, y) \leq 1\}$

$d(\text{"mola"},y)=0 \Longleftrightarrow y = \text{"mola"}$

Con $d(\text{"mola"},y) = 1$ tenemos $(27 \text{ letras} - 1) \cdot 4 = 104 \text{ casos posibles}$

Por lo que la [[Bola Cerrada]] en total tendría 105 elementos

- Con la [[Métrica de Levensthein]]

1. Si es una [[Bola Abierta]] tendríamos un solo elemento como en la [[Métrica]] anterior.

2. Si es una [[Bola Cerrada]]

Con $d(\text{"mola"},y)=1$ tendríamos los 105 casos anteriores más los casos de borradas que se nos quedarían en $26 \cdot 6 + 1= 157 \text{ casos}$
Si por último si le añadimos los casos de inserciones tenemos $157 + 4 = 161 \text{ casos totales}$

Por lo que la [[Bola Cerrada]] en total tendríamos $161$ elementos


