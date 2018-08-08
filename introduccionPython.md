
# Introducción 

[Python](https://www.python.org/) es un lenguaje de programación muy popular que puede utilizarse para la creación de sitios web, juegos, software académico, y mucho más.

Pyhon se origino en la década de los 1980 por [Guido van Rossun](https://es.wikipedia.org/wiki/Guido_van_Rossum) en el Centro para las Matemáticas y la Infomática (CWI, Centrun Wiskunde & Informatica) en Holanda. 

El objetivo principal de Python es ser legible por los seres humanos, es decir, se hace hincapié en una sintaxis que favorezca el codigo legible, es por eso que Python parece mucho más simple que otros lenguajes de programación.

Actualmente existen Python 2 en su última versión 2.7.15 y Python 3 en su última versión 3.7.0. 

En este curso vamos a trabajar con Python 2, la razón es que utilizremos el módulo [GAlgebra](https://github.com/brombo/galgebra), el cual solo esta disponible para Python 2.

# Instalación 
### Windows
Puedes descargar Python para Windows desde el sitio web https://www.python.org/downloads/windows/, aquí debes elegir Python 2.

Después de descargar el archivo *Windows x86-64 MSI installer* debes ejeutarlo y seguir las instrucciones. Es importante recordar la ruta/direcctorio donde se ha instalado Python, aveces es necesario.

### Ubuntu/Linux 
Es posible que ya tengas instalado Python. Para verificarlo, abrimos la consola/terminal y escribes: 
```
python2 --version
```
El comando anterior sirve para verificar que versión de Python tienes.

Si no tienes instalado Python o quieres un version diferente, podemos hacerlo de la siguiente manera:
```
sudo apt install python2
```
### OS X
Puedes descargar Python para Windows desde el sitio web https://www.python.org/downloads/mac-osx/, aquí debes elegir Python 2.

Descarga el archivo *Mac OS X 64 bit/32 bit installer*, después hz click en Python.mpkg para ejecutar el instalador.

Por último verifica que la instalación fue exitosa abriendo la termianl y escribiendo lo siguiente:
```
python2 --version
```

# Instalación del *pip*
¿Qué es el *pip*?
Pip viene del acrónimo, *Pip Installs Packages* o *Pip Installs Python*, esto quiere decir que este programa hace una gestión de paquetes y se utiliza para instalar y desinstalar software que se ha escrito para Python.

Existen varias maneras de instalar y gestionar paquetes en Python, pero una de las más senillas y altamente recomendable es el uso del *pip* en la consola.

Usando *pip* podemos instalar/actualizar/desinstalar cualquier paquete de Python. 
### Windows
Descarge el siguiente script del [enlace](https://bootstrap.pypa.io/get-pip.py) y guárdalo en cualquier carpeta de tu PC, por ejemplo la carpeta *Desktop*.

Abrimos la terminal y navegamos hasta el archivo *get-pip.py* y ejecutamos lo siguiente:  
```
python get-pip.py
```
### Linux/Ubuntu

Para instalar *pip* en Ubuntu, ejecutamo lo siguiente en la terminal: 
```
sudo apt-get install python-pip
```
### OS X
Solo debemos escribir en la consola lo siguiente:
```
sudo easy_install pip
```
__Observación__
Si está utilizando Python 2.7.9 (o superior) o Python 3.4 (o superior), entonces *pip* viene instalado con Python por defecto. 

### Python Prompt
Para empezar a jugar con Python, tenemos que abrir una línea de comandos en nuestra computadora. 

Hacemos la anterior de la siguiente manera, escribe en la consola: 
```
python
```
y pulsa Enter.

### Nuestro primer comando en Python.
Después de ejecutar el comando de Python, el cursor cambia a ``` >>> ```. Para nosotros esto significa que por ahora sólo podemos utilizar comandos en el lenguaje Python. 

Si deseas salir de la consola de Python en cualquier momento, simplemente escribe ```exit()``` o usa el atajo ```Ctrl + Z``` para Windows y ```Ctrl + D``` para Mac/Linux. Asi desaparece ```>>>```.

Pero ahora no queremos salir de la consola de Python. Queremos aprender más sobre ella. Vamos a empezar con algo muy simple. Por ejemplo, trata de escribir algo de aritmética, como ```2 + 3``` y pulsa Enter.
```
>>> 2 + 3
5
```
¡Bien! Como puedes ver salió la respuesta, eso nos dice que Python sabe matemáticas. Por lo tanto python sabe dividir, multiplicar, sumar, restas, etc.

### Strings
Un *string* es una secuencia de caracteres que puede ser procesada por una computadora.

```
>>> "Ola"
'Ola'
```
Nota que un *string* debe comenzar y terminar con el mismo carácter. Esto puede ser comillas simples (') o dobles ("),  ellas le dicen a Python que lo que esta dentro es una cadena.

Las cadenas pueden ser concatenadas. Prueba esto:
```
>>> "Hola " + "Ola"
'Hola Ola'
```
También puedes multiplicar las cadenas con un número:
```
>>> "Ola" * 3
'OlaOlaOla'
```
Si necesitas poner un apóstrofe dentro de tu cadena, tienes dos maneras de hacerlo.

Usando comillas dobles:
```
>>> "Pepe's Party "
"Pepe's Party"
```
o escapando el apóstrofe con una barra invertida \:
```
>>> 'Pepe\'s Party'
'Pepe's Party'
```

Para ver tu nombre en letras mayúsculas, simplemente escribe:
```
>>> "Ola".upper()
'OLA'
```

¡Muy bien! Aqui estamos usando la función upper. Una función (como upper()) es un conjunto de instrucciones que Python tiene que realizar sobre un objeto determinado (en este caso "Ola") una vez que se llama.

Si quisieras saber el número de letras que contiene tu nombre, también existe una función para esto.
```
>>> len("Ola")
3
```

una buena pregunta es por qué a veces se llama a las funciones con un . al final de una cadena (como "Ola".upper()) y a veces se llama a una función y colocas la cadena entre paréntesis. 

Bueno, en algunos casos las funciones pertenecen a objetos, como upper(), que sólo puede ser utilizado sobre strings (upper() es una función de los objetos string). En este caso, llamamos método a esta función. 

Otra veces, las funciones no pertenecen a ningún objeto específico y pueden ser usados en diferentes objetos, como len(). Esta es la razón de por qué estamos pasando "Ola" como un parámetro a la función len.

__Observación__
Hasta ahora has aprendido sobre:

 * __Consola__ - teclear comandos (código) dentro de la consola de Python resulta en respuestas de Python;
 * __Números y Strings__ - en Python los números son usados para matemáticas y strings para objetos de texto;
 * __Operadores__ - como + y *, combina valores para producir uno nuevo;
 * __funciones__ - como *upper()* y *len()*, realizan opciones sobre los objetos.

Estos son los conocimientos básicos que puedes aprender de cualquier lenguaje de programación. 

### Variables
Un concepto importante en programación son las variables. Una variable no es más que un nombre para alguna cosa para que puedas usarla más tarde. 

Los programadores usan estas variables para almacenar datos, hacer su código más legible y así no tener que seguir recordando qué hace cada cosa.

Supongamos que queremos crear una nueva variable llamada name:
```
>>> name = "Ola"
```
Como te has dado cuenta, el programa no regresa algo como lo hacia antes. Entonces, ¿Cómo sabemos que la variable existe realmente? Simplemente introduce name y pulsa Enter:
```
>>> name
'Ola'
````
Podemos asignarle un valor distinto a esa misma variable, ya que siempre se quedará con el último valor asignado
```
>>> name = "Sonja"
>>> name
'Sonja'
```
Las variables tambien se pueden usar de funciones:
```
>>> len(name)
5
```
Las variables pueden ser cualquier cosa, como números. Prueba esto:
```
>>> a = 4
>>> b = 6
>>> a * b
24
```
Pero ¿qué pasa si usamos el nombre equivocado?
```
>>> city = "Tokyo"
>>> ctiy
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'ctiy' is not defined
```
¡Un error! Este error se llama NameError. Python te dará este error si intentas utilizar una variable que no ha sido definida aún. Si más adelante te encuentras con este error, verifica tu código para ver si no has escrito mal una variable.

### La función print()
Comencemos intentando lo siguiente:
```
>>> name = 'Maria'
>>> name
'Maria'
>>> print(name)
Maria
```
Cuando sólo escribes name, el intérprete de Python responde con la representación del string de la variable 'name', que son las letras M-a-r-i-a, rodeadas de comillas simples ''. Cuando dices print(name), Python va a "imprimir" el contenido de la variable a la pantalla, sin las comillas, que es mejor.

Como veremos después, print() también es útil cuando queremos imprimir cosas desde adentro de las funciones, o bien cuando queremos imprimir cosas en múltiples líneas.

### Listas
Además de strings y enteros, Python tiene diferentes tipos de objetos. Ahora vamos a introducir uno llamado *listas*. Las listas son exactamente lo que piensas que son: son objetos que son listas de otros objetos.
```
>>> []
[]
```
Lo anterior crea una lista vacía, ahora vamos a crear una lista de números de lotería. No queremos repetir todo el tiempo, así que los pondremos en una variable también:
```
>>> lottery = [3, 42, 12, 19, 30, 59]
```
Muy bien ya tenemos una lista que no es vacía, ¿Qué podemos hacer con ella? Vamos a ver cuántos números de lotería hay en la lista. ¿Tienes alguna idea de qué función deberías usar para eso? 
```
>>> len(lottery)
6
```
Claro la función *len()* puede darte el número de objetos en una lista. Ahora ordenemos la lista con la siguiente función:
```
>>> lottery.sort()
```
Esto no devuelve nada, sólo cambió el orden en que los números aparecen en la lista. Vamos a imprimir la lista otra vez y ver que pasó:
```
>>> print(lottery)
[3, 12, 19, 30, 42, 59]
```

Como puedes ver, los números en tu lista ahora están ordenados de menor a mayor. 
Para invertir el orden hacemos lo siguiente:
```
>>> lottery.reverse()
>>> print(lottery)
[59, 42, 30, 19, 12, 3]
```
Ahora agregemos  elemento a la lista, y lo hacemos así:
```
>>> lottery.append(199)
>>> print(lottery)
[59, 42, 30, 19, 12, 3, 199]
```

Si deseamos mostrar sólo el primer número, puedemos hacerlo mediante el uso de índices. Un índice es el número que te dice dónde en una lista aparece un ítem. La computadora inicia la cuenta en 0, así que el primer objeto en tu lista está en el índice 0, el siguiente es 1, y así sucesivamente. 
```
>>> print(lottery[0])
59
>>> print(lottery[1])
42
```
Como puedes ver, puedes acceder a diferentes objetos en tu lista utilizando el nombre de la lista y el índice del objeto dentro de corchetes.

Para diversión adicional, prueba algunos otros índices: 6, 7, 1000, -1, -6 ó -1000. A ver si se puedes predecir el resultado antes de intentar el comando. ¿Tienen sentido los resultados?

Puedes encontrar una lista de todos los métodos disponibles para listas en este capítulo de la documentación de Python: https://docs.python.org/2.7/tutorial/datastructures.html

### Diccionarios
Un diccionario es similar a una lista, pero accedes a valores usando una clave en vez de un índice. Una clave puede ser cualquier cadena o número. La sintaxis para definir un diccionario vacío es:
```
>>> {}
{}
```
Acabamos de crear un diccionario vacío. 
```
>>> participant = {'name': 'Ola', 'country': 'Poland', 'favorite_numbers': [7, 42, 92]}
```
Con este comando, acabamos de crear una variable *participant* con tres pares clave-valor:

 * La clave *name* apunta al valor 'Ola',
 * *country *apunta a 'Poland',y  
 * *favorite_numbers* apunta a [7, 42, 92] 

Podemos verificar el contenido de claves individuales con esta sintaxis:
```
>>> print(participant['name'])
Ola
```

Podemos observar que un diccionario es similar a una lista. Pero no necesitamos recordar el índice, si no el nombre.

¿Qué pasa si le pedimos a Python el valor de una clave que no existe?

¿Cuándo utilizar un diccionario o una lista? Bueno, eso es un buen punto para reflexionar. Sólo ten una solución en mente antes de mirar la respuesta en la siguiente línea.

 * ¿Sólo necesitas una secuencia ordenada de elementos? Usa una lista.
* ¿Necesitas asociar valores con claves, así puedes buscarlos eficientemente (usando las claves) más adelante? Utiliza un diccionario.

Los diccionarios, como las listas, son mutables, lo que significa que pueden ser cambiados después de ser creados. Puedes agregar nuevos pares clave/valor en el diccionario después de que ha sido creado, por ejemplo:
```
>>> participant['favorite_language'] = 'Python'
```
Como en las listas, el método len() en los diccionarios, devuelve el número de pares clave-valor en el diccionario. Adelante, escribe el comando:
```
>>> len(participant)
4
```

Puedemos utilizar el comando pop() para borrar un elemento en el diccionario. Por ejemplo, si deseas eliminar la entrada correspondiente a la clave 'favorite_numbers', sólo tienes que escribir el siguiente comando:
```
>>> participant.pop('favorite_numbers')
>>> participant
{'country': 'Poland', 'favorite_language': 'Python', 'name': 'Ola'}
```
Como podemos ver en la salida, el par de clave-valor correspondiente a la clave 'favorite_numbers' ha sido eliminado.

Además de esto, también puedes cambiar un valor asociado a una clave ya creada en el diccionario.
```
>>> participant['country'] = 'Germany'
>>> participant
{'country': 'Germany', 'favorite_language': 'Python', 'name': 'Ola'}
```

Como puedemos notar, el valor de la clave 'country' ha sido modificado de 'Poland' a 'Germany'.

__Observación__
En esta última parte hemos aprendido.
 * __Variables__ - nombres para los objetos que te permiten codificar más fácilmente y hacer el código más legible
 * __listas__ - listas de objetos almacenados en un orden determinado
 * __diccionarios__ - objetos almacenados como pares clave-valor

### Comparar cosas
Una gran parte de la programación incluye comparar cosas. ¿Qué es lo más fácil para comparar? Números, por supuesto. Vamos a ver cómo funciona:
```
>>> 5 > 2
True
>>> 3 < 1
False
>>> 5 > 2 * 2
True
>>> 1 == 1
True
>>> 5 != 2
True

```
Le dimos a Python algunos números para comparar.

¿Te preguntas por qué pusimos dos signos igual == al lado del otro para comparar si los números son iguales? Recuerda que Utilizamos un solo = para asignar valores a las variables. Siempre es necesario poner dos ==. Si deseas comprobar que las cosas son iguales entre sí. También podemos afirmar que las cosas no son iguales a otras. Para eso, utilizamos el símbolo !=, como mostramos en el ejemplo anterior.

Da dos tareas más a Python con los ignos mayor que y menor que:
```
>>> 6 >= 12 / 2
True
>>> 3 <= 2
False
> y < son fáciles, pero ¿qué es significa > = y < =? Se leen así:
```
Ahora intentemos lo siguiente:
```
>>> 6 > 2 and 2 < 3
True
>>> 3 > 2 and 2 < 1
False
>>> 3 > 2 or 2 < 1
True
```
Podemos darle a Python todos los números para comparar y siempre nos dará una respuesta. 

 * __and__ - si utilizas el operador and, ambas comparaciones deben ser True para que el resultado de todo el comando sea True
* __or__ - si utilizas el operador or, sólo una de las comparaciones tiene que ser True para que el resultado de todo el comando sea True

¿Has oído la expresión "comparar peras con manzanas"? Vamos a probar el equivalente en Python:
```
>>> 1 > 'python'
```
¿Cuál sera el resultado?

### Boolean
Por cierto, acabamos de aprender acerca de un nuevo tipo de objeto en Python. Se llama un *Boolean* -- y es probablemente el tipo más simple que existe.

Hay sólo dos objetos Boolean: - True - False

Pero para que Python entienda esto, es necesario que siempre lo escribas como True (primera letra mayúscula, con el resto de la letras minúsculas). true, TRUE, tRUE no funcionarán -- sólo True es correcto. (Lo mismo aplica a False también).

Los valores booleanos pueden ser variables, también. Ve el siguiente ejemplo:
```
>>> a = True
>>> a
True
```
También puedes hacerlo de esta manera:
```
>>> a = 2 > 5
>>> a
False
```

### Estructuras de Control
#### if/elif/else
Sintaxis
```
a=1111
if a>10:
    print('Python')
else:
    print('No Python')
```
Cuando necesitamos comprobar más de una condicion utilizamos elif tantas veces como sea necesario. También, mediante un else podemos destinar la ejecucicon de instrucciones si no se satisface ninguna condicion impuesta
```
a=1111
if a>10:
    print('Python')
elif a == 3:
    print('No Python')
else:
    print("Si Python")
```

#### while
Sintaxis
```
contador=1
while contador<5:
    print(contador)
    contador=contador+1
```
Permite ejecutar un bloque de instrucciones mientras se cumpla una condición. Las instrucciones que deseamos repetir deben estar identadas.

#### for
Sintaxis
```
lista=['a','b','c']
for elemento in lista:
    print(elemento)
```
Esta instrucción recorre los elementos en una lista, por cada uno de ellos, repite un bloque de instrucciones.

#### try / except
Para evitar que el programa/script se deje de ejecutar por un error , por ejemplo: 
```
variable1='A'
print(variable1<3)
```
utilizamos la sentencia try/excep
Sintaxis
```
variable1='A'
try:
    print(variable1<3)
except:
    print('no es un numero')
```
Es probable que durante la ejecución de nuestro código, ocurran errores. Podemos condicionar que, si ocurre un error, se ejecuten otras instrucciones.




