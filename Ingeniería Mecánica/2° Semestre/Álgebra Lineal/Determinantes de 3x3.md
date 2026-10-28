Sea $A$ una matrix de $3 \times 3$ definida como
$$ A=\begin{bmatrix} 
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33}
\end{bmatrix} $$
Se define su determinante como 

$$ det(A) = a_{11}|A_{11}| - a_{12}|A_{12}|-a_{13}|A_{13}| $$
Donde la matriz $A_{ij}$ es aquella donde se eliminan la columna $i$ y la fila $j$
$$ det(A) = a_{11} \Bigg|\begin{bmatrix} a_{22} & a_{23}  \\ a_{32} & a_{33}\end{bmatrix}\Bigg| - a_{12}\Bigg| \begin{bmatrix}  a_{21} & a_{23}  \\ a_{31} & a_{33} \end{bmatrix}    \Bigg| - a_{13}\Bigg|\begin{bmatrix}  a_{21} & a_{22}  \\ a_{31} & a_{32} \end{bmatrix} \Bigg| $$