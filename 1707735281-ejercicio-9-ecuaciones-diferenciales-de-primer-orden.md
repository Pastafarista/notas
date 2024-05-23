---
id: 1707735281-ejercicio-9-ecuaciones-diferenciales-de-primer-orden
aliases:
  - Ejercicio 9 ecuaciones diferenciales de primer orden
  - Resuelve la siguiente ecuación diferencial
tags:
  - ecuaciones-diferenciales
---
 
# Resuelve la siguiente [[1706869334-ecuacin-diferencial|ecuación diferencial]]

$$\begin{split}
    & (x + y - 2)dx + (x - y + 4)dy = 0 \implies \\
    & \implies y' = - \frac{(x+y-2)}{x-y+4} = f \left( \frac{-x-y+2}{x-y-+4} \right)\\
    & r: x+y-2= 0 \;\;\;\; s: x-y+4 = 0 \implies \\
    & \begin{cases}
        r: y = -x + 2 \\
        s: y = x - 4
    \end{cases}
    \implies x = -1 \;\; y=3 \implies \\
    & \implies
    \begin{cases}
      & x = \mathcal{X} + y_0 = \mathcal{X} - 1 \implies dx = d \mathcal{X} \\ 
       & y = \mathcal{Y} + y_0 = \mathcal{Y} + 3 \implies dy = d \mathcal{Y} \\
    \end{cases} \\
       & y' = \frac{-x-y+2}{x-y+4} \implies \mathcal{Y}' = \frac{-(\mathcal{X} - 1) - (\mathcal{Y} + 3) + 2}{(\mathcal{X} - 1) - (\mathcal{Y} + 3) + 4} \implies \\
       & \implies \mathcal{Y}' = \frac{\mathcal{X} + \mathcal{Y}}{\mathcal{Y} - \mathcal{X}} = f  \left( \frac{\mathcal{X}}{\mathcal{Y}} \right)\\
       & \mathcal{Y}' = \frac{\mathcal{X} + \mathcal{Y}}{\mathcal{Y} - \mathcal{X}} \implies u + \mathcal{X}u' = \frac{\mathcal{X} + \mathcal{X}u}{\mathcal{X}u - \mathcal{X}} \implies \\
       & \implies u + \mathcal{X}u' = \frac{1 + u}{u - 1} \implies \mathcal{X}u' = \frac{1+u}{u-1} - u \implies \\
       & \implies \mathcal{X}u' = \frac{1+u-u^2 + u}{u-1} \implies \mathcal{X} \frac{du}{d\mathcal{X}} = \frac{1 + 2u - u^2 }{u - 1} \implies \\
       & \implies \frac{u - 1}{1 + 2u - u^2}du = \frac{1}{\mathcal{X}} d \mathcal{X} \implies \int \frac{1 - u}{1 + 2u - u^2}du = \int - \frac{1}{\mathcal{X}} d \mathcal{X} \implies \\
       & \implies \frac{1}{2} ln | 1 +2u - u^2 | = -ln | \mathcal{X} | + C_1 \implies\\
       & \implies ln | 1 + 2u - u^2 |^{\frac{1}{2}} = ln| \mathcal{X}|^{-1} + C_1 \implies \\
       & \implies \sqrt{|1+2u-u^2|} = \frac{1}{\mathcal{X}} \cdot C_2 , C_2 \in \mathbb{R} \implies \\
       & \implies \sqrt{|1 + 2 \left( \frac{\mathcal{Y}}{\mathcal{X}} \right) - \left( \frac{\mathcal{Y}}{\mathcal{X}}  \right)^2|} = \frac{1}{|\mathcal{X}|} + C_2 \implies \\
       & \implies \frac{\sqrt{|\mathcal{X}^2 - 2 \mathcal{X}\mathcal{Y} - \mathcal{Y}^2|}}{\sqrt{\mathcal{X}^2}} = \frac{1}{|\mathcal{X}|} \cdot C_2 \implies \sqrt{|\mathcal{X}^2 - 2\mathcal{X} \mathcal{Y} - \mathcal{Y}^2|} = C_2
    
\end{split}$$
