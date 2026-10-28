Sirve para realizar operaciones entre [[Tensores]] , sin la necesidad de utilizar los vectores unitarios $\hat{e}_1$ 
Considere el siguiente sistema de ecuaciones
$$ \begin {split} a_{11}x_1+a_{12}x_2+a_{13}x_3=b_1 \\
                  a_{21}x_1+a_{22}x_2+a_{23}x_3=b_2\\
                  a_{31}x_3+a_{32}x_3+a_{33}x_3=b_3\end{split}$$
        NOTA: $a_{11}x_1$ es un solo término, mientras que $a_{22}x_2$ es otro término diferente, en total, en este sistema de ecuaciones existen nueve términos.
Se puede reescribir como:
$$ \sum_{k=1}^3 a_{ik}x_k=b_i\ ; \ \ \ i=1,2,3  $$
**Importante:** El subíndice $k$ se lleva la carga de la suma, mientras que el $i$ queda libre (solo aparece una vez).
## Convenciones
**Convención 1**. Todos los subíndices utilizados tienen el rango $[1,2,3]$. 
**Convención 2**. Siempre que un subíndice se repita solamente **una vez**, es decir, que aparezca dos veces en el mismo término, se requiere realizar la suma de dicho subíndice.
Tomando en cuenta ambas convenciones la expresión en forma de suma se puede reescribir como:

$$ a_{ik}x_k=b_i  $$
		Nota: No se puede repetir un término mas de una vez

### ¿qué pasa si necesito más de un subíndice libre?
Como hemos visto anteriormente existen dos tipos de subíndice.
- Libre: Su rango es de $[1,2,3]$, sin embargo al no estar repetido
- Dummy. aparece en un término dos veces. Su rango es de $[1,2,3]$ y tiene asociado a el la suma de términos
$$\begin{split} 
a_{11}x_1^2+a_{12}x_2x_1+a_{13}x_3x_1=b_{11}\\
a_{11}x_1x_2+a_{12}x_2^2+a_{13}x_3x_2=b_{12}\\
a_{11}x_1x_3+a_{12}x_2x_3+a_{13}x_3^2=b_{13}\\
a_{21}x_1^2+a_{22}x_2x_1+a_{23}x_3x_1=b_{21}\\
a_{21}x_1x_2+a_{22}x_{2}^2+a_{23}x_3x_2=b_{22}\\
a_{21}x_1x_3+a_{22}x_2x_3+a_{23}x_3^2=b_{23}\\
a_{31}x_1^2+a_{32}x_2x_1+a_{33}x_3x_1=b_{31}\\
a_{31}x_1x_2+a_{31}x_2^2+a_{33}x_3x_2=b_{32}\\
a_{31}x_1x_3+a_{32}x_2x_3+a_{33}x_3^2=b_{33}

\end{split}$$

Si se analiza detenidamente es sistema de ecuaciones presentado, podremos notar que se puede expresar en notación índice como:
$$a_{ik}x_kx_j=b_{ij}$$
Obteniendo dos subíndices libres $i,j$ (que aparecen sólo una vez en el término $a_{ik}x_kx_j$) y un subíndice suma $k$. Por lo que podemos escribir tantos subíndices libre como queramos mientras se denoten con letras distintas, pues por definición, ya no serían libres si se repiten.

