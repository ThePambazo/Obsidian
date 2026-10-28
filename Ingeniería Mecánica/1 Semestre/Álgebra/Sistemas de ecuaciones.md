

Si se tiene un sistema de ecuaciones, ya sea en arreglo matricial o lineal, se deben detener $m$ número de incógnitas y $n$ número de ecuaciones 

## Clasificación de Sistemas 
### 1. **Según el número de soluciones**

Esta clasificación depende de si el sistema tiene una, ninguna o infinitas soluciones.

- **Sistema consistente (compatible)**:
    
    - **Determinados**: Si el sistema tiene una única solución. Esto ocurre cuando el número de ecuaciones es suficiente y no hay contradicciones.
    - **Indeterminados**: Si el sistema tiene infinitas soluciones. Esto ocurre cuando las ecuaciones del sistema son dependientes entre sí (es decir, no proporcionan información nueva) o cuando el rango de la matriz de coeficientes es menor que el número de incógnitas.
- **Sistema inconsistente (incompatible)**: Si el sistema no tiene ninguna solución. Esto ocurre cuando hay una contradicción entre las ecuaciones, por ejemplo, cuando una ecuación implica que 0=10 = 10=1, lo que no es posible.
    

### 2. **Según la relación entre el número de ecuaciones y el número de incógnitas**

Aquí se analiza cuántas incógnitas se pueden resolver dependiendo del número de ecuaciones.

- **Sistema determinado**: Tiene el mismo número de ecuaciones que incógnitas, lo que en teoría sugiere que debería tener una única solución (aunque puede haber excepciones si las ecuaciones son dependientes).
    
- **Sistema sobredeterminado**: Tiene más ecuaciones que incógnitas. Esto puede generar un sistema incompatible si hay contradicciones entre las ecuaciones o redundancia si algunas ecuaciones no añaden nueva información.
    
- **Sistema subdeterminado**: Tiene menos ecuaciones que incógnitas. En este caso, es común que el sistema tenga infinitas soluciones, ya que no hay suficiente información para determinar un valor único para cada incógnita.
    

### 3. **Según la linealidad de las ecuaciones**

Se refiere a la forma de las ecuaciones que forman el sistema.

- **Sistema lineal**: Todas las ecuaciones son lineales, es decir, tienen la forma a1x1+a2x2+⋯+anxn=ba_1x_1 + a_2x_2 + \cdots + a_nx_n = ba1​x1​+a2​x2​+⋯+an​xn​=b, donde los coeficientes aia_iai​ son constantes, y las incógnitas no están elevadas a potencias ni multiplicadas entre sí.
    
- **Sistema no lineal**: Al menos una de las ecuaciones no es lineal, es decir, incluye términos como xi2x_i^2xi2​, xixjx_i x_jxi​xj​, exie^{x_i}exi​, etc. Este tipo de sistemas puede ser mucho más complejo de resolver y, en muchos casos, no tiene una solución analítica.
    

### 4. **Según el tipo de coeficientes**

Se refiere a la naturaleza de los coeficientes y las incógnitas del sistema.

- **Sistema con coeficientes constantes**: Los coeficientes de las incógnitas son números constantes.
    
- **Sistema con coeficientes variables**: Los coeficientes dependen de una o más variables externas (como en sistemas diferenciales o sistemas dinámicos).
    

### 5. **Según la homogeneidad**

Se basa en si los términos independientes (en el lado derecho de las ecuaciones) son todos cero o no.

- **Sistema homogéneo**: Un sistema es homogéneo cuando todos los términos independientes son iguales a cero, es decir, todas las ecuaciones son de la forma a1x1+a2x2+⋯+anxn=0a_1x_1 + a_2x_2 + \cdots + a_nx_n = 0a1​x1​+a2​x2​+⋯+an​xn​=0. Este tipo de sistemas siempre tiene al menos una solución trivial (cuando todas las incógnitas son cero).
    
- **Sistema no homogéneo**: Un sistema es no homogéneo cuando al menos uno de los términos independientes es distinto de cero, es decir, tiene la forma a1x1+a2x2+⋯+anxn=ba_1x_1 + a_2x_2 + \cdots + a_nx_n = ba1​x1​+a2​x2​+⋯+an​xn​=b, con b≠0b \neq 0b=0.
    

### 6. **Según la estructura de la matriz de coeficientes**

Esta clasificación está relacionada con el rango de la matriz asociada al sistema.

- **Sistema de rango completo**: Un sistema tiene rango completo si el rango de la matriz de coeficientes es igual al número de incógnitas. En un sistema lineal, esto implica que el sistema es determinado y tiene una única solución.
    
- **Sistema de rango deficiente**: Un sistema tiene rango deficiente si el rango de la matriz de coeficientes es menor que el número de incógnitas. En este caso, el sistema es indeterminado (con infinitas soluciones) o inconsistente (sin solución).
    

### Resumen gráfico de la clasificación de sistemas:

| **Criterio**                         | **Tipos de Sistemas**                                          |
| ------------------------------------ | -------------------------------------------------------------- |
| Número de soluciones                 | Compatible determinado, Compatible indeterminado, Incompatible |
| Relación entre ecuaciones/incógnitas | Determinado, Sobredeterminado, Subdeterminado                  |
| Linealidad                           | Lineal, No lineal                                              |
| Coeficientes                         | Constantes, Variables                                          |
| Homogeneidad                         | Homogéneo, No homogéneo                                        |
| Rango de la matriz                   | Rango completo, Rango deficiente                               |

## Sistema de ecuaciones de $m\times n$ 
Los sistemas de ecuaciones están compuestos por $m$ cantidad de ecuaciones y $n$ cantidad de incógnitas. De esta forma es posible ordenar en una matriz de  $m\times n$ el sistema, como se muestra a continuación:
$$ \begin{bmatrix}  a_{11} & a_{12} &⋯& a_{1n} \\
					a_{21} & a_{22} &...& a_{2n} \\
					⋮ & ⋮ & & ⋮    \\
					 a_{m1} & a_{m2} & ...& a_{mn}
				 	\end{bmatrix} $$
Existen tres posibles casos para el sistema:
- **Sistema Determinado ($m=n$).** Matriz cuadrada, tiene solución exacta para cada caso.
- **Sistema Sobredeterminado ($m>n$).** Tiene más ecuaciones que incógnitas, la solución estará dada por mínimos cuadrados.
- **Sistema Subdeterminado ($m<n$)**. Tiene menos ecuaciones que incógnitas, solución básica con un máximo de $m$ componentes distintos de cero.

