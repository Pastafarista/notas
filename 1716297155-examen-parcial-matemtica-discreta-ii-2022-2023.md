---
id: 1716297155-examen-parcial-matemtica-discreta-ii-2022-2023
aliases:
  - Examen parcial matemática discreta II 2022-2023
tags:
  - matemática-discreta-II
---

# Examen parcial matemática discreta II 2022-2023

1. Sabemos que $6|m,8|m,4|n,3|n$. ¿Es verdad que?

a) $48|m$

Sabemos que $m$ tiene como múltiplos a $6$ y $8$, lo que implica que tiene como factores $2^3$ y $3$. Por ende, tiene como factor $2^3\cdot 3 = 24$. La conclusión por lo tanto es **falsa**:

$$
\begin{split}
    & 6 | 24\\
    & 8 | 24\\
    & 48 \nmid 24\\
\end{split}
$$

b) $12|n$

En este caso si que se cumplirá la afirmación, ya que $n$ tiene como múltiplos a $4$ y $3$, lo que implica que tiene como factores $2^2$ y $3$. Por ende, tiene como factor $2^2\cdot 3 = 12$. La conclusión por lo tanto es **verdadera**.

c) $4|(m+n)$

Sabemos que $m = 24k_{1}$ y que $n=12k_{2}$, por lo tanto operando vemos que es **verdadera**:

$$
\begin{split}
    & m + n = 24k_{1} + 12k_{2} = 4(6k_{1} + 3k_{2}) = 4k_{3} \implies 4 | (m + n)
\end{split}
$$

d) $12 | (m+n)$

También es **verdadera**:

$$
\begin{split}
    & m + n = 24k_{1} + 12k_{2} = 12(2k_{1} + k_{2}) = 12k_{3} \implies 12 | (m + n)
\end{split}
$$

e) $288|mn$

Si operamos veremos que es **verdadera**:

$$
\begin{split}
    & mn = 24k_{1} \cdot 12k_{2} = 288k_{1}k_{2} = 288k_{3} \implies 288 | mn
\end{split}
$$

2. ¿Cuántos divisores tiene el número $7^3\cdot 13^{4} \cdot 25^{5}$?

Primero reescribiremos el número para que solo tenga factores primos:

$$
7^3\cdot 13^{4} \cdot 25^{5} = 7^3\cdot 13^{4} \cdot 5^{10}
$$

Por lo tanto el número de divisores será:

$$
(3+1)(4+1)(10+1) = 4\cdot 5\cdot 11 = 220
$$

Esto se debe a que por cada factor tenemos el caso de cada potencia, contando la potencia $0$ que es 1.

3. Calcula $\phi(495)$

Si descomponemos en factores primos:

$$
\phi(495) = \phi(11)\phi(5)\phi(3^2)
$$

Luego es sencillo calcularlo, ya que para los de potencia $1$ el resultado es $p-1$ y para los de potencia $n$ el resultado es $p^{n-1}(p-1)$:

$$
\begin{split}
    & \phi(11) = 11 - 1 = 10\\
    & \phi(5) = 5 - 1 = 4\\
    & \phi(3^2) = 3^{2-1}(3-1) = 6
\end{split}
$$

Por lo tanto:

$$
\phi(495) = 10\cdot 4\cdot 6 = 240
$$

4. Calcula

a) $2223\cdot 2224\cdot 2225 + 2221^{101104} \mod 11$

$$
\begin{split}
	& (2222+1)(2222+2)(2222+3)+(2222-1)^{101104} \mod 11 \equiv\\
	& 1 \cdot 2 \cdot 3 + (-1)^{101104} \mod 11 \equiv 6 + 1 \mod 11 \equiv\\
	& 7 \mod 11
\end{split}
$$

b) $239^{217} \mod 37$

$$
\begin{split}
	& 239^{217} \mod 37 = 239 \cdot 239^{216} \mod 37 = 239 \cdot \left(239^{36}\right)^{6} \mod 37 =\\
	& 239 \cdot 1^6 \mod 37 = 239 \mod 37 =\\
	& 17 \mod 37
\end{split}
$$

c) $351^{302} \mod 125$

Primero veremos si 351 y 125 son coprimos
$$
(351,125) = (125,101) = (101, 24) = (24,5) = (5,4) = (4,1) = 1
$$

Sabemos que $\phi(125)= \phi(5^3) = 5^2(5-1) = 100$

Gracias que lo son podemos aplicar la generalización del teorema de Fermat:

$$
\begin{split}
	& 351^{302} \mod 125 =  351^2 \cdot \left(351^{100}\right)^3 \mod 125 =\\
	& 351^2 \mod 125 =\\
	& 76 \mod 125
\end{split}
$$

d) $191^{151413} \mod 96$

$$
\begin{split}
	& 191^{151413} \mod 96 = (192-1)^{151413} \mod 96 = (-1)^{151413} \mod 96 =\\
	& -1 \mod 96 =\\
	& 95 \mod 96
\end{split}
$$

5. Resuelve las ecuaciones y sistemas modulares:

a) $26x \equiv 3 \mod 37$

Calculamos la ecuación modular de $\frac{37}{26}$

$$
\begin{split}
	& \frac{37}{26} = 1 + \frac{11}{26} = 1 + \frac{1}{\frac{26}{11}} = 1 + \frac{1}{2 + \frac{4}{11}} =\\
    & = 1 + \frac{1}{2 + \frac{1}{\frac{11}{4}}} = 1 + \frac{1}{2 + \frac{1}{2 + \frac{3}{4}}} = 1 + \frac{1}{2 + \frac{1}{2 + \frac{1}{\frac{4}{3}}}} =\\
    & = 1 + \frac{1}{2 + \frac{1}{2 +\frac{1}{1 + \frac{1}{3}}}} = 
    [1;2,2,1,3]
\end{split}
$$

Nos quedamos con la ecuación sin el último término:

$$
\begin{split}
    & [1;2,2,1] = 1 + \frac{1}{2+\frac{1}{2+\frac{1}{1}}} = \frac{10}{7}
\end{split}
$$

Usando el denominador sabemos que $(-1)^{4}\cdot 10 \equiv 1 \mod 37$ (usamos 4 porque es el número de términos en la ecuación continua). Por lo tanto, multiplicamos por $3$:

$$
x = 3\cdot 10 = 30 \mod 37
$$

b)

$$
\begin{cases}
    3x \equiv 7 \mod 11\\
    2x + 2 \equiv 6 \mod 7 \iff 2x \equiv 4 \mod 7\\
    5x \equiv 4 \mod 9
\end{cases}
$$

Calculamos las $M_i$:

$$
\begin{split}
    & M_{1} = 7*9 = 63 \equiv 8 \mod 11\\
    & M_{2} = 11*9 = 99 \equiv 1 \mod 7\\
    & M_{3} = 11*7 = 77 \equiv 5 \mod 9
\end{split}
$$

Obtenemos nuestros $y_i$:

- Para $y_{1}$:

$$
\begin{split}
    & 3\cdot 8 \cdot y_{1} \equiv 1 \mod 11 \implies 24y_{1} \equiv 1 \mod 11 \implies 2y_{1} \equiv 1 \mod 11
\end{split}
$$

Usamos la fracción continua de $\frac{11}{2}$:

$$
\begin{split}
    & \frac{11}{2} = 5 + \frac{1}{2}\\
    & y_{1} = -5 \equiv 6 \mod 11
\end{split}
$$

- Para $y_{2}$:

$$
\begin{split}
    & 2\cdot 1\cdot y_{2} \equiv 1 \mod 7 \implies 2y_{2} \equiv 1 \mod 7
\end{split}
$$

Se ve a simple vista que $y_{2}=4$

- Para $y_{3}$:

$$
\begin{split}
    & 5\cdot 5 \cdot y_{3} \equiv 1 \mod 9 \implies 25y_{3} \equiv 1 \mod 9 \implies 7y_{3} \equiv 1 \mod 9
\end{split}
$$

Usamos la fracción continua de $\frac{9}{7}$:

$$
\begin{split}
    & \frac{9}{7} = 1 + \frac{2}{7} = 1 + \frac{1}{3 + \frac{1}{2}} = [1;3,2]\\
    & [1;3] = 1 + \frac{1}{3} = \frac{4}{3} \implies y_{3} = 4
\end{split}
$$

Por lo tanto, nuestra solución final será:

$$
\begin{split}
    & x = 7\cdot 63\cdot 6 + 4 \cdot 99 \cdot 4 + 4\cdot 77\cdot 4 = 5462
\end{split}
$$

6. Resuelve la ecuación diofántica $102x + 58y = 6$

Primero simplificamos la ecuación: 

$$
\begin{split}
    & 102x + 58y = 6 \implies\\
    & 51x + 29y = 3
\end{split}
$$

Ahora calculamos la ecuación continua $\frac{51}{29}$

$$
\begin{split}
    & 51 = 1 + \frac{22}{29} = 1 + \frac{1}{\frac{29}{22}} = 1 + \frac{1}{1 + \frac{7}{22}} =\\
    & 1 + \frac{1}{1 + \frac{1}{\frac{22}{7}}} = 1 + \frac{1}{1 + \frac{1}{3 + \frac{1}{7}}} = [1;1,3,7]
\end{split}
$$
Ahora si calculamos la ecuación quitando el último término:

$$
[1;1,3] = 1 + \frac{1}{1 + \frac{1}{3}} = 1 + \frac{3}{4} = \frac{7}{4}
$$

Por lo tanto una solución a la ecuación $51x + 29y = 1$ será:

$$
\begin{split}
    & x_{0} = 4\\
    & y_{0} = -7
\end{split}
$$

Para nuestra ecuación diofántica multiplicamos por $3$:

$$
\begin{split}
    & x_{0} = 12\\
    & y_{0} = -21
\end{split}
$$

Sabiendo esta solución particular podemos sacar la general:

$$
\begin{split}
    & \begin{cases}
        51x_{0} + 29y_{0} = 3\\
        51x + 29y = 3
    \end{cases} \implies 51(x - x_{0}) + 29(y - y_{0}) = 0 \implies\\
    & \implies \begin{cases}
        x - x_{0} = 29k\\
        y - y_{0} = -51k
    \end{cases} \implies\\
    & \begin{cases}
        x = 29k + 12\\
        y = -51k - 21
    \end{cases}
\end{split}
$$

7. Encuentra la mejor aproximación para $\frac{54}{23}$ con el denominador menor de 10. Justifícalo.

Calculamos la fracción continua de $\frac{54}{23}$:

$$
\begin{split}
    & \frac{54}{23} = 2 + \frac{8}{23} = 2 + \frac{1}{\frac{23}{8}} = 2 + \frac{1}{2 + \frac{7}{8}} =\\
    & = 2 + \frac{1}{2 + \frac{1}{\frac{8}{7}}} = 2 + \frac{1}{2 + \frac{1}{1 + \frac{1}{7}}} = [2;2,1,7]
\end{split}
$$

Ahora vamos quitando términos:

$$
\begin{split}
    & [2; 2] = 2 + \frac{1}{2} = \frac{5}{2}\\
    & [2; 2, 1] = 2 \frac{1}{2 + \frac{1}{1}} = 2 + \frac{1}{3} = \frac{7}{3}\\
    & [2; 1, 1, 7] = \frac{54}{23}
\end{split}
$$

Por lo tanto, vemos que la mejor aproximación con denominador menor de 10 es $\frac{7}{3}$.

8. Para encriptar un mensaje se ha usado $n = 11 \cdot 13$, la clave pública $e=7$. Busca la clave privada que permita desencriptar el mensaje.

Primero calculamos $\phi(n)$:

$$
\begin{split}
    & \phi(n) = \phi(11)\phi(13) = 10\cdot 12 = 120
\end{split}
$$

Sabemos que $a^{120k + 1} \equiv a \mod n$, por lo que nuestra cable privada $d$ tiene que cumplir:

$$
\begin{split}
    & 120k + 1 = 7d
\end{split}
$$

Esto nos da la siguiente ecuación modular:

$$
\begin{split}
    & 7d \equiv 1 \mod 120
\end{split}
$$

Calculamos la ecuación continua de $\frac{120}{7}$:

$$
\begin{split}
    & 17 + \frac{120}{7} - 17 = 17 + \frac{1}{7} = [17;7]
\end{split}
$$

Calculamos la ecuación sin el último término:

$$
[17] = 17
$$

Entonces, para calcular la clave privada:

$$
17(-1)^1 = -17 \equiv 103 \mod 120
$$

Por lo tanto, la clave privada es $d = 103$.

$$
\begin{split}
    & a^{7\cdot 103} = a^{721} = a^{120\cdot 6} \cdot a \equiv a \mod 120
\end{split}
$$

9. $(a+b)|a^2,(a+b)|b^2$. ¿Es verdad que $(a+b)|ab$?

$$
\begin{split}
    & (a+b)|a^2 \implies a^2 = k_{1}(a+b) \implies a = \sqrt{k_{1}(a+b)}\\
    & (a+b)|b^2 \implies b^2 = k_{2}(a+b) \implies a = \sqrt{k_{2}(a+b)} \\
    & ab = \sqrt{k_{1}(a+b)}\sqrt{k_{2}(a+b)} = \sqrt{k_{1}k_{2}}|a+b| = k|a+b| \implies (a+b)|ab 
\end{split}
$$

10. Desarrolla como fracción continua $\sqrt{11}$

$$
\begin{split}
    & \sqrt{11} = 3 + \sqrt{11} - 3 = 3 + \frac{1}{\frac{1}{\sqrt{11} - 3 } \cdot \frac{\sqrt{11} + 3}{\sqrt{11} + 3}} =\\
    & = 3 + \frac{1}{\frac{\sqrt{11} + 3}{2}}\\
    & \frac{\sqrt{11} + 3}{2} = 3 + \frac{\sqrt{11} + 3}{2} - 3 = 3 + \frac{\sqrt{11} - 3}{2}=\\
    & = 3 + \frac{1}{\frac{2}{\sqrt{11} - 3} \cdot \frac{\sqrt{11} + 3}{\sqrt{11} + 3}} = 3 + \frac{1}{3 + \sqrt{11}} \implies\\
    & \sqrt{11} = 3 + \frac{1}{3 + \frac{1}{3 + \sqrt{11}}} = 3 + \frac{1}{3 + \frac{1}{3 + 3 + \frac{1}{3 + \frac{1}{3 + \sqrt{11}}}}} \implies\\
    & \implies \sqrt{11} = [3;3,6,3,6,3,6,\ldots] 
\end{split}
$$

11. Demuestra que la ecuación diofántica $x^2+ y^2 = 10000000000007$ no tiene solución.

Reducimos la ecuación a módulo 10

$$
\begin{split}
	& x^2 + y^2 = 7 \pmod{10}
\end{split}
$$
Podemos sacar dos ecuaciones:

$$
\begin{split}
	& x^2 = 2-y^2 = a \pmod{10}\\
	& y^2 = 2-x^2 = b \pmod{10}
\end{split}
$$

Los únicos valores que pueden tomar $x^2$ y $y^2$ para que esas ecuaciones tengan solución son $\{0,1,4\}$

| $x^2$ | $y^2$ | $x^2 + y^2$ |
| ----- | ----- | ----------- |
| 0     | 0     | 0           |
| 0     | 1     | 1           |
| 1     | 0     | 1           |
| 1     | 1     | 2           |
| 4     | 0     | 4           |
| 0     | 4     | 4           |
| 4     | 1     | 5           |
| 1     | 4     | 5           |
| 4     | 4     | 8           |

Como vemos, no hay ninguna combinación que de 7, por lo que la ecuación diofántica no tiene solución.

