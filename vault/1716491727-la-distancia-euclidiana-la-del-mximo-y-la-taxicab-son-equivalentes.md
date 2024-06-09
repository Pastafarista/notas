---
id: 1716491727-la-distancia-euclidiana-la-del-mximo-y-la-taxicab-son-equivalentes
aliases:
 - La distancia euclidiana, la del máximo y la taxicab son equivalentes
---

#topología 


## La [[1716491727-distancia-euclidiana|Distancia Euclidiana]] es [[1716491727-distancia-equivalente|equivalente]] a la [[1716491727-distancia-taxicab|Taxicab]]

$d_\epsilon = \sqrt{(x_1 - y_1)^2 + (x_2 - y_2)^2}$
$d_M = |x_1 - y_1| + |x_2 - y_2|$

$C \cdot d_M \leq d_\epsilon \leq c \cdot d_M$

1. $d_M \geq d_\epsilon$

$$\begin{split}
& \sqrt{(x_1 - y_1)^2 + (x_2 - y_2)^2} \leq |x_1 - y_1| + |x_2 - y_2| \Longleftrightarrow \\
& \Longleftrightarrow (x_1 - y_1)^2 + (x_2 - y_2)^2 \leq (x_1 - y_1)^2 + (x_2 - y_2)^2 + 2|x_1 - y_1|\cdot|x_2 - y_2| \Longleftrightarrow \\
& \Longleftrightarrow 2|x_1 - y_1| \cdot |x_2 - y_2| \geq 0
\end{split}$$

2. $\frac{d_M}{\sqrt{2}} \leq d_\epsilon$ 
$$\begin{split}
& \frac{|x_1 - y_1|+|x_2 - y_2|}{\sqrt{2}} \leq \sqrt{(x_1 - y_1)^2 + (x_2 - y_2)^2} \Longleftrightarrow \\
& \frac{(x_1 - y_1)^2 + (x_2 - y_2)^2 + 2 |x_1 - y_1| \cdot |x_2 - y_2|}{2} \leq (x_1 - y_1)^2 + (x_2 - y_2)^2 \Longleftrightarrow \\
& (x_1 - y_1)^2 + (x_2 - y_2)^2 + 2 |x_1 - y_1| \cdot |x_2 - y_2| \leq 2\cdot(x_1 - y_1)^2 + 2 \cdot (x_2 - y_2)^2 \Longleftrightarrow\\
& (x_1 - y_1)^2 + (x_2 - y_2)^2 - 2 |x_1 - y_1| \cdot |x_2 - y_2| \geq 0 \Longleftrightarrow \\
& (|x_1 - y_1| - |x_2 - y_2|)^2 \geq 0


\end{split}$$


## La [[1716491727-distancia-mximo|Distancia Máximo]] es [[1716491727-distancia-equivalente|Distancia equivalente]] a la [[1716491727-distancia-euclidiana|Distancia Euclidiana]] en espacios finitos:

- Supongamos un espacio de $k$ dimensiones de tal forma que $d_{max}(a,b)=max(|a_1 - b_1|, |a_2 - b_2|, ..., |a_n -b_n|) = |a_n - b_n|$

- $d_{\epsilon}(A,B)= \sqrt{(a_1 - b_1)^2 + (a_2 + b_2)^2 + ... (a_n + b_n)^2} \leq \sqrt{(a_n - b_n)^2 + (a_n - b_n)^2 + ... + (a_n - b_n)^2} = \sqrt{K \cdot (a_n - b_n)^2} =$ $=\sqrt{K} \cdot d_{max}(A,B)$

- $d_{MAX} = \sqrt{(a_n - b_n)^2} \leq \sqrt{(a_1 - b_1)^2 + (a_2 + b_2)^2 + ... (a_n + b_n)^2} = d_\epsilon(A,B)$

- $\sqrt{K} d_{MAX} \geq d_{\epsilon} \implies d_{MAX} \geq \frac{d_{\epsilon}}{\sqrt{K}}$
- $\frac{d_{\epsilon}}{\sqrt{K}} \leq d_{MAX} \leq d_{\epsilon}$

## La [[1716491727-distancia-mximo|Distancia Máximo]] no es [[1716491727-distancia-equivalente|Distancia equivalente]] a la [[1716491727-distancia-euclidiana|Distancia Euclidiana]] en espacios infinitos:

$\vec{V} = (1,1,...,1)$ $d_{max}=1$ $d_{\epsilon}=\sqrt{1^2 + 1^2 + ... + 1^2}=\infty$

- Como vemos no pueden ser equivalentes ya que nunca se cumplirían las desigualdades

