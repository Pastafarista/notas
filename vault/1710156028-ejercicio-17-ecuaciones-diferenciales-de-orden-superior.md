---
id: 1710156028-ejercicio-17-ecuaciones-diferenciales-de-orden-superior
aliases:
  - Ejercicio 17 ecuaciones diferenciales de orden superior
tags:
  - ecuaciones-diferenciales
---

# Resuelve la ecuación ${x^2y''-xy'+2y=0}$

$$
\begin{split}
    & y = x^{m} \implies y' = m\cdot x^{m-1} \implies y'' = m(m-1)x^{m-2}\\
    
    & x^2\cdot y'' - xy' + 2y = 0 \implies x^2\cdot m(m-1)x^{m-2} - x \cdot  mx^{m-1}+2x^{m} = 0 \implies\\
    
    & \implies x^{m}(m^{2}-2m+2) = 0\implies m^2 - 2m + 2 = 0 \implies m = 1 \pm i \implies\\
    
    & \implies 
    \begin{cases}
		& \alpha = 1\\
		& \beta  = 1
	\end{cases}\\
	
    & y = x^{1}(C_{1}\cos (\ln (x^1)) + C_{2}\sin (\ln (x^1)))\\
    
    & \mathcal{W}(y_{1},y_{2}) =\\
    & \begin{vmatrix}
        x^{\alpha } \cdot \cos (\ln (x^{\beta } )) & x^{\alpha } \cdot  \sin (\ln (x^{\beta } ))\\
	    \alpha \cdot x^{\alpha  - 1} \cdot  \cos (\ln (x^{\beta } )) - x^{\alpha } \cdot \sin (\ln (x^{\beta } )) \cdot \beta \cdot \frac{x^{\beta -1} }{x^{\beta } } & \alpha \cdot  x^{\alpha -1} \sin (\ln (x^{\beta }))  + x^{\alpha }\cdot \cos (\ln (x^{\beta } ))\cdot \beta \cdot \frac{x^{\beta -1} }{x^{\beta } } 
    \end{vmatrix} =\\
    
    & = \alpha \cdot x^{\alpha } \cdot x^{\alpha -1}\sin (\ln (x^{\beta } ))\cdot \cos (\ln (x^{\beta } ))  + x^{\alpha }\cdot x^{\alpha }\cdot \cos ^2(\ln (x^{\beta } )) \cdot \beta x^{-1}+\\
    
    & - \alpha \cdot x^{\alpha } \cdot x^{\alpha -1}\sin (\ln (x^{\beta } ))*\cos (\ln (x^{\beta } )) + x^{\alpha } \cdot  x^{\alpha } \cdot  \sin^2(\ln (x^{\beta } ))\cdot \beta \cdot x^{-1}=x^{2\alpha -1}\cdot \beta \neq 0 \text{ si } x \neq  0    
\end{split}
$$
