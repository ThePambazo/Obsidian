El método de Bisección o **corte binario**, **de partición de intervalos** o simplemente **Bolzano**, se enfoca en dividir a la mitad el intervalo de trabajo. Si la función cambia de signo sobre un intervalo, se evalúa el valor de la función en el punto medio y se aproxima a la raíz cerrando el intervalo y aproximándose situando la raíz en el punto medio.
En general se busca que ambos extremos del intervalos tengan signos opuestos, esto es.
$$ f(x_1)f(x_0) $$
## Algoritmo del método

Paso 1: Elija los valores iniciales inferior $x_i$ y superior $x_s$, que encierran a la raíz, de forma tal que la función cambie de signo en el intervalo. Esto es  $f(x_1)f(x_0) < 0$.
	Paso 1: Elija los valores iniciales inferior $x_i$ y superior $x_s$, que encierran a la raíz, de forma tal que la función cambie de signo en el intervalo. Esto es  $f(x_1)f(x_0) < 0$.
	Paso 2: la aproximación de la raíz se determina mediante: $$ x_r=\frac{x_1+x_u}{2} $$
	Paso 3: Realice las siguientes evaluaciones para determinar en qué subintervalo está la raíz :
		a) Si $f(x_1)f(x_r)<0$, entonces la raíz se encuentra dentro del subintervalo inferior o izquierdo. Por lo tanto, haga $x_u=x_r$ y vuelva al paso 2.
		b) Si $f(x_1)f(x_r)>0$, entonces la raíz se encuentra dentro del subintervalo **superior** o **derecho**. Por lo tanto, haga $x_0=x_r$ y vuelva al paso 2.
		c) Si $f(x_1)f(x_r)=0$, la raíz es igual a $x_r$; termina el cálculo.
### Criterio de finalización

$$ \epsilon_a= \bigg|\frac{x_r^{nueva}-x_r^{vieja}}{x_r^{nueva}}\bigg| $$
$$ \epsilon_a= \bigg|\frac{x_u - x_l}{x_u+x_l}\bigg| $$
