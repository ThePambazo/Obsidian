![[Pasted image 20231203212344.png]]
La deformación de un cuerpo es debida a las fuerzas ejercidas sobre el mismo.
Para su análisis introducimos las [[Coordenadas Materiales]] y las [[Coordenadas Espaciales]]

En ocasiones se facilitará usar el [[Enfoque Lagrangiano (Material)]] y usualmente es mas fácil realizar análisis desde este marco de referencia, sin embargo existe también el [[Enfoque Euleriano (Espacial)]]  para otro tipo de análisis.


El vector de posición $\vec{X}_A$ describe las coordenadas del punto $P$ (punto en la posición sin deformación) mientras el vector $\vec{x}_i$ describe las coordenadas del punto $p$  ya deformado. 
$$ \vec{X}=X_A\vec{I_A}=X_1 \vec{I_1}+X_2\vec{I_2}+X_3\vec{I_3} \longrightarrow \text{Cordenadas Materiales}  $$
$$ \vec{x}(t) = x_i\vec{i}_i=x_1\vec{i}_1 +x_2\vec{i}_2+x_3\vec{i}_3 \longrightarrow \text{Coordenadas Espaciales} $$
## Ley de Movimiento
La ley de movimiento de un cuerpo describe el cambio en posición de las partículas de un cuerpo. Partiendo de las [[Coordenadas Materiales]] se obtienen las [[Coordenadas Espaciales]] en un tiempo $t>0$. Esto es un función multivariable done las variables independientes son el tiempo $t$ y las coordenadas materiales.
$$ x=(X,t)  $$
### Relación inversa
Aún cuando existe la Ley de Movimiento general, en ocasiones es conveniente expresarla en su forma inversa, esto es.
$$ X=(x,t)$$
### Jacobiano
Es la condición que garantiza la existencia de la función inversa, el Jacobiano debe ser diferente de cero.
$$ J= det\begin{vmatrix} \frac{\partial{x_1}}{\partial{X_1}} &  \frac{\partial{x_1}}{\partial{X_2}} & \frac{\partial{x_1}}{\partial{X_3}} \\ \frac{\partial{x_2}}{\partial{X_1}} & \frac{\partial{x_2}}{\partial{X_2}}  & \frac{\partial{x_2}}{\partial{X_3}}\\ \frac{\partial{x_3}}{\partial{X_1}} &\frac{\partial{x_3}}{\partial{X_2}} & \frac{\partial{x_3}}{\partial{X_3}}\end{vmatrix} \neq 0 $$

$$  $$
## Campo de desplazamientos (Vector de los desplazamientos u)
El vector mostrado en la imagen $\vec{u}_i$ se define como la diferencia entre los vectores de posición $x_i$ y $X_A$. Obteniendo la siguiente expresión:
$$  u=x-X \longrightarrow \vec{u}_i=\vec{x}_i-\vec{X}_A $$
### Derivada del vector de los desplazamientos
La derivada del vector de los desplazamientos con respecto al tiempo, se define como:
$$ \frac{du}{dt}=\frac{d(x-X)}{dt}=\frac{dx}{dt}=V  $$
Si se encuentra en su forma espacial (depende del tiempo) la diferencia de los vectores de posición, resultará en la derivada de un vector de posición respecto al tiempo, lo que se traduce en la **velocidad**.

## Tensor de Deformación Finita
![[Pasted image 20231204005151.png|500]]
### El vector relativo diferencial de posición
Si se sitúan dos puntos $P$ y $Q$  en el sistema de referencia  y se define un vector que una ambos puntos  $d\vec{X}_A$ podremos vislumbrar el cambio en dicho vector conforme a la deformación, pues los mismos puntos $p$ y $q$ en el sistema deformado tendrán su propio vector relativo $dx_i$. Por tanto el vector $dX$ se convierte en el vector $dx$. 

$$dX=dX_A\hat{I}_A \longrightarrow dx=dx_i\hat{e}_i $$

### Tensor Gradiente de Deformación
Es aquel tensor que caracteriza la deformación local de $X$ , es útil para determinar el vector diferencial de posición $dX$, se define como:
$$ F_{iA}\equiv \frac{\partial{x_i}}{\partial{X_A}} $$
Que en notación matricial se escribe como:
$$ \begin{bmatrix} \frac{\partial{x_1}}{\partial{X_1}} &  \frac{\partial{x_1}}{\partial{X_2}} & \frac{\partial{x_1}}{\partial{X_3}} \\ \frac{\partial{x_2}}{\partial{X_1}} & \frac{\partial{x_2}}{\partial{X_2}}  & \frac{\partial{x_2}}{\partial{X_3}}\\ \frac{\partial{x_3}}{\partial{X_1}} &\frac{\partial{x_3}}{\partial{X_2}} & \frac{\partial{x_3}}{\partial{X_3}}\end{bmatrix}  $$
Con ayuda de este tensor es posible definir al vector relativo diferencial de posición
$$ dx_i=F_{iA} \cdot dX_A $$
El Gradiente de Deformación inverso se define como:
$$ F_{iA}^{ \\-1}= \frac{\partial{X_A}}{\partial{x_i}} $$
Podemos definir entonces al vector diferencial de posición en coordenadas materiales como:
$$dX_A=F_{iA}^{ \\-1}\cdot dx_i $$
### Diferencia de magnitudes

Existen diversas formas de medir la deformación, una de ellas es la diferencia entre las magnitudes del vector relativo diferencial de posición en coordenadas espaciales contra las materiales. 
$$ (dx)^2-(dX)^2=dx_i \\ dx_i -dX_AdX_A$$
Con esta simple diferencia podemos determinar tres casos:
- Si la diferencia es positiva (+).  Se presenta una elongación.
- Si la diferencia es negativa (-). Se presenta una compresión.
- Si la diferencia es cero (0). No existe deformación.

## Tensor de Deformación Finita 
 Desarrollando la ultima expresión
 $$ \begin{align*} (dx)^2-(dX)^2 & = \bigg(\frac{\partial{x_i}}{\partial{X_A}}dX_A\bigg)\bigg(\frac{\partial{x_i}}{\partial{X_B}}dX_B\bigg)- \delta_{AB} dX_AdX_A \\\\
 & = \bigg(\frac{\partial{x_i}}{\partial{X_A}} \frac{\partial{x_i}}{\partial{X_B}} - \delta_{AB}\bigg)dX_AdX_B \\\\
 &=\bigg(C_{AB}-\delta_{AB}\bigg)dX_AdX_B
  \end{align*} $$
 #### Tensor de Deformaciones Finitas de Green
Se define a  $C_{AB}$  como el **Tensor de Deformaciones Finitas de Green**.
$$ C_{AB}=\bigg(\frac{\partial{x_i}}{\partial{X_A}} \frac{\partial{x_i}}{\partial{X_B}}\bigg) \ \ \ \ \ \ \text{ó} \ \ \ \ \ \ \ C=F^T \cdot F $$
#### Tensor de Esfuerzos Finitos de Lagrange
Se define como $2E_{AB}$ al tensor de esfuerzos finitos de Lagrange, como se muestra a continuación.
$$ 2E_{AB} = C_{AB}-\delta_{AB} \ \ \ \ \ \ ó \ \ \ \ \ \ 2E=C-I   $$
Donde $I$ es la matriz o vector Identidad.
$$ I=\begin{bmatrix} 1 & 0 & 0 \\ 0&1&0 \\0&0&1 \end{bmatrix} $$

### Tensor de deformaciones de Cauchy
Se define como $c_{ij}$ al tensor de deformaciones de Cauchy (en coordenadas espaciales)
$$ c_{ij}=\bigg(   \frac{\partial X_A}{\partial x_i} \frac{\partial X_A}{\partial x_j}  \bigg) \ \ \ \ \ \ \text{ó} \ \ \ \ \ \ \ c=(F^{-1})^T\cdot (F^{-1}) $$

### Tensor de Esfuerzos Finitos de Euler
Se define como $2e_{ij}$ al tensor de esfuerzos finitos de Euler (en coordenadas espaciales).
$$ 2e_{ij}= (\delta_{ij}-c_{ij}) \ \ \ \ \ \ \text{ó} \ \ \ \ \ \ \  2e=(I-c) $$
Donde $I$ es la matriz o vector Identidad.
$$ I=\begin{bmatrix} 1 & 0 & 0 \\ 0&1&0 \\0&0&1 \end{bmatrix} $$

### Diferencia de magnitudes del vector relativo diferencial de posición utilizando el tensor de Deformaciones finitas de Lagrange
Es posible definir la diferencia de las magnitudes de los vectores de posición relativas utilizando el tensor de deformaciones finitas de Lagrange, como se muestra  a continuación.
 $$ \begin{align}  (d\vec{x})^2-(d\vec{X})^2=2E_{AB}dX_AdX_B \\ 
 (d\vec{x})^2-(d\vec{X})^2= dX\cdot2E_{AB}\cdot dX \end{align}$$
 Así mismo es posible definirla utilizando el vector de esfuerzos finitos de Euler
  $$ \begin{align}  (d\vec{x})^2-(d\vec{X})^2=2e_{ij}dx_idx_j \\ 
 (d\vec{x})^2-(d\vec{X})^2= dx\cdot2e\cdot dx \end{align}$$
 