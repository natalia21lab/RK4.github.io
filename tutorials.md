
## Funciones:  

En esta parte se muestran las funciones que se deben implementar para resolver el problema y otra que el usuario debe implementar para obtener la solución al problema dinámico.

Por ejemplo, primero debe implementarse la función que genera el estado dinámico: 

def dyn_generator(oper,state):
"""Genera la función de estado dinámico

Ejemplos: 
   >>> np.dot(oOper, state)
   np.array([0,0], [0,0]])

Args: 

   np.oOper(list): primer argumento
   np.state(list): segundo argumento 

Returns: 

   list: retorna el resultado de multiplicar `np.oOper` y `np.state`

   """
return np.dot(oOper, state)

La otra función que debe implementarse es propiamente la del método Runge Kutta: 

def rk4(func, oper, state, h):

"""La función Runge Kutta
    t_values = np.arange(t0, t_end + dt, dt)
    y_values = np.zeros(len(t_values))
    y_values[0] = y0

"""

Aquí el usuario debe introducir valores y realizar el for loop. 

for tt in range(times.size):
""" Este es el ciclo que va a iterar sobre los valores definidos previamente, debe escribir un código

Seguidamente, se obtienen los valores de las entradas de yInit: 

    #Aquí deben obtenerse los valores de las entradas de yInit mediante un código
    #Aquí se invoca el método rk4 operando sobre yInit y se devuelve el resultado a un nuevo yN:        

Finalmente, se asigna yN a yInit para iterar y obtener los valores de k de forma consecutiva. 
    
    # Ahora asignamos yN a yInit
    # De esta manera, en la siguiente iteración, el operador de esta iteración se convierte en el inicial
    # de la siguiente iteración
    yInit = yN

    
