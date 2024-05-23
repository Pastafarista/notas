#ejercicios-estadística 

Examen extraordinario INSO3W

## En una asignatura universitaria asisten a clase 90 de los 150 alumnos matriculados. Se sabe que aprueban la asignatura el 90% de los alumnos que asisten a clase y el 30% de los que no asisten.


- Primero definiremos nuestros [[sucesos]]
	
	$A \equiv \text{Probabilidad de que un alumno elegido al azar asista a clase}$
	$B \equiv \text{Probabilidad de que un alumno elegido al azar apruebe la asignatura}$

- Para calcular $P(A)$ usaremos la [[Definición clásica probabilidad|definición clásica de probabilidad]]
$$P(A)=\frac{90}{150}=0.6$$

- Dibujemos el diagrama de árbol

![[Ejercicio 2 Probabilidades 2023-11-21 20.22.29.excalidraw]]

1. Calcular la probabilidad de que un alumno elegido al azar no haya asistido a clase y haya aprobado

- Nos piden $P(\overline{A} \cap B)$, sabemos por la [[probabilidad condicionada]] que 
$$P(\overline{A}\cap B) = P(B \cap \overline{A}) = P(B/\overline{A}) \cdot P(\overline{A}) = 0.3 \cdot 0.4 = 0,12$$

2. ¿Qué porcentaje de alumnos suspensos no habían asistido a clase?

- Nos piden $P(\overline{A}/B)$, para calcularlo usaremos el [[teorema de Bayes]]
$$P(\overline{A}/B) = \frac{P(B/\overline{A}) \cdot P(\overline{A})}{P(B)} = \frac{0.3 \cdot 0.4}{0.66}=0.1818$$
- Por lo tanto un $18.18\%$ de los alumnos suspensos no habían asistido a clase

3. ¿Cuántos alumnos han aprobado la asignatura?

- Calculamos $P(B)$ usando el [[teorema de probabilidad total]]
$$P(B) =\sum_{i=1}^{n}P(B/A_i) \cdot P(A_i) = (0.9 \cdot 0.6) + (0.4 \cdot0.3) = 0.66$$

- Ahora si multiplicamos $P(B)$ por el tamaño de la muestra $(150)$
$$\text{Personas que no han asistido a clase}=0.66 \cdot 150 = 99 \text{ personas}$$

Ahora con todos estos datos podemos ver que hemos hecho bien el ejercicio comprobando que
$$P(\overline{A} \cap B) = P(\overline{A}/B)\cdot P(B) = 0.1818 \cdot 0.66 = 0.1199 \approx 0.12$$