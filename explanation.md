## El método Runge Kutta 

Este es uno de los métodos más utilizados para resolver numéricamente problemas de ecuaciones diferenciales ordinarias con condiciones iniciales, es útil cuando la solución no puede hallarse mediante otros métodos; este método proporciona un pequeño margen de error con respecto a la solución real del problema. Resuelve ecuaciones diferenciales de la forma: 

$$
f(x,y,\frac{dy}{dx})= 0 
$$

Con 

$$
{y(x_0)}= {y_0}  
$$ 

El método para este problema está dado por esta ecuación: 

$$
y_{i+1}= {y_i} + \frac{1}{6}[{k_1} + 2{k_2} + 2{k_3} + {k_4}] 
$$ 

El método RK4 utiliza un tamaño de paso h y n número de iteraciones. Además, para i=0,…, n-1 la solución se da a lo largo del intervalo $$(x_{0}, x_{0} + hn)$$  donde: 

$$ 
k_{1}= h f(x_{i}, y_{i})
$$

$$
k_{2}= h f[x_{i} + \frac{h}{2}, y_{i}+ \frac{k_1}{2}]
$$

$$
k_{3}= h f [x_{i} + \frac{h}{2}, y_{i} + \frac{k_2}{2}]
$$

$$
k_{4} = h f [x_{i} + h, y_{i} + k_{3}]
$$

Entonces el siguiente valor $$y_{i+1}$$ es determinado por el valor $${y_i}$$ actual sumándole el producto del tamaño del intervalo h por una pendiente estimada. La pendiente es un promedio ponderado de pendientes:

k1: pendiente al principio del intervalo 

k2: pendiente en el punto medio del intervalo, usando k1 para determinar el valor de y en el punto  xi + $$\frac{h}{2}$$.  

k3: nuevamente la pendiente del punto medio, pero ahora usando k2 para determinar el valor de y 

k4: pendiente al final del intervalo, con el valor de y determinado por k3

Finalmente, se promedian las 4 pendientes y se le asigna mayor peso a las pendientes en el punto medio, de esta manera: 

$$ Pendiente = \frac{(k_{1} + 2 k_{2} +2k_{3} + k_{4})}{6} $$ 
