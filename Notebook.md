Fundamentos de Informática - Curso 2025-26

# LENGUAJE DE PROGRAMACIÓN PYTHON¶

# INTRODUCCIÓN¶

## Los lenguajes de programación¶

Un **lenguaje de programación** es un conjunto limitado de palabras y símbolos que representan procedimientos, cálculos, decisiones y operaciones que se pueden ejecutar en una computadora.

Los lenguajes de programación se pueden clasificar en:

### Lenguajes de BAJO NIVEL¶

Lenguajes directamente relacionados con las instrucciones que ejecuta el procesador.

- **Lenguaje Máquina**: utiliza instrucciones en forma de cadenas de números binarios (ceros y unos) reconocibles directamente por el procesador.

```
Ejemplo de instrucción del procesador x86: 1011 0000 0110 0001
 Mueve (1011) al registro AL (0000) del procesador el número hexadecimal 61 (01100001)

```
- **Lenguaje Ensamblador**: Lenguaje de bajo nivel que utiliza mnemotécnicos para representar instrucciones y direcciones simbólicas.

```
 Ejemplo anterior: MOV AL,61h
```

Ventajas: mayor adaptación al equipo, máxima velocidad con mínimo uso de memoria.

Inconvenientes: imposibilidad de escribir código independiente de la máquina, mayor dificultad en la programación y en la comprensión de los programas.

### Lenguajes de ALTO NIVEL¶

Lenguajes que utilizan un repertorio de instrucciones complejas siguiendo unas estrictas reglas gramaticales (sintaxis del lenguaje).

No existe relación directa entre estas instrucciones y las que ejecuta el procesador.

Ejemplos: Basic, C, C++, C#, Cobol, Fortran, Java, Pascal, Perl, PHP, Python, Lisp, Ada, Prolog, etc…

```python
Ejemplo de instrucción del procesador x86:  1011 0000 0110 0001
  Mueve (1011) al registro AL (0000) del procesador el número hexadecimal 61 (01100001)
```

```python
Ejemplo de instrucción del procesador x86:  1011 0000 0110 0001
  Mueve (1011) al registro AL (0000) del procesador el número hexadecimal 61 (01100001)
```

## Compiladores e intérpretes¶

### Lenguajes COMPILADOS¶

La ejecución de programas escritos en un lenguaje compilado requiere la traducción previa de todo el código fuente a código máquina (Código objeto).

La herramienta que utilizamos para dicha traducción se llama **Compilador**.
El programa desarrollado nunca se ejecuta mientras haya errores en el código fuente.

### Lenguajes INTERPRETADOS¶

La ejecución de programas escritos en un lenguaje interpretado requiere solamente la traducción a código máquina de la instrucción que se va a ejecutar en ese momento.

La herramienta que utilizados para la traducción/ejecución se llama **Interprete**.

El programa desarrollado puede ejecutarse aunque haya errores en el código fuente. Solo se detecta el error cuando se ejecuta la instrucción errónea.

## Estilos de programación¶

Permite 3 modos o estilos de programación (paradigmas):

### Programación imperativa¶

Conjunto de instrucciones que se ejecutan una tras otra (pasos de ejecución) de forma secuencial.
En la ejecución de estas instrucciones se van cambiando los valores de las variables y, dependiendo de estos valores, se modifica el flujo de control de la ejecución del programa.

```python
n = 5
factorial = 1
while n>1:
  factorial=factorial*n
  n=n-1
print("Factorial de 5 =",factorial)  # Factorial de 5 = 120
```

```python
n = 5
factorial = 1
while n>1:
  factorial=factorial*n
  n=n-1
print("Factorial de 5 =",factorial)  # Factorial de 5 = 120
```

```python
n = 5
factorial = 1
while n>1:
  factorial=factorial*n
  n=n-1
print("Factorial de 5 =",factorial)  # Factorial de 5 = 120
```

### Programación funcional¶

El código es una secuencia de declaración de funciones.

No existen asignación de variables, las funciones se llaman entre ellas y las repeticiones de instrucciones se sustituyen por recursividad (cuando una función se llama a si misma).

```python
def doble(x):
  return x+x
def triple(x):
  return doble(x)+x
def factorial(n):
  if n>1:
    return n*factorial(n-1)
  else:
    return 1
```

```python
def doble(x):
  return x+x
def triple(x):
  return doble(x)+x
def factorial(n):
  if n>1:
    return n*factorial(n-1)
  else:
    return 1
```

```python
def doble(x):
  return x+x
def triple(x):
  return doble(x)+x
def factorial(n):
  if n>1:
    return n*factorial(n-1)
  else:
    return 1
```

### Programación orientada a objetos¶

El código se organiza en unidades denominadas clases, de las cuales se crean objetos que se relacionan entre sí para conseguir un objetivo.

Forma de programación más cercana a la realidad donde cada elemento persona/cosa (objetos) con sus características que lo identifica (atributos) son capaces de realizar determinadas acciones (métodos).

```python
class Persona:
  # Atributos
  nombre = "Pedro"
  # Métodos
  def saludo(self):
    print("hola",self.nombre)
    return
  def cambiaNombre(self,nuevo):
    self.nombre = nuevo
    return
```

```python
class Persona:
  # Atributos
  nombre = "Pedro"
  # Métodos
  def saludo(self):
    print("hola",self.nombre)
    return
  def cambiaNombre(self,nuevo):
    self.nombre = nuevo
    return
```

```python
class Persona:
  # Atributos
  nombre = "Pedro"
  # Métodos
  def saludo(self):
    print("hola",self.nombre)
    return
  def cambiaNombre(self,nuevo):
    self.nombre = nuevo
    return
```

```python
hombre = Persona()
hombre.saludo()                     # hola Pedro
hombre.cambiaNombre("Alejandro")
hombre.saludo()                     # hola Alejandro
```

```python
hombre = Persona()
hombre.saludo()                     # hola Pedro
hombre.cambiaNombre("Alejandro")
hombre.saludo()                     # hola Alejandro
```

```python
hombre = Persona()
hombre.saludo()                     # hola Pedro
hombre.cambiaNombre("Alejandro")
hombre.saludo()                     # hola Alejandro
```

## El lenguaje Python¶

Python es un lenguaje de programación de alto nivel multiparadigma y de propósito general creado por Guido van Rossum en 1990.

Actualmente el lenguaje lo desarrollan y mantiene la “Python Software Foundation” (www.python.org)

- Es de código abierto (certificado por la OSI).
- Es interpretable y compilable.
- Es fácil de aprender gracias a que su sintaxis es bastante legible para los humanos.
- Es fácilmente extensible e integrable en otros lenguajes (C, java).
- Mantenido por una gran comunidad de desarrolladores y hay multitud de recursos para su aprendizaje.

### Modos de ejecución¶

Interpretado en la consola de Python

El usuario introduce una instrucción y el interprete la ejecuta. Similar a una calculadora

Interpretado en fichero

El usuario crea un fichero de texto con una secuencia de instrucciones (programa) y el interperte ejecuta de forma secuencial todas las instrucciones contenidas en el fichero.

### Entornos de programación¶

IDLE PYTHON

Para escribir y ejecutar código en Python instalaremos el interprete y el entorno de desarrollo (**IDLE**) que descargaremos de la página de la fundación: [https://www.python.org/downloads](https://www.python.org/downloads)

Ejecutando el IDLE de Python entramos en la consola (shell) donde podremos ejecutar instrucciones de manera interactiva.

Desde el Shell podremos lanzar el Editor que nos permitirá crear y ejecutar (Run) el fichero o (módulo) con la extensión "**.py**". Este fichero contendrá las líneas de código de nuestro programa.

Manual completo del IDLE de Python: [https://docs.python.org/es/3/library/idle.html](https://docs.python.org/es/3/library/idle.html)

THONNY

Se puede descargar gratuitamente de [https://thonny.org/](https://thonny.org/).

En Windows ofrece versiones portables para los alumnos que no deséen instalarla en su Sistema Operativo.

# VARIABLES¶

Una variable es el **nombre** que se utiliza para referirse a un objeto que reside en la memoria.

Cada variable debe tener un nombre **único** llamado identificador.

A diferencia de otros lenguajes no tienen asociado un tipo y no es necesario declararlas antes de usarlas (**tipado dinámico**).

El **nombre** de la variable debe respetar las siguientes reglas:

- Comienzar siempre por una **letra**, seguida de otras letras o números.
- No utilizar **palabras reservadas** del lenguaje: *False None True **peg_parser** and as assert async await break class continue def del elif else except finally for from global if import in is lambda nonlocal not or pass raise return try while with yield*.

Para asignar un valor a una variable se utiliza el operador **=**. Este operador permite asignar valores a mas de una variable con una sola instrucción (**asignación múltiple**).

**id(variable)** : Devuelve la dirección de memoria a la que apunta la variable (donde se encuentra el objeto).

**del(variable)** : Borra una variable.

Por economía del lenguaje, nos tomaremos la licencia de hablar de "guardar un valor en una variable" en vez de "guardar el valor en un objeto y asociar una variable al objeto".

```python
lenguaje = 'Python'
id(lenguaje)  # 138149071795632
id('Python')  # 138149071795632
x = 3.14
y = 3 + 2
a1,a2 = 1,2   # Asignación múltiple  a1 = 1 , a2 = 2
x,y = y,x     # Intercambio de valores
x += 2        # Incremento (equivale a x=x+2)
x -= 1        # Decremento (equivale a x=x-1)
x = None      # Valor no definido
del(x)        # Elimina la variable
```

```python
lenguaje = 'Python'
id(lenguaje)  # 138149071795632
id('Python')  # 138149071795632
x = 3.14
y = 3 + 2
a1,a2 = 1,2   # Asignación múltiple  a1 = 1 , a2 = 2
x,y = y,x     # Intercambio de valores
x += 2        # Incremento (equivale a x=x+2)
x -= 1        # Decremento (equivale a x=x-1)
x = None      # Valor no definido
del(x)        # Elimina la variable
```

```python
lenguaje = 'Python'
id(lenguaje)  # 138149071795632
id('Python')  # 138149071795632
x = 3.14
y = 3 + 2
a1,a2 = 1,2   # Asignación múltiple  a1 = 1 , a2 = 2
x,y = y,x     # Intercambio de valores
x += 2        # Incremento (equivale a x=x+2)
x -= 1        # Decremento (equivale a x=x-1)
x = None      # Valor no definido
del(x)        # Elimina la variable
```

# TIPOS DE DATOS SIMPLES¶

- **Números** (numbers) : 0 , -1 , 3.1415
- **Cadenas** (strings) : 'Hola' , "Adiós"
- **Booleanos** (boolean) : True , False

Estos datos son **inmutables**, es decir, una vez creados en la memoria su valor es constante y no puede cambiar.

La clase a la que pertenece un dato (objeto) se obtiene con la función **type()**.

## NÚMEROS (clases int y float)¶

Secuencia de dígitos que representan números.

Pueden incluir el ' **-** ' para negativos, el ' **.** ' para decimales y la ' **e** ' para expresar potencias de 10 en notación científica.

Pueden ser **enteros** (clase int) o **reales** (clase float).

### Operadores aritméticos¶

```
+ (suma) - (resta) * (producto) / (cociente) ** (potencia)
// (cociente división entera) % (resto división entera)
```

```python
+ (suma)  - (resta)  * (producto)  / (cociente)  ** (potencia)
// (cociente división entera)  % (resto división entera)
```

```python
+ (suma)  - (resta)  * (producto)  / (cociente)  ** (potencia)
// (cociente división entera)  % (resto división entera)
```

Orden de prioridad de evaluación

```
Funciones predefinidas >> Productos y cocientes >> Sumas y restas

```

Se puede saltar el orden de evaluación utilizando paréntesis **( )**.

```python
Funciones predefinidas >> Productos y cocientes >> Sumas y restas
```

```python
Funciones predefinidas >> Productos y cocientes >> Sumas y restas
```

### Operadores lógicos¶

Devuelven un valor lógico o booleano True/False:

```
== (igual que) != (distinto de)
< (menor que) > (mayor que)
<= (menor o igual que) >= (mayor oigual que)
```

```python
==  (igual que)           !=  (distinto de)
<   (menor que)           >   (mayor que)
<=  (menor o igual que)   >=  (mayor oigual que)
```

```python
==  (igual que)           !=  (distinto de)
<   (menor que)           >   (mayor que)
<=  (menor o igual que)   >=  (mayor oigual que)
```

```python
type(4.5)   # float
type(-1)    # int
type(4e5)   # float
2+3         # 5
5*-2        # -10
5/2         # 2.5
5//2        # 2
5%2         # 1
(2+3)**2    # 25
3==3        # True
3.1<=3      # False
-1!=1       # True
```

```python
type(4.5)   # float
type(-1)    # int
type(4e5)   # float
2+3         # 5
5*-2        # -10
5/2         # 2.5
5//2        # 2
5%2         # 1
(2+3)**2    # 25
3==3        # True
3.1<=3      # False
-1!=1       # True
```

```python
type(4.5)   # float
type(-1)    # int
type(4e5)   # float
2+3         # 5
5*-2        # -10
5/2         # 2.5
5//2        # 2
5%2         # 1
(2+3)**2    # 25
3==3        # True
3.1<=3      # False
-1!=1       # True
```

### Funciones con numeros¶

**int(c,b)** : Devuelve el entero representado en base **b** que contiene la cadena **c**.

**bin(i)** : Devuelve una cadena con el entero **i** representado en **binario**.

**hex(i)** : Devuelve una cadena con el entero **i** representado en **hexadecimal**.

**oct(i)** : Devuelve una cadena con el entero **i** representado en **octal**.

**round(f,d)** : Redondea el número real **f** con **d** decimales. Si se omite d redondea sin decimales (el resultado seguirá siendo **float**)

```python
int('1010',2)  # 10
bin(10)        # '0b1010'
hex(10)        # '0xa'
oct(10)        # '0o12'
```

```python
int('1010',2)  # 10
bin(10)        # '0b1010'
hex(10)        # '0xa'
oct(10)        # '0o12'
```

```python
int('1010',2)  # 10
bin(10)        # '0b1010'
hex(10)        # '0xa'
oct(10)        # '0o12'
```

## CADENAS (clase str)¶

Secuencia de caracteres alfanuméricos que representan un texto.

Se escriben entre comillas sencillas **'** o dobles **"**.

```
Ejemplos de cadenas: 'Python' "123" 'True' 'A'
Cadena vacía: '' ""
Cadena con un espacio: ' ' " "
Cambio o salto de línea: '\n' "\n"
Tabulador: '\t' "\t"
```

```python
Ejemplos de cadenas: 'Python'  "123"  'True'  'A'
Cadena vacía: ''  ""
Cadena con un espacio: ' '  " "
Cambio o salto de línea: '\n'  "\n"
Tabulador: '\t'  "\t"
```

```python
Ejemplos de cadenas: 'Python'  "123"  'True'  'A'
Cadena vacía: ''  ""
Cadena con un espacio: ' '  " "
Cambio o salto de línea: '\n'  "\n"
Tabulador: '\t'  "\t"
```

### Acceso a los elementos de una cadena¶

Cada carácter tiene asociado un índice que permite acceder a él.

```
Cadena " P y t h o n "
Índice positivo 0 1 2 3 4 5
Índice negativo -6 -5 -4 -3 -2 -1

```

**c[i]** : Devuelve el carácter de la cadena **c** con el índice **i**. El índice del primer carácter de la cadena = **0**. Se pueden utilizar índices negativos para recorrer la cadena del final al principio. El índice del último carácter de la cadena = **-1**.

**c[i:j]** : Devuelve la subcadena de **c** desde el carácter con el índice **i** hasta el carácter con el índice **j-1**.

**c[i:j:k]** : Devuelve la subcadena de **c** desde el carácter con el índice **i** hasta el carácter con el índice **j-1** con saltos de **k** caracteres.

```python
Cadena            " P   y   t   h   o   n "
Índice positivo     0   1   2   3   4   5
Índice negativo    -6  -5  -4  -3  -2  -1
```

```python
Cadena            " P   y   t   h   o   n "
Índice positivo     0   1   2   3   4   5
Índice negativo    -6  -5  -4  -3  -2  -1
```

```python
c = 'Universidad Miguel Hernandez'
c[2]      # 'i'
c[3:7]    # 'vers'
c[1:6:2]  # 'nvr'
```

```python
c = 'Universidad Miguel Hernandez'
c[2]      # 'i'
c[3:7]    # 'vers'
c[1:6:2]  # 'nvr'
```

```python
c = 'Universidad Miguel Hernandez'
c[2]      # 'i'
c[3:7]    # 'vers'
c[1:6:2]  # 'nvr'
```

### Operaciones con cadenas¶

**c1 + c2** : Devuelve la cadena resultado de concatenar las cadenas **c1** y **c2**.

**c * n** : Devuelve la cadena resultado de concatenar **n** copias de la cadena **c**.

**c1 in c2** : Devuelve True si **c2** contiene la cadena **c1**.

**c1 not in c2** : Devuelve True si **c2** no contiene la cadena **c1**.

**c1 == c2** : Devuelve True si la cadena **c1** es igual que la cadena
**c2**.

**c1 > c2** : Devuelve True si la cadena **c1** sucede a la cadena **c2**.

**c1 < c2** : Devuelve True si la cadena **c1** antecede a la cadena **c2**.

**c1 >= c2** : Devuelve True si la cadena **c1** sucede o es igual a la cadena **c2**.

**c1 <= c2** : Devuelve True si la cadena **c1** antecede o es igual a la cadena **c2**.

**c1 != c2** : Devuelve True si la cadena **c1** es distinta de la cadena **c2**.

Distingue entre mayúsculas y minúsculas.

 Utilizan el orden establecido en el código [ASCII](https://www.google.com/search?q=tabla+ascii+completa&sca_esv=8536d3cccb765549&sca_upv=1&hl=es&udm=2&biw=1099&bih=799&sxsrf=ADLYWIKEgzLeoxID2rSA-J71e12_MJVWGg%3A1727464884556&ei=tAX3ZsDPIdqLkdUPmuGp4AI&ved=0ahUKEwjA-biW7OOIAxXaRaQEHZpwCiwQ4dUDCBA&uact=5&oq=tabla+ascii+completa&gs_lp=Egxnd3Mtd2l6LXNlcnAiFHRhYmxhIGFzY2lpIGNvbXBsZXRhMgUQABiABDIFEAAYgAQyBhAAGAUYHjIGEAAYCBgeMgYQABgIGB4yBhAAGAgYHjIGEAAYCBgeMgYQABgIGB4yBhAAGAgYHjIHEAAYgAQYGEjxalDHLViCZXACeACQAQCYAWKgAYQNqgECMjC4AQPIAQD4AQGYAhagArMOwgINEAAYgAQYsQMYQxiKBcICChAAGIAEGEMYigXCAggQABiABBixA8ICEBAAGIAEGLEDGEMYgwEYigXCAgsQABiABBixAxiDAZgDAIgGAZIHBDIwLjKgB8l0&sclient=gws-wiz-serp).

```python
'Me gusta '+'Python'    # 'Me gusta Python'
'Python'*3              # 'PythonPythonPython'
'y' in 'Python'         # True
'Tho' not in 'Python'   # True
'Python' == 'python'    # False
'Python' < 'python'     # True
'a' > 'Z'               # True
'A' >= 'Z'              # False
'' < 'Python'           # True
```

```python
'Me gusta '+'Python'    # 'Me gusta Python'
'Python'*3              # 'PythonPythonPython'
'y' in 'Python'         # True
'Tho' not in 'Python'   # True
'Python' == 'python'    # False
'Python' < 'python'     # True
'a' > 'Z'               # True
'A' >= 'Z'              # False
'' < 'Python'           # True
```

```python
'Me gusta '+'Python'    # 'Me gusta Python'
'Python'*3              # 'PythonPythonPython'
'y' in 'Python'         # True
'Tho' not in 'Python'   # True
'Python' == 'python'    # False
'Python' < 'python'     # True
'a' > 'Z'               # True
'A' >= 'Z'              # False
'' < 'Python'           # True
```

### Funciones con cadenas¶

**len(c)** : Devuelve el número de caracteres de la cadena **c**.

**min(c)** : Devuelve el carácter menor de la cadena **c**.

**max(c)** : Devuelve el carácter mayor de la cadena **c**.

**chr(i)** : Devuelve una cadena con el caracter cuyo ascii es **i**

**ord(c)** : Devuelve el ascii del caracter que contiene la cadena **c**.

**c.upper()** : Devuelve la cadena con los mismos caracteres que la cadena **c** en mayúsculas.

**c.lower()** : Devuelve la cadena con los mismos caracteres que la cadena **c** minúsculas.

**c.title()** : Devuelve la cadena con los mismos caracteres que la cadena **c** con el primer carácter en mayúscula y el resto en minúsculas.

**c.find(subcadena)** : Busca **subcadena** en la cadena **c**. Devuelve la posición en la cadena **c** del primer carácter de la subcadena . Si no la encuentra devuelve **-1**.

**c.replace(c1,c2)** : Devuelve la cadena reemplazando las subcadenas **c1** por **c2**.

**c.split(delimitador)** : Devuelve la lista formada por las subcadenas que resultan de partir la cadena **c** usando como delimitador la cadena **delimitador**. Si no se especifica el delimitador utiliza por defecto el **espacio** en blanco.

```python
len('Python')             # 6
min('Python')             # 'P'
max('Python')             # 'y'
'Python'.upper()          # 'PYTHON'
'A,B,C'.split(',')        # ['A', 'B', 'C']
'I love Python'.split()   # ['I', 'love', 'Python']
chr(65)                   # 'A'
ord('A')                  # 65
```

```python
len('Python')             # 6
min('Python')             # 'P'
max('Python')             # 'y'
'Python'.upper()          # 'PYTHON'
'A,B,C'.split(',')        # ['A', 'B', 'C']
'I love Python'.split()   # ['I', 'love', 'Python']
chr(65)                   # 'A'
ord('A')                  # 65
```

```python
len('Python')             # 6
min('Python')             # 'P'
max('Python')             # 'y'
'Python'.upper()          # 'PYTHON'
'A,B,C'.split(',')        # ['A', 'B', 'C']
'I love Python'.split()   # ['I', 'love', 'Python']
chr(65)                   # 'A'
ord('A')                  # 65
```

### Cadenas formateadas¶

**f'cadena'** : La cadena formateada es un tipo de cadena que permite insertar en ellas datos números o cadenas de caracteres.

Se utilizan las llaves **{ }** (marcadores de posición) para señalar el lugar de inserción.

Sintaxis de los marcadores de posición:

- **{dato}** : Inserta el **dato** completo sin espacio adicional.
- **{dato:n}** : Reserva **n** caracteres e inserta el **dato** alineado **izquierda** (cadenas) y **derecha** (números).
- **`{dato:`**` : Reserva n caracteres e inserta el dato (entero/real/cadena) alineado izquierda. `

`
`

```python
f'Texto {45} Texto'             # 'Texto 45 Texto'
f'Texto {45:6} Texto'           # 'Texto     45 Texto'
f'Texto {45:>6} Texto'          # 'Texto     45 Texto'
f'Texto {45:^6} Texto'          # 'Texto   45   Texto'
f'Texto {45:<6} Texto'          # 'Texto 45     Texto'
f'Texto {3.1416:6.2f}'          # 'Texto   3.14'
f'Texto {3.1416:<6.2f} Texto'   # 'Texto 3.14   Texto'
f'Texto {"Hola":^6} Texto'      # 'Texto  Hola  Texto'
f"Texto {'Hola':^6} Texto"      # 'Texto  Hola  Texto'
f'Texto {'Hola':^6} Texto'      # ERROR
```

```python
f'Texto {45} Texto'             # 'Texto 45 Texto'
f'Texto {45:6} Texto'           # 'Texto     45 Texto'
f'Texto {45:>6} Texto'          # 'Texto     45 Texto'
f'Texto {45:^6} Texto'          # 'Texto   45   Texto'
f'Texto {45:<6} Texto'          # 'Texto 45     Texto'
f'Texto {3.1416:6.2f}'          # 'Texto   3.14'
f'Texto {3.1416:<6.2f} Texto'   # 'Texto 3.14   Texto'
f'Texto {"Hola":^6} Texto'      # 'Texto  Hola  Texto'
f"Texto {'Hola':^6} Texto"      # 'Texto  Hola  Texto'
f'Texto {'Hola':^6} Texto'      # ERROR
```

```python
f'Texto {45} Texto'             # 'Texto 45 Texto'
f'Texto {45:6} Texto'           # 'Texto     45 Texto'
f'Texto {45:>6} Texto'          # 'Texto     45 Texto'
f'Texto {45:^6} Texto'          # 'Texto   45   Texto'
f'Texto {45:<6} Texto'          # 'Texto 45     Texto'
f'Texto {3.1416:6.2f}'          # 'Texto   3.14'
f'Texto {3.1416:<6.2f} Texto'   # 'Texto 3.14   Texto'
f'Texto {"Hola":^6} Texto'      # 'Texto  Hola  Texto'
f"Texto {'Hola':^6} Texto"      # 'Texto  Hola  Texto'
f'Texto {'Hola':^6} Texto'      # ERROR
```

## DATOS LÓGICOS o BOOLEANOS (clase bool)¶

Contiene únicamente dos elementos **True** y **False** que representan los valores lógicos **verdadero** y **falso** respectivamente.

**False** tiene asociado el valor **0** y **True** tiene asociado el valor **1**.

### Operaciones con valores lógicos¶

```
== (igual que) > (mayor) < (menor)
>= (mayor o igual) <= (menor o igual) != (distinto de)

```

**not b** (negación) : Devuelve True si el dato booleano b es False y False en caso contrario.

**b1 and b2** : Devuelve True si los datos booleanos b1 y b2 son True y False en caso contrario.

**b1 or b2** : Devuelve True si alguno de los datos booleanos b1 o b2 son True, y False en caso contrario.

Tabla de verdad :
| x | y | not x | x and y | x or y |
|-----|---|-------|---------|--------|
|False|False|True |False|False|
|False|True |True |False|True |
|True|False|False|False|True|
|True|True|False|True|True|

```python
== (igual que)       >  (mayor)           <  (menor)
>= (mayor o igual)   <= (menor o igual)   != (distinto de)
```

```python
== (igual que)       >  (mayor)           <  (menor)
>= (mayor o igual)   <= (menor o igual)   != (distinto de)
```

```python
not True          # False
False or True     # True
True and False    # False
True and True     # True
True > False      # True
True != False     # True
```

```python
not True          # False
False or True     # True
True and False    # False
True and True     # True
True > False      # True
True != False     # True
```

```python
not True          # False
False or True     # True
True and False    # False
True and True     # True
True > False      # True
True != False     # True
```

## Conversión de datos primitivos simples¶

Las siguientes funciones convierten un dato de un tipo en otro, siempre y cuando la conversión sea posible:

**int()** : convierte a entero.

**float()** : convierte a real.

**str()** : convierte a cadena.

**bool()** : convierte a lógico.

```python
int(2.3)      # 2
int('12')     # 12
int(True)     # 1
float(3)      # 3.0
float('3.4')  # 3.4
float(True)   # 1.0
str(3)        # '3'
str(3.14)     # '3.14'
str(True)     # 'True'
bool(0)       # False
bool('')      # False
bool('Hola')  # True
```

```python
int(2.3)      # 2
int('12')     # 12
int(True)     # 1
float(3)      # 3.0
float('3.4')  # 3.4
float(True)   # 1.0
str(3)        # '3'
str(3.14)     # '3.14'
str(True)     # 'True'
bool(0)       # False
bool('')      # False
bool('Hola')  # True
```

```python
int(2.3)      # 2
int('12')     # 12
int(True)     # 1
float(3)      # 3.0
float('3.4')  # 3.4
float(True)   # 1.0
str(3)        # '3'
str(3.14)     # '3.14'
str(True)     # 'True'
bool(0)       # False
bool('')      # False
bool('Hola')  # True
```

# TIPOS DE DATOS COMPUESTOS¶

Un **iterable** es un tipo de objeto que puede ser recorrido o iterado elemento por elemento.

Los iterables más comunes son:

- **Contenedores** : objetos que pueden almacenar elementos en la memoria y que permiten comprobar si contiene ciertos valores (operador **in**).

- **Cadenas de texto** (clase str): Secuencia **ordenada** e **inmutable** de caracteres alfanuméricos
- **Listas** (clase list): Colecciones **ordenadas** y **mutables** de elementos.
- **Tuplas** (clase tuple): Colecciones **ordenadas** e **inmutables** de elementos.
- **Conjuntos** (clase set): Colecciones **no ordenadas** de elementos **únicos**.
- **Diccionarios** (clase dict): Colecciones de pares **clave-valor**.
- **Generadores** : objetos capaz de generar bajo demanda una secuencia iterable de elementos sin almacenarlos en la memoria.

- **Rangos** (clase range): Generador de secuencia **ordenada** de números enteros en **sucesión aritmética**.

## LISTAS (clase list)¶

Una lista es una secuencias ordenadas de objetos de distintos tipos.

Se construyen poniendo los elementos entre corchetes **[ ]** separados por comas:

[ objeto1 , objeto2 , … , objetoN ]

Se caracterizan por:

- Tienen **orden**.
- Pueden contener elementos de **distintos tipos**.
- Son **mutables**, pueden alterarse durante la ejecución de un programa.

**list(c)** : Crea una lista con los elementos del iterable **c**.

```python
type([])          # list
[1, "dos", True]
[1, [2, 3], 4]
list()            # []
list((1, 2, 3))   # [1, 2, 3]
list("Python")    # ['P', 'y', 't', 'h', 'o', 'n']
```

```python
type([])          # list
[1, "dos", True]
[1, [2, 3], 4]
list()            # []
list((1, 2, 3))   # [1, 2, 3]
list("Python")    # ['P', 'y', 't', 'h', 'o', 'n']
```

```python
type([])          # list
[1, "dos", True]
[1, [2, 3], 4]
list()            # []
list((1, 2, 3))   # [1, 2, 3]
list("Python")    # ['P', 'y', 't', 'h', 'o', 'n']
```

### Acceso a los elementos de una lista¶

Se utilizan los mismos operadores de acceso que para cadenas de caracteres.

**lista[i]** : Devuelve el elemento de lista con el índice i. El índice del primer elemento de lista es 0.

**lista[i:j]** : Devuelve la sublista desde el elemento con el índice i hasta el elemento con índice j-1.

**lista[i:j:k]** : Devuelve la sublista desde el elemento i hasta el elemento j-1, tomando elementos cada k.

```python
lista = [0,1,2,3,4,5,6,7]
lista[2]                  # 2
lista[0:5]                # [0, 1, 2, 3, 4]
lista[::2]                # [0, 2, 4, 6]
lista[-1:4:-1]            # [7, 6, 5]
```

```python
lista = [0,1,2,3,4,5,6,7]
lista[2]                  # 2
lista[0:5]                # [0, 1, 2, 3, 4]
lista[::2]                # [0, 2, 4, 6]
lista[-1:4:-1]            # [7, 6, 5]
```

```python
lista = [0,1,2,3,4,5,6,7]
lista[2]                  # 2
lista[0:5]                # [0, 1, 2, 3, 4]
lista[::2]                # [0, 2, 4, 6]
lista[-1:4:-1]            # [7, 6, 5]
```

### Operaciones que no modifican la lista¶

**lista.index(dato)** : Devuelve la posición que ocupa en lista el primer elemento con valor dato.

**lista.count(dato)** : Devuelve el número de veces que el valor dato está contenido en lista.

**lista1 + lista2** : Crea una nueva lista concatenando los elementos de lista1 y lista2.

```python
a = [1, 2, 2, 3, 2]
a.index(2)            # 1
a.count(2)            # 3
[1,2,3]+[6,7,8]       # [1, 2, 3, 6, 7, 8]
```

```python
a = [1, 2, 2, 3, 2]
a.index(2)            # 1
a.count(2)            # 3
[1,2,3]+[6,7,8]       # [1, 2, 3, 6, 7, 8]
```

```python
a = [1, 2, 2, 3, 2]
a.index(2)            # 1
a.count(2)            # 3
[1,2,3]+[6,7,8]       # [1, 2, 3, 6, 7, 8]
```

### Operaciones que modifican la lista¶

**lista.append(dato)** : Añade dato al final de lista.

**lista.insert(índice, dato)** : Inserta dato en la posición índice de lista y desplaza los elementos una posición a partir de la posición índice.

**lista.remove(dato)** : Elimina el primer elemento con valor dato de lista y desplaza los que están por detrás de él una posición hacia delante.

**lista.pop([índice])** : Devuelve el dato en la posición índice y lo elimina de lista, desplazando los elementos por detrás de él una posición hacia delante.

**lista.sort()** : Ordena los elementos de lista de acuerdo al orden predefinido, siempre que los elementos sean comparables.

**lista.reverse()** : invierte el orden de los elementos de lista.

```python
a = [1, 3]
b = [2, 4, 6]
a.append(5)       # a = [1, 3, 5]
a.extend([8, 9])  # a = [1, 3, 5, 8, 9]
a.insert(2,9)     # a = [1, 3, 9, 5, 8, 9]
a.remove(3)       # a = [1, 9, 5, 8, 9]
x = a.pop(3)      # a = [1, 9, 5, 9]   x = 8
a.sort()          # a = [1, 5, 9, 9]
a.reverse()       # a = [9, 9, 5, 1]
```

```python
a = [1, 3]
b = [2, 4, 6]
a.append(5)       # a = [1, 3, 5]
a.extend([8, 9])  # a = [1, 3, 5, 8, 9]
a.insert(2,9)     # a = [1, 3, 9, 5, 8, 9]
a.remove(3)       # a = [1, 9, 5, 8, 9]
x = a.pop(3)      # a = [1, 9, 5, 9]   x = 8
a.sort()          # a = [1, 5, 9, 9]
a.reverse()       # a = [9, 9, 5, 1]
```

```python
a = [1, 3]
b = [2, 4, 6]
a.append(5)       # a = [1, 3, 5]
a.extend([8, 9])  # a = [1, 3, 5, 8, 9]
a.insert(2,9)     # a = [1, 3, 9, 5, 8, 9]
a.remove(3)       # a = [1, 9, 5, 8, 9]
x = a.pop(3)      # a = [1, 9, 5, 9]   x = 8
a.sort()          # a = [1, 5, 9, 9]
a.reverse()       # a = [9, 9, 5, 1]
```

## TUPLAS (clase tuple)¶

Una tupla es una secuencias ordenadas de objetos de distintos tipos.

Se construyen poniendo los elementos entre paréntesis **( )** separados por comas.

( objeto1 , objeto2 , ... ,objetoN )

Se caracterizan por:

- Tienen **orden**.
- Pueden contener elementos de **distintos tipos**.
- Son **inmutables**, no pueden alterarse durante la ejecución de un programa.

**tuple(c)** : Crea una tupla con los elementos del iterable **c**.

```python
tuple()                 # ()
tuple((1, 2, 'hola'))   # (1, 2, 'hola')
tuple("Python")         # ('P', 'y', 't', 'h', 'o', 'n')
tuple([1, 2, 3])        # (1, 2, 3)
```

```python
tuple()                 # ()
tuple((1, 2, 'hola'))   # (1, 2, 'hola')
tuple("Python")         # ('P', 'y', 't', 'h', 'o', 'n')
tuple([1, 2, 3])        # (1, 2, 3)
```

```python
tuple()                 # ()
tuple((1, 2, 'hola'))   # (1, 2, 'hola')
tuple("Python")         # ('P', 'y', 't', 'h', 'o', 'n')
tuple([1, 2, 3])        # (1, 2, 3)
```

### Operaciones con tuplas¶

El **acceso a los elementos de una tupla** se realiza del mismo modo que en las **listas**. También se pueden obtener subtuplas de la misma manera que las sublistas.

Las **operaciones de listas que no modifican la lista** también son aplicables a las tuplas.

```python
t=(1,2,3,4,5,6)
t[2]              # 3
t[0:5]            # (1, 2, 3, 4, 5)
t[::2]            # (1, 3, 5)
t[4:1:-1]         # (5, 4, 3)
t.index(2)        # 1
t.count(2)        # 1
(1,2,3)+(6,7,8)   # (1, 2, 3, 6, 7, 8)
```

```python
t=(1,2,3,4,5,6)
t[2]              # 3
t[0:5]            # (1, 2, 3, 4, 5)
t[::2]            # (1, 3, 5)
t[4:1:-1]         # (5, 4, 3)
t.index(2)        # 1
t.count(2)        # 1
(1,2,3)+(6,7,8)   # (1, 2, 3, 6, 7, 8)
```

```python
t=(1,2,3,4,5,6)
t[2]              # 3
t[0:5]            # (1, 2, 3, 4, 5)
t[::2]            # (1, 3, 5)
t[4:1:-1]         # (5, 4, 3)
t.index(2)        # 1
t.count(2)        # 1
(1,2,3)+(6,7,8)   # (1, 2, 3, 6, 7, 8)
```

## CONJUNTOS (clase set)¶

Un conjunto es una colección no ordenada de objetos **únicos**.

Se construyen poniendo los elementos entre llaves { } separados por comas:

{ objeto1 , objeto2 , … , objetoN }

Se caracterizan por:

- **No tienen orden**. Los elementos no tienen una posición fija, no se puede acceder a los elementos con índices (como ocurre con las listas o las tuplas).
- **No se pueden repetir**.
- Pueden contener elementos de **distintos tipos**.
- Son **mutables**, pueden alterarse durante la ejecución de un programa.

**set(c)** : Crea un conjunto con los elementos del iterable **c**.

```python
x = set([0,1,2,4,4,6,'hola','hola',True,False])   # x = {0, 1, 2, 4, 6, 'hola'}
y = {0,1,2,4,4,6,'hola','hola',True,False}        # y = {0, 1, 2, 4, 6, 'hola'}
```

```python
x = set([0,1,2,4,4,6,'hola','hola',True,False])   # x = {0, 1, 2, 4, 6, 'hola'}
y = {0,1,2,4,4,6,'hola','hola',True,False}        # y = {0, 1, 2, 4, 6, 'hola'}
```

```python
x = set([0,1,2,4,4,6,'hola','hola',True,False])   # x = {0, 1, 2, 4, 6, 'hola'}
y = {0,1,2,4,4,6,'hola','hola',True,False}        # y = {0, 1, 2, 4, 6, 'hola'}
```

### Operaciones que no modifican el conjunto¶

**conjunto1 | conjunto2** : Unión conjunto1 y conjunto2 (elimina duplicados). Elementos que están en conjunto1 o conjunto2.

**conjunto1 & conjunto2** : Intersección de conjunto1 y conjunto2. Elementos que están en conjunto1 y conjunto2.

**conjunto1 - conjunto2** : Diferencia de conjunto1 y conjunto2. Elementos de conjunto1 que no están en conjunto2.

**conjunto1 == conjunto2** : True si conjunto1 y conjunto2 tienen los mismos elementos.

**conjunto1.issubset(conjunto2)** : True si conjunto1 es un subconjunto de conjunto2. Todos los elementos de conjunto1 están en conjunto2.

**conjunto1.symmetric_difference(conjunto2)** : Diferencia simétrica de conjunto1 – conjunto2. Elementos de conjunto1 y conjunto2 que solo están en uno de los dos conjuntos y no en la intersección.

**conjunto1.isdisjoint(conjunto2)** : True si conjunto1 y conjunto2 son disconexos. No comparten ningún elemento.

```python
s1 = {1,2,3,4,5}
s2 = {4,5,6,7,8}
s1|s2                         # {1, 2, 3, 4, 5, 6, 7, 8}
s1&s2                         # {4, 5}
s1-s2                         # {1, 2, 3}
s1==s2                        # False
{1,3}.issubset(s1)            # True
s1.symmetric_difference(s2)   # {1, 2, 3, 6, 7, 8}
s1.isdisjoint(s2)             # False
```

```python
s1 = {1,2,3,4,5}
s2 = {4,5,6,7,8}
s1|s2                         # {1, 2, 3, 4, 5, 6, 7, 8}
s1&s2                         # {4, 5}
s1-s2                         # {1, 2, 3}
s1==s2                        # False
{1,3}.issubset(s1)            # True
s1.symmetric_difference(s2)   # {1, 2, 3, 6, 7, 8}
s1.isdisjoint(s2)             # False
```

```python
s1 = {1,2,3,4,5}
s2 = {4,5,6,7,8}
s1|s2                         # {1, 2, 3, 4, 5, 6, 7, 8}
s1&s2                         # {4, 5}
s1-s2                         # {1, 2, 3}
s1==s2                        # False
{1,3}.issubset(s1)            # True
s1.symmetric_difference(s2)   # {1, 2, 3, 6, 7, 8}
s1.isdisjoint(s2)             # False
```

### Operaciones que modifican el conjunto¶

**conjunto.add(elemento)** : Añade elemento a conjunto.

**conjunto.discard(elemento)** : Elimina elemento de conjunto. Si no existe no elimina nada.

**conjunto.pop()** : Extrae y devuelve aleatoriamente un elemento de conjunto.

**conjunto.clear()** : Elimina todos los elementos de conjunto.

```python
s = {1,2,3}
s.add(4)                      # s = {1, 2, 3, 4}
s.discard(2)                  # s = {1, 3, 4}
x = s.pop()                   # s = {3, 4}  x = 1
s.clear()                     # s = {}
```

```python
s = {1,2,3}
s.add(4)                      # s = {1, 2, 3, 4}
s.discard(2)                  # s = {1, 3, 4}
x = s.pop()                   # s = {3, 4}  x = 1
s.clear()                     # s = {}
```

```python
s = {1,2,3}
s.add(4)                      # s = {1, 2, 3, 4}
s.discard(2)                  # s = {1, 3, 4}
x = s.pop()                   # s = {3, 4}  x = 1
s.clear()                     # s = {}
```

## DICCIONARIOS (clase dict)¶

Un diccionario es una colección de pares formados por una **clave** y un **valor** asociado a la clave.

Se construyen poniendo los pares entre llaves **{ }** separados por comas, y separando la clave del valor con dos puntos :

{ clave1:objeto1 , clave2:objeto2 , … , claveN:objetoN }

Se caracterizan por:

- **No tienen orden**.
- Pueden contener elementos de **distintos tipos**.
- **Son mutables**, pueden alterarse durante la ejecución de un programa.
- Las **claves son únicas**, no pueden repetirse en un mismo diccionario, y pueden ser de cualquier tipo de **datos inmutable**.

**dict(c:v)** : crea un diccionario a partir de pares **clave:valor** .

```python
# Diccionario con elementos de distintos tipos
dic1 = {'nombre':'Alfredo', 'despacho': 218, 'email':'asalber@ceu.es'}
# Diccionarios anidados
dic2 = {'nombre_completo':{'nombre': 'Alfredo', 'Apellidos': 'Sánchez Alberca' }, 'edad':34}
```

```python
# Diccionario con elementos de distintos tipos
dic1 = {'nombre':'Alfredo', 'despacho': 218, 'email':'asalber@ceu.es'}
# Diccionarios anidados
dic2 = {'nombre_completo':{'nombre': 'Alfredo', 'Apellidos': 'Sánchez Alberca' }, 'edad':34}
```

```python
# Diccionario con elementos de distintos tipos
dic1 = {'nombre':'Alfredo', 'despacho': 218, 'email':'asalber@ceu.es'}
# Diccionarios anidados
dic2 = {'nombre_completo':{'nombre': 'Alfredo', 'Apellidos': 'Sánchez Alberca' }, 'edad':34}
```

### Acceso a los elementos de un diccionario¶

**diccionario[clave]** : devuelve el **valor** de diccionario asociado a la **clave**. Si la **clave no existe** en el diccionario devuelve un **error**.

**diccionario.get(clave, valor)** : devuelve el valor de diccionario asociado a la clave clave. Si la **clave no existe** en diccionadio devuelve **valor** (si no se especifica un valor por defecto devuelve **None**).

```python
dic = {'nombre':'Alfredo', 'despacho': 218, 'email':'asalber@ceu.es'}
x = dic['nombre']                 # x = 'Alfredo'
x = dic['despacho']               # x = 218
x = dic.get('email')              # x = 'asalber@ceu.es'
x = dic.get('universidad','UMH')  # x = 'UMH'
# Diccionarios anidados
dic2 = {'nombre_completo':{'nombre': 'Alfredo', 'Apellidos': 'Sánchez Alberca' }, 'edad':34}
x = dic2['nombre_completo']['nombre']   # x = 'Alfredo'
```

```python
dic = {'nombre':'Alfredo', 'despacho': 218, 'email':'asalber@ceu.es'}
x = dic['nombre']                 # x = 'Alfredo'
x = dic['despacho']               # x = 218
x = dic.get('email')              # x = 'asalber@ceu.es'
x = dic.get('universidad','UMH')  # x = 'UMH'
# Diccionarios anidados
dic2 = {'nombre_completo':{'nombre': 'Alfredo', 'Apellidos': 'Sánchez Alberca' }, 'edad':34}
x = dic2['nombre_completo']['nombre']   # x = 'Alfredo'
```

```python
dic = {'nombre':'Alfredo', 'despacho': 218, 'email':'asalber@ceu.es'}
x = dic['nombre']                 # x = 'Alfredo'
x = dic['despacho']               # x = 218
x = dic.get('email')              # x = 'asalber@ceu.es'
x = dic.get('universidad','UMH')  # x = 'UMH'
# Diccionarios anidados
dic2 = {'nombre_completo':{'nombre': 'Alfredo', 'Apellidos': 'Sánchez Alberca' }, 'edad':34}
x = dic2['nombre_completo']['nombre']   # x = 'Alfredo'
```

### Operaciones que no modifican el diccionario¶

**diccionario.keys()** : Devuelve un iterador sobre las **claves** de diccionario.

**diccionario.values()** : Devuelve un iterador sobre los **valores** diccionario.

**diccionario.items()** : Devuelve un iterador sobre los pares **(clave,valor)** de diccionario.

```python
a = {'nombre':'Alfredo', 'despacho': 218, 'email':'asalber@ceu.es'}
a.keys()    # dict_keys(['nombre', 'despacho', 'email'])
a.values()  # dict_values(['Alfredo', 218, 'asalber@ceu.es'])
a.items()   # dict_items([('nombre', 'Alfredo'), ('despacho', 218), ('email', 'asalber@ceu.es')])
```

```python
a = {'nombre':'Alfredo', 'despacho': 218, 'email':'asalber@ceu.es'}
a.keys()    # dict_keys(['nombre', 'despacho', 'email'])
a.values()  # dict_values(['Alfredo', 218, 'asalber@ceu.es'])
a.items()   # dict_items([('nombre', 'Alfredo'), ('despacho', 218), ('email', 'asalber@ceu.es')])
```

```python
a = {'nombre':'Alfredo', 'despacho': 218, 'email':'asalber@ceu.es'}
a.keys()    # dict_keys(['nombre', 'despacho', 'email'])
a.values()  # dict_values(['Alfredo', 218, 'asalber@ceu.es'])
a.items()   # dict_items([('nombre', 'Alfredo'), ('despacho', 218), ('email', 'asalber@ceu.es')])
```

### Operaciones que modifican un diccionario¶

**diccionario[clave] = valor** : Añade a diccionario el par formado por la **clave** y el **valor**.

**diccionario1.update(d2)** : Añade los pares del diccionario2 al diccionario1.

**diccionario.pop(clave, alternativo)** : Devuelve el **valor** asociado a la **clave** y lo elimina de diccionario. Si la **clave no existe** devuelve el valor **alternativo**.

**diccionario.popitem()** : Devuelve la **tupla** formada por la **clave** y el **valor** del último par añadido a diccionario y lo elimina de diccionario.

**del diccionario[clave]** : Elimina del diccionario el par guardado con la **clave**.

**diccionario.clear()** : Elimina todos los pares de diccionario (diccionario vacío).

```python
a = {'nombre':'Alfredo','despacho': 218,'email':'asalber@ceu.es'}
a['universidad'] = 'CEU'  # a = {'nombre':'Alfredo','despacho': 218,'email':'asalber@ceu.es','universidad': 'CEU'}
x = a.pop('despacho')     # a = {'nombre': 'Alfredo', 'email': 'asalber@ceu.es', 'universidad': 'CEU'}   x = 218
x = a.popitem()           # a = {'nombre': 'Alfredo', 'email': 'asalber@ceu.es'}   x = ('universidad', 'CEU')
del a['email']            # a = {'nombre': 'Alfredo'}
a.clear()                 # a = {}
```

```python
a = {'nombre':'Alfredo','despacho': 218,'email':'asalber@ceu.es'}
a['universidad'] = 'CEU'  # a = {'nombre':'Alfredo','despacho': 218,'email':'asalber@ceu.es','universidad': 'CEU'}
x = a.pop('despacho')     # a = {'nombre': 'Alfredo', 'email': 'asalber@ceu.es', 'universidad': 'CEU'}   x = 218
x = a.popitem()           # a = {'nombre': 'Alfredo', 'email': 'asalber@ceu.es'}   x = ('universidad', 'CEU')
del a['email']            # a = {'nombre': 'Alfredo'}
a.clear()                 # a = {}
```

```python
a = {'nombre':'Alfredo','despacho': 218,'email':'asalber@ceu.es'}
a['universidad'] = 'CEU'  # a = {'nombre':'Alfredo','despacho': 218,'email':'asalber@ceu.es','universidad': 'CEU'}
x = a.pop('despacho')     # a = {'nombre': 'Alfredo', 'email': 'asalber@ceu.es', 'universidad': 'CEU'}   x = 218
x = a.popitem()           # a = {'nombre': 'Alfredo', 'email': 'asalber@ceu.es'}   x = ('universidad', 'CEU')
del a['email']            # a = {'nombre': 'Alfredo'}
a.clear()                 # a = {}
```

## RANGOS (clase range)¶

Los datos de tipo rango representan una **secuencia inmutable de números enteros en sucesión aritmética** (la diferencia entre dos términos consecutivos es siempre la misma).

No se considera un contenedor porque no almacena la secuencia de números, la genera bajo demanda cuando se itera sobre él.

**range(n)** : secuencia creciente de **n** números enteros consecutivos que empieza en **0** y acaba en **n-1**.

**range(m,n)** : secuencia creciente de **n** números enteros consecutivos que empieza en **m** y acaba en **n-1**.

**range(m,n,p)** : secuencia creciente de **n** números enteros consecutivos que empieza en **m** y acaba en **n-1**, aumentando los valores **de p en p**. Si **p negativo**, la secuencia será decreciente.

```python
list(range(4))      # [0, 1, 2, 3]
list(range(4,8))    # [4, 5, 6, 7]
list(range(4,10,2)) # [4, 6, 8]
list(range(-3))     # []
list(range(8,4))    # []
list(range(8,4,-1)) # [8, 7, 6, 5]
```

```python
list(range(4))      # [0, 1, 2, 3]
list(range(4,8))    # [4, 5, 6, 7]
list(range(4,10,2)) # [4, 6, 8]
list(range(-3))     # []
list(range(8,4))    # []
list(range(8,4,-1)) # [8, 7, 6, 5]
```

```python
list(range(4))      # [0, 1, 2, 3]
list(range(4,8))    # [4, 5, 6, 7]
list(range(4,10,2)) # [4, 6, 8]
list(range(-3))     # []
list(range(8,4))    # []
list(range(8,4,-1)) # [8, 7, 6, 5]
```

## OPERACIONES COMUNES CON ITERABLES¶

**print( *iterable )** : Imprime los elementos de un iterable

**cadena.join(iterable)** : Devuelve la cadena resultante de concatenar todos los objetos del iterable y colocando la **cadena** entre cada par de elementos. El **iterable** solo puede contener objetos de tipo **string**.

**len(iterable)** : Devuelve el número de elementos del iterable.

**min(iterable)** : Devuelve el mínimo elemento de un iterable (siempre que los datos sean comparables). En los diccionarios hace referencia a las claves.

**max(iterable)** : Devuelve el máximo elemento de un iterable (siempre que los datos sean comparables). En los diccionarios hace referencia a las claves.

**sum(iterable)** : Devuelve la suma de los elementos de un iterable (siempre que los datos se puedan sumar). En los diccionarios hace referencia a las claves.

**sorted(iterable)** : Devuelve una lista ordenada de un iterable

**dato in iterable** : Devuelve **True** si el dato pertenece al iterable o **False** en caso contrario. En los diccionarios hace referencia a las claves.

**any(iterable)** : Devuelve **True** si **algún** elemento es verdadero

**all(iterable)** : Devuelve **True** si **todos** los elementos del iterable son verdaderos

```python
numeros = [5, 0, 3, 1, 4]
print(numeros)                    # [5, 0, 3, 1, 4]
print(*numeros)                   # 5 0 3 1 4
s = '-'.join(['11','AA','BB'])    # s = '11-AA-BB'
s = '-'.join(map(str,numeros))    # s = '5-0-3-1-4'
n = len(numeros)                  # n = 5
minimo = min(numeros)             # minimo = 1
maximo = max(numeros)             # maximo = 5
suma = sum(numeros)               # suma = 13
ordenados = sorted(numeros)       # ordenados = [0, 1, 3, 4, 5]
b = 3 in numeros                  # b = True
x = any(numeros)                  # x = True  (valor distinto de cero considerado True)
y = all(numeros)                  # y = False (0 es considerado False)
```

```python
numeros = [5, 0, 3, 1, 4]
print(numeros)                    # [5, 0, 3, 1, 4]
print(*numeros)                   # 5 0 3 1 4
s = '-'.join(['11','AA','BB'])    # s = '11-AA-BB'
s = '-'.join(map(str,numeros))    # s = '5-0-3-1-4'
n = len(numeros)                  # n = 5
minimo = min(numeros)             # minimo = 1
maximo = max(numeros)             # maximo = 5
suma = sum(numeros)               # suma = 13
ordenados = sorted(numeros)       # ordenados = [0, 1, 3, 4, 5]
b = 3 in numeros                  # b = True
x = any(numeros)                  # x = True  (valor distinto de cero considerado True)
y = all(numeros)                  # y = False (0 es considerado False)
```

```python
numeros = [5, 0, 3, 1, 4]
print(numeros)                    # [5, 0, 3, 1, 4]
print(*numeros)                   # 5 0 3 1 4
s = '-'.join(['11','AA','BB'])    # s = '11-AA-BB'
s = '-'.join(map(str,numeros))    # s = '5-0-3-1-4'
n = len(numeros)                  # n = 5
minimo = min(numeros)             # minimo = 1
maximo = max(numeros)             # maximo = 5
suma = sum(numeros)               # suma = 13
ordenados = sorted(numeros)       # ordenados = [0, 1, 3, 4, 5]
b = 3 in numeros                  # b = True
x = any(numeros)                  # x = True  (valor distinto de cero considerado True)
y = all(numeros)                  # y = False (0 es considerado False)
```

**zip(iterable1,iterable2,...)** : Combina varios iterables emparejando sus elementos en tuplas. Devuelve in **iterador** que permite recorrer las tuplas generadas.

```python
nombres = ["Ana", "Luis", "Pedro"]
edades = [20, 25, 30]
print(list(zip(nombres, edades)))         # [('Ana', 20), ('Luis', 25), ('Pedro', 30)]
print(dict(zip(nombres, edades)))         # {'Ana': 20, 'Luis': 25, 'Pedro': 30}
```

```python
nombres = ["Ana", "Luis", "Pedro"]
edades = [20, 25, 30]
print(list(zip(nombres, edades)))         # [('Ana', 20), ('Luis', 25), ('Pedro', 30)]
print(dict(zip(nombres, edades)))         # {'Ana': 20, 'Luis': 25, 'Pedro': 30}
```

```python
nombres = ["Ana", "Luis", "Pedro"]
edades = [20, 25, 30]
print(list(zip(nombres, edades)))         # [('Ana', 20), ('Luis', 25), ('Pedro', 30)]
print(dict(zip(nombres, edades)))         # {'Ana': 20, 'Luis': 25, 'Pedro': 30}
```

**enumerate(iterable)** : Devuelve pares de índice y valor para cada elemento. Devuelve un **iterador** de los pares formados por un índice y el elemento correspondiente del iterable.

```python
frutas = ["manzana", "naranja", "pera"]
print(list(enumerate(frutas)))  # [(0, 'manzana'), (1, 'naranja'), (2, 'pera')]
```

```python
frutas = ["manzana", "naranja", "pera"]
print(list(enumerate(frutas)))  # [(0, 'manzana'), (1, 'naranja'), (2, 'pera')]
```

```python
frutas = ["manzana", "naranja", "pera"]
print(list(enumerate(frutas)))  # [(0, 'manzana'), (1, 'naranja'), (2, 'pera')]
```

**map(función,iterable)** : Aplica una función a cada elemento del iterable, devolviendo un **iterador** con los resultados.

```python
numeros = ['1', '2', '3', '4']
cuadrados = map(int, numeros)
print(list(cuadrados))        # [1, 2, 3, 4]
```

```python
numeros = ['1', '2', '3', '4']
cuadrados = map(int, numeros)
print(list(cuadrados))        # [1, 2, 3, 4]
```

```python
numeros = ['1', '2', '3', '4']
cuadrados = map(int, numeros)
print(list(cuadrados))        # [1, 2, 3, 4]
```

**filter(función_lógica,iterable)** : Filtra los elementos de in iterable, devolviendo un **iterador** con los que cumplen una condición

```python
def positivo(x):
  return x % 2 == 0

numeros = [1, 2, 3, 4, 5]
pares = filter(positivo, numeros)
print(list(pares))  # [2, 4]
```

```python
def positivo(x):
  return x % 2 == 0

numeros = [1, 2, 3, 4, 5]
pares = filter(positivo, numeros)
print(list(pares))  # [2, 4]
```

```python
def positivo(x):
  return x % 2 == 0

numeros = [1, 2, 3, 4, 5]
pares = filter(positivo, numeros)
print(list(pares))  # [2, 4]
```

**Comprensión de listas, tuplas y conjuntos** : Las comprensiones son una forma concisa de crear listas, tuplas o conjuntos a partir de iterables, aplicando operaciones o filtrados sobre los elementos. La sintaxis general es:

    **[ expresión for elemento in iterable if condición ]**

    **( expresión for elemento in iterable if condición )**

    **{ expresión for elemento in iterable if condición }**

donde:

- **expresión** : es la operación o transformación que se aplicará a cada elemento.
- **for** elemento **in** iterable : es el bucle que recorre el iterable.
- **if** condición (opcional) : filtra los elementos. Solo los elementos que cumplan con la condición serán incluidos en el iterable final.

```python
numeros = [1, 2, 3, 4, 5]
cuadrados = [n**2 for n in numeros]                       # cuadrados = [1, 4, 9, 16, 25]
dic_cuadrados = {x: x**2 for x in range(5)}               # dic_cuadrados = {0:0,1:1,2:4,3:9,4:16}
paresalcubo = [n**3 for n in numeros if n%2==0]           # paresalcubo = [8, 64]
edad = [(12,'pepe'),(47,'ramón'),(3,'luis'),(19,'raul')]
mayores = [n for e,n in edad if e>=18]                    # mayores = ['ramón', 'raul']
```

```python
numeros = [1, 2, 3, 4, 5]
cuadrados = [n**2 for n in numeros]                       # cuadrados = [1, 4, 9, 16, 25]
dic_cuadrados = {x: x**2 for x in range(5)}               # dic_cuadrados = {0:0,1:1,2:4,3:9,4:16}
paresalcubo = [n**3 for n in numeros if n%2==0]           # paresalcubo = [8, 64]
edad = [(12,'pepe'),(47,'ramón'),(3,'luis'),(19,'raul')]
mayores = [n for e,n in edad if e>=18]                    # mayores = ['ramón', 'raul']
```

```python
numeros = [1, 2, 3, 4, 5]
cuadrados = [n**2 for n in numeros]                       # cuadrados = [1, 4, 9, 16, 25]
dic_cuadrados = {x: x**2 for x in range(5)}               # dic_cuadrados = {0:0,1:1,2:4,3:9,4:16}
paresalcubo = [n**3 for n in numeros if n%2==0]           # paresalcubo = [8, 64]
edad = [(12,'pepe'),(47,'ramón'),(3,'luis'),(19,'raul')]
mayores = [n for e,n in edad if e>=18]                    # mayores = ['ramón', 'raul']
```

**Copia de iterables mutables (listas, conjuntos y diccionarios)** : Existen dos formas de copiar iterables mutables. En el caso de conjuntos serían:

- **Copia por referencia conjunto1 = conjunto2`** : Asocia la variable conjunto1 el mismo conjunto que tiene asociado la variable conjunto2, es decir, ambas variables apuntan a la misma dirección de memoria. Cualquier cambio que hagamos a través de conjunto1 o conjunto2 afectará al mismo conjunto.
- **Copia por valor conjunto1 = set(conjunto2)`** : Crea una copia del conjunto2 en una dirección de memoria diferente y se la asocia a conjunto1. Las variables apuntan a direcciones de memoria diferentes que contienen los mismos datos. Cualquier cambio que hagamos a través de conjunto1 no afectará al conjunto2 y viceversa.

```python
# copia por referencia
a = {'A', 'B', 'C'}   # a = {'A', 'B', 'C'}
b = a                 # a = {'A', 'B', 'C'}  b = {'A', 'B', 'C'}
x = b.pop()           # a = {'A', 'C'}  b = {'A', 'C'}  x = 'B'
# copia por valor
a = {'A', 'B', 'C'}   # a = {'A', 'B', 'C'}
b = set(a)            # a = {'A', 'B', 'C'}  b = {'A', 'B', 'C'}
x = b.pop()           # a = {'A', 'B', 'C'}  b = {'A', 'C'}  x = 'B'
```

```python
# copia por referencia
a = {'A', 'B', 'C'}   # a = {'A', 'B', 'C'}
b = a                 # a = {'A', 'B', 'C'}  b = {'A', 'B', 'C'}
x = b.pop()           # a = {'A', 'C'}  b = {'A', 'C'}  x = 'B'
# copia por valor
a = {'A', 'B', 'C'}   # a = {'A', 'B', 'C'}
b = set(a)            # a = {'A', 'B', 'C'}  b = {'A', 'B', 'C'}
x = b.pop()           # a = {'A', 'B', 'C'}  b = {'A', 'C'}  x = 'B'
```

```python
# copia por referencia
a = {'A', 'B', 'C'}   # a = {'A', 'B', 'C'}
b = a                 # a = {'A', 'B', 'C'}  b = {'A', 'B', 'C'}
x = b.pop()           # a = {'A', 'C'}  b = {'A', 'C'}  x = 'B'
# copia por valor
a = {'A', 'B', 'C'}   # a = {'A', 'B', 'C'}
b = set(a)            # a = {'A', 'B', 'C'}  b = {'A', 'B', 'C'}
x = b.pop()           # a = {'A', 'B', 'C'}  b = {'A', 'C'}  x = 'B'
```

# ESTRUCTURAS SECUENCIALES¶

En una estructura secuencial de un programa, las instrucciones se ejecutan una tras otra en el mismo orden en el que están escritas, sin tomar decisiones, hacer repeticiones ni desviarse del flujo establecido.

## ENTRADA / SALIDA DE DATOS¶

### Leer datos del teclado¶

Para asignar a una variable un valor introducido por teclado por el usuario se utiliza la instrucción:

**input(mensaje)** : Muestra la cadena **mensaje** por la terminal y devuelve una **cadena** con la entrada del usuario.

El valor devuelto siempre es una cadena, incluso cuando el usuario introduce un dato numérico.

Al ejecutarse esta función, el programa se detiene esperando que se escriba algo y se pulse la tecla **INTRO** .

Posteriormente, se utilizarán las **funciones de conversión de tipo** para transformar la cadena en el tipo de dato deseado.

```python
nombre = input('Introduce nombre: ')    # Introduce nombre: Pepe
entrada = input('Introduce edad: ')     # Introduce edad: 23
                                        # entrada = '23'
edad = int(entrada)                     # edad = 23
edad = int(input('Introduce edad: '))   # Introduce edad: 23
                                        # edad = 23
```

```python
nombre = input('Introduce nombre: ')    # Introduce nombre: Pepe
entrada = input('Introduce edad: ')     # Introduce edad: 23
                                        # entrada = '23'
edad = int(entrada)                     # edad = 23
edad = int(input('Introduce edad: '))   # Introduce edad: 23
                                        # edad = 23
```

```python
nombre = input('Introduce nombre: ')    # Introduce nombre: Pepe
entrada = input('Introduce edad: ')     # Introduce edad: 23
                                        # entrada = '23'
edad = int(entrada)                     # edad = 23
edad = int(input('Introduce edad: '))   # Introduce edad: 23
                                        # edad = 23
```

### Escribir datos en pantalla¶

Para mostrar un dato por la terminal se utiliza la instrucción:

**print( dato1 , ... , sep=' ' , end='\n' )** :

- **dato1, ...** : son los datos a imprimir separados por comas.
- **sep** : establece el separador entre los datos (por defecto es un espacio en blanco **' '**.
- **end** : indica la cadena final de la impresión (por defecto es un salto de línea **\n**.

**print( *contenedor , ... , sep=' ' , end='\n' )** : imprime todos los elementos del contenedor (cadena de caracteres, lista, etc.).

```python
nombre = input('Teclea tu nombre: ')    # Teclea tu nombre: Pepe
print('Mi nombre es',nombre)            # Mi nombre es Pepe
print('Mi nombre es',nombre,sep='')     # Mi nombre esPepe
print('Mi nombre es',nombre,sep='\n')   # Mi nombre es
                                        # Pepe
print('Mi nombre es',nombre,end='*')    # Mi nombre es Pepe*
print(f'Mi nombre es {nombre:^10}.')    # Mi nombre es    Pepe   .
lista=[1,'hola',2]
print(*lista , sep='-',end='*')         # 1-hola-2*
cadena='hola'
print(*cadena , sep='-')                # h-o-l-a
```

```python
nombre = input('Teclea tu nombre: ')    # Teclea tu nombre: Pepe
print('Mi nombre es',nombre)            # Mi nombre es Pepe
print('Mi nombre es',nombre,sep='')     # Mi nombre esPepe
print('Mi nombre es',nombre,sep='\n')   # Mi nombre es
                                        # Pepe
print('Mi nombre es',nombre,end='*')    # Mi nombre es Pepe*
print(f'Mi nombre es {nombre:^10}.')    # Mi nombre es    Pepe   .
lista=[1,'hola',2]
print(*lista , sep='-',end='*')         # 1-hola-2*
cadena='hola'
print(*cadena , sep='-')                # h-o-l-a
```

```python
nombre = input('Teclea tu nombre: ')    # Teclea tu nombre: Pepe
print('Mi nombre es',nombre)            # Mi nombre es Pepe
print('Mi nombre es',nombre,sep='')     # Mi nombre esPepe
print('Mi nombre es',nombre,sep='\n')   # Mi nombre es
                                        # Pepe
print('Mi nombre es',nombre,end='*')    # Mi nombre es Pepe*
print(f'Mi nombre es {nombre:^10}.')    # Mi nombre es    Pepe   .
lista=[1,'hola',2]
print(*lista , sep='-',end='*')         # 1-hola-2*
cadena='hola'
print(*cadena , sep='-')                # h-o-l-a
```

### Leer datos de fichero¶

Abrir y leer fichero

**open(nombre,'r')** : Abre el fichero llamado nombre en **modo lectura** (el argumento **‘ r ’** significa read) y devuelve un **objeto** que lo referencia.

Una vez abierto el fichero, se puede leer todo el contenido del fichero o se puede leer línea a línea.

**fichero.read()** : Lee todos los caracteres fasta el final del fichero y los devuelve como cadena de caracteres.

#### Cerrar fichero¶

**fichero.close()** : Cierra el fichero referenciado por el objeto fichero.

Cuando se termina de trabajar con un fichero conviene cerrarlo.

Si no se cierra explícitamente un fichero, Python intentará cerrarlo cuando estime que ya no se va a usar más.

```python
f = open('saludo.txt', 'r')
x = f.read()
print(f.read())
f.close()
```

```python
f = open('saludo.txt', 'r')
x = f.read()
print(f.read())
f.close()
```

```python
f = open('saludo.txt', 'r')
x = f.read()
print(f.read())
f.close()
```

### Escribir datos en un fichero¶

#### Crear fichero nuevo y escribir dados¶

**open(nombre,'w')** : Crea un fichero nuevo llamado nombre, lo abre en **modo escritura** (**‘w’** write) y devuelve un **objeto** que lo referencia.

Si el fichero ya existe se reemplazará por el nuevo.

El nombre puede contener la ruta completa hasta llegar al fichero.

**fichero.write(c)** : Escribe la cadena c en el fichero referenciado por fichero.

No añade ningún caracter adicional.

#### Añadir datos a un fichero existente¶

**open(nombre,'a')** : Abre el fichero llamado nombre en **modo añadir** (**‘a’** append) y devuelve un **objeto** que lo referencia.
Si el fichero no existe crea uno nuevo.

El nombre puede contener la ruta completa hasta llegar al fichero.

**fichero.write(c)** : Escribe la cadena c en el fichero referenciado por fichero.

#### Cerrar fichero¶

**fichero.close()** : Cierra el fichero referenciado por el objeto fichero.

Cuando se termina de escribir en un fichero hay que cerrarlo.

Si finaliza la ejecución del programa sin cerrar el fichero puede que las ultimas ordenes de escritura no se ejecuten completamente.

Si no se cierra explícitamente un fichero, Python intentará cerrarlo cuando estime que ya no se va a usar más.

Mientras esté abierto en modo escritura no se debe abrir por otra aplicación.

### EJERCICIOS¶

#### Numeros (clases int y float)¶

**Ejercicio 1001** : A partir del diámetro, calcular la circunferencia y superficie de un círculo.

```python
'''
Inicio
    leer diametro
    circunferencia = pi*diametro
    superficie = pi*(diametro/2)**2
    escribir circunferencia
    escribir superficie
Fin
'''
diametro = float(input('Introduce el diámetro: '))
circunferencia = 3.14*diametro
superficie = 3.14*(diametro/2)**2
print('La circunferencia es',circunferencia)
print('La superficie es',superficie)
```

```python
'''
Inicio
    leer diametro
    circunferencia = pi*diametro
    superficie = pi*(diametro/2)**2
    escribir circunferencia
    escribir superficie
Fin
'''
diametro = float(input('Introduce el diámetro: '))
circunferencia = 3.14*diametro
superficie = 3.14*(diametro/2)**2
print('La circunferencia es',circunferencia)
print('La superficie es',superficie)
```

```python
'''
Inicio
    leer diametro
    circunferencia = pi*diametro
    superficie = pi*(diametro/2)**2
    escribir circunferencia
    escribir superficie
Fin
'''
diametro = float(input('Introduce el diámetro: '))
circunferencia = 3.14*diametro
superficie = 3.14*(diametro/2)**2
print('La circunferencia es',circunferencia)
print('La superficie es',superficie)
```

**Ejercicio 1002** : Dados 2 números enteros distintos de cero, calcular el cuadrado de cada uno, su suma, resta, multiplicación y división; escribiendo el resultado de dichas operaciones.

**Ejercicio 1003** : Calcular el perímetro y superficie de un rectángulo.

**Ejercicio 1004** : Realizar la conversión de grados Celsius a grados Fahrenheit. El resultado se mostrará con un dígito decimal. (F=(9/5)C+32).

```python
'''
Inicio
    leer celsuis
    fahr = (9/5)*celsius+32
    escibir fahr
Fin
'''
celsius = float(input('Introduce º celsius= '))
fahr = (9/5)*celsius+32
print(f'{celsius} º celsius son {fahr:.1f} º fahr')
```

```python
'''
Inicio
    leer celsuis
    fahr = (9/5)*celsius+32
    escibir fahr
Fin
'''
celsius = float(input('Introduce º celsius= '))
fahr = (9/5)*celsius+32
print(f'{celsius} º celsius son {fahr:.1f} º fahr')
```

```python
'''
Inicio
    leer celsuis
    fahr = (9/5)*celsius+32
    escibir fahr
Fin
'''
celsius = float(input('Introduce º celsius= '))
fahr = (9/5)*celsius+32
print(f'{celsius} º celsius son {fahr:.1f} º fahr')
```

```python
def cel_far(celsius):
    fahr = (9/5)*celsius+32
    return fahr

celsius = float(input('Introduce º celsius= '))
print(f'{celsius} º celsius son {cel_far(celsius):.1f} º fahr')
```

```python
def cel_far(celsius):
    fahr = (9/5)*celsius+32
    return fahr

celsius = float(input('Introduce º celsius= '))
print(f'{celsius} º celsius son {cel_far(celsius):.1f} º fahr')
```

```python
def cel_far(celsius):
    fahr = (9/5)*celsius+32
    return fahr

celsius = float(input('Introduce º celsius= '))
print(f'{celsius} º celsius son {cel_far(celsius):.1f} º fahr')
```

**Ejercicio 1005** : Resolver la ecuación de 1º grado: ax + b = 0

**Ejercicio 1006** : Se desea invertir capital en un banco. ¿Cuánto dinero ganará al mes si el interés es el 2% mensual?

**Ejercicio 1007** : Un vendedor recibe sueldo base y 10% de comisión de sus ventas. ¿Cuánto dinero obtiene de comisiones por 3 ventas mensuales? ¿Cuál es el sueldo total (base y comisiones)?

**Ejercicio 1008** : Una empresa constructora vende terrenos con la forma de la figura. Realizar un algoritmo para obtener el área de un terreno de medidas de cualquier valor

**Ejercicio 1009** : Leer la fecha de nacimiento y la fecha actual e indicar cuantos meses ha vivido la persona. Para leer las fechas se pedirán 2 números enteros: mes y año.

**Ejercicio 1010`** : Calcular la nota final de Informática si la calificación se obtiene del 55% del promedio de 3 notas parciales, 30% del examen final y 15% del trabajo final.

**Ejercicio 1010** : Leer el número de hombres y de mujeres que hay en un grupo de estudiantes. Mostrar en pantalla el porcentaje de hombres y mujeres con un dígito decimal.

#### Cadenas de caracteres (clase str)¶

**Ejercicio 1101** : Crear el fichero “frase.txt” con la cadena de caracteres (frase) introducida por teclado

**Ejercicio 1102** : Crear el fichero “frase.txt” con la cadena de caracteres (frase) introducida por teclado. A continuación, leer el fichero "frase.txt" y mostrar su contenido en pantalla.

**Ejercicio 1103** : Pedir por teclado una cadena de caracteres (frase) y crear un fichero llamado “salida.txt” con la frase repetida N veces. Cada frase en una línea distinta.

```python
'''
Inicio
    leer frase y N
    crear cadena salida con frase N veces en N lineas
    Escribir cadena salida en fichero salida.txt
Fin
'''
frase = input('Frase=')
N = int(input('N='))
salida = (frase+'\n')*N
print(salida)
f = open('')
f.write()
```

```python
'''
Inicio
    leer frase y N
    crear cadena salida con frase N veces en N lineas
    Escribir cadena salida en fichero salida.txt
Fin
'''
frase = input('Frase=')
N = int(input('N='))
salida = (frase+'\n')*N
print(salida)
f = open('')
f.write()
```

```python
'''
Inicio
    leer frase y N
    crear cadena salida con frase N veces en N lineas
    Escribir cadena salida en fichero salida.txt
Fin
'''
frase = input('Frase=')
N = int(input('N='))
salida = (frase+'\n')*N
print(salida)
f = open('')
f.write()
```

**Ejercicio 1104** : Leer un fichero de texto llamado “entrada.txt”, eliminar los espacios y escribir el resultado en un fichero llamado “salida.txt”. Mostrar por pantalla el número total de caracteres leidos de "entrada.txt" y escritos en "salida.txt".

**Ejercicio 1105** : Leer por teclado una frase y mostrar en pantalla los 2 primeros caracteres de la frase, los 3 últimos caracteres de la frase y la frase completa sin espacios

#### Listas (clase list)¶

**Ejercicio 1201** : De la siguiente lista de listas l = [ [1,'pepe'] , [2,'ramón'] , [3,'luis'] ], extrae y muestra en pantalla los 3 nombres.

**Ejercicio 1202** : El fichero “numeros.txt” contiene una secuencia de números separados por un espacio. Imprimir en pantalla la suma de todos los números.

**Ejercicio 1203** : El fichero 'datos.txt' contiene en cada linea el nombre de un alumno. Mostrar en pantalla los nombres ordenados alfabéticamente separados por comas.

**Ejercicio 1204** : El fichero “numeros.txt” contiene una secuencia de números enteros separados por un espacio. Eliminar los repetidos y escribirlos separados por comas en el fichero “salida.txt”.

#### Tuplas (clase tuple)¶

**Ejercicio 1301** : Data la tupla t=(1,2,3,4,5,6), muestra en pantalla:

- Primer y último elemento.
- Todos los elementos menos el primero y el último.
- Los elementos que ocupan las posiciones pares.

**Ejercicio 1302** : Convierte la lista de listas lista1 = [ [1,'pepe'] , [2,'ramón'] , [3,'luis'] ] en una lisla de tuplas lista2 = [ (1,'pepe') , (2,'ramón') , (3,'luis') ]

**Ejercicio 1303** : El fichero 'datos.txt' contiene en cada linea el nombre y el numero de expediente (separados por comas) de los alumnos. Mostrar en pantalla una lista con los datos de cada alumno en formato tupla:

[ (nombre1,exp1) , (nombre2,exp2) , ... , (nombreN,expN) ]

#### Conjuntos (clase set)¶

**Ejercicio 1401** : Dados los conjuntos A={1,2,3,4} y B={3,4,5,6}, muestra en pantalla:

- Unión de ambos conjuntos
- Elementos que están en ambos conjuntos
- Elementos que están en A y que no están en B
- Elementos que sólo están en A o en B (no están en ambos)

**Ejercicio 1402** : El fichero 'datos.txt' contiene varios numeros separados por comas. Muestra en pantalla los números sin repetir.

**Ejercicio 1403** : Dado un archivo de texto 'archivo.txt', lee todas las palabras únicas del archivo (palabras sin repetir) y guárdalas en el fichero 'unicas.txt'.

**Ejercicio 1404** : Comparar el contenido de dos ficheros de texto "entrada1.txt" y "entrada2.txt" y mostrar los caracteres que tienen en común.

**Ejercicio 1405** : Comparar el contenido de dos ficheros de texto "entrada1.txt" y "entrada2.txt" y mostrar en pantalla los caracteres exclusivos de cada fichero.

**Ejercicio 1406** : Introduce por teclado varias palabras en minúsculas separadas por un espacio y muestre por pantalla las letras que se repiten en todas las palabras.

#### Diccionarios (clase dict)¶

**Ejercicio 1501** : Pedir un número del 1 al 7 y mostrar en pantalla a qué día de la semana corresponde. (utilizar Diccionarios)

#### Rangos (clase range)¶

**Ejercicio 1601** : Crea una Lista con una secuencia de números entre N1 y N2. Se supone que N1

# ESTRUCTURAS CONDICIONALES¶

La instrucción condicional permite evaluar el estado del programa y tomar decisiones sobre qué código ejecutar en función del mismo.

CONDICIONAL SIMPLE

```
if condición :
 # bloque código

```

Evalúa la expresión lógica **condición** y si es verdadera (True) ejecuta el **bloque de código**

CONDICIONAL DOBLE

```
if condición :
 # bloque código 1
else :
 # bloque código 2

```

Evalúa la expresión lógica **condición**, si es verdadera (True) ejecuta el **bloque de código 1** y si es falsa (False) ejecuta el **bloque de código 2**.

CONDICIONAL MULTIPLE

```
if condición1 :
 # bloque código 1
elif condición2 :
 # bloque código 2
elif condición3 :
 # bloque código 3
...
else :
 # bloque código N

```

Evalúa la expresión lógica **condición1** y si es verdadera (True) ejecuta el **bloque de código 1** y salta al final de la estructura; si no, evalúa la condición2 y si es verdadera (True) ejecuta el **bloque de codigo 2** y salta al final de la estructura,... y así sucesivamente hasta que una de las condiciones se cumpla.

Si ninguna condición es cierta, entra en el **else** (en caso contrario) y ejecuta el **bloque de código N**.

Puede contener varios bloques **elif** pero solo un **else** al final (opcional).

Un **BLOQUE DE CÓDIGO** es un grupo de sentencias con la misma **indentación** o **sangrado**.

```python
if condición :
  # bloque código
```

```python
if condición :
  # bloque código
```

```python
# Condicional simple
edad = 50
if edad <= 18 :
  print('Menor de edad')
```

```python
# Condicional simple
edad = 50
if edad <= 18 :
  print('Menor de edad')
```

```python
# Condicional simple
edad = 50
if edad <= 18 :
  print('Menor de edad')
```

```python
# Condicional doble
edad = 14
if edad <= 18 :
  print('Menor de edad')
else:
print('Mayor de edad')
```

```python
# Condicional doble
edad = 14
if edad <= 18 :
  print('Menor de edad')
else:
print('Mayor de edad')
```

```python
# Condicional doble
edad = 14
if edad <= 18 :
  print('Menor de edad')
else:
print('Mayor de edad')
```

```python
# Condicional múltiple
empleados = 7
if empleados < 10 :
  print('Microempresa')
elif empleados < 50 :
  print('Pequeña empresa')
elif empleados < 250:
  print('Mediana empresa')
else:
  print('Gran empresa')
```

```python
# Condicional múltiple
empleados = 7
if empleados < 10 :
  print('Microempresa')
elif empleados < 50 :
  print('Pequeña empresa')
elif empleados < 250:
  print('Mediana empresa')
else:
  print('Gran empresa')
```

```python
# Condicional múltiple
empleados = 7
if empleados < 10 :
  print('Microempresa')
elif empleados < 50 :
  print('Pequeña empresa')
elif empleados < 250:
  print('Mediana empresa')
else:
  print('Gran empresa')
```

### EJERCICIOS¶

#### Condicional SIMPLE¶

**Ejercicio 2001** : Leer el nombre, primer apellido y segundo apellido de dos personas e indicar si pueden ser hermanos.

**Ejercicio 2002** : ¿Cuántos intereses genera un capital?. Si los intereses exceden los 7000€ se reinvierten. En este caso, ¿cuál es el capital?

**Ejercicio 2003** : Leer una hora (hora, minuto y segundo) e indicar si la hora es correcta, en caso contrario no indicar nada.

```python
h = int(input('hora='))
m = int(input('minutos='))
s = int(input('segundos='))
if h>=0 and h<=23 and m>=0 and m<=59 and s>=0 and s<=59 :
    print('la hora es correcta')
else:
    print('la hora es incorrecta')
```

```python
h = int(input('hora='))
m = int(input('minutos='))
s = int(input('segundos='))
if h>=0 and h<=23 and m>=0 and m<=59 and s>=0 and s<=59 :
    print('la hora es correcta')
else:
    print('la hora es incorrecta')
```

```python
h = int(input('hora='))
m = int(input('minutos='))
s = int(input('segundos='))
if h>=0 and h<=23 and m>=0 and m<=59 and s>=0 and s<=59 :
    print('la hora es correcta')
else:
    print('la hora es incorrecta')
```

#### Condicional DOBLE¶

**Ejercicio 2101** : Pedir dos números y decir si ambos son pares o impares.

**Ejercicio 2102** : Leer el nombre, primer apellido y segundo apellido de dos personas e indicar pueden ser hermanos o primos.

**Ejercicio 2103** : Comparar el contenido de dos ficheros de texto e indicar si son iguales.

**Ejercicio 2104** : Un alumno aprueba la asignatura si su promedio de 3 calificaciones es mayor o igual a 5, suspende en otro caso.

**Ejercicio 2105** : Leer la edad de una persona e indicar cuantas veces podría haber votado, suponiendo que hay elecciones cada 4 años y que puede votar cuando cumple los 18 años.

**Ejercicio 2106** : El fichero “dni.txt” contiene separados por un espacio, los DNI's de los empleados de una empresa. Mostrar en pantalla los DNIs repetidos y eliminarlos del fichero.

**Ejercicio 2107** : El fichero “dni.txt” contiene separados por un espacio, los DNI's de los empleados de una empresa. Pedir por teclado un DNI y comprobar si el empleado está en la empresa. Si no lo está, añadir el DNI al fichero dni.txt y mostrar en pantalla el mensaje 'DNI añadido'.

```python
fichero = open('dni.txt','r')
cadena = fichero.read()
fichero.close()
dni = input('dni=')
if   dni not in cadena   : #dni no está en la cadena
# añadir dni a dni.txt
    fichero1 = open('dni.txt','a')
    fichero1.write(' '+dni)
    fichero1.close()
    print(f'dni {dni} añadido a dni.txt')
```

```python
fichero = open('dni.txt','r')
cadena = fichero.read()
fichero.close()
dni = input('dni=')
if   dni not in cadena   : #dni no está en la cadena
# añadir dni a dni.txt
    fichero1 = open('dni.txt','a')
    fichero1.write(' '+dni)
    fichero1.close()
    print(f'dni {dni} añadido a dni.txt')
```

```python
fichero = open('dni.txt','r')
cadena = fichero.read()
fichero.close()
dni = input('dni=')
if   dni not in cadena   : #dni no está en la cadena
# añadir dni a dni.txt
    fichero1 = open('dni.txt','a')
    fichero1.write(' '+dni)
    fichero1.close()
    print(f'dni {dni} añadido a dni.txt')
```

#### Condicional MÚLTIPLE¶

**Ejercicio 2201** : Leer 3 números e imprimir el mayor de los 3. Si ningún número es el mayor de los tres, debe mostrar el mensaje “no hay mayor”.

**Ejercicio 2202** : Leer 3 números enteros y mostrarlos en pantalla de mayor a menor (separados por un punto). Por ejemplo: 97.32.15

**Ejercicio 2203** : En una tienda se hace un descuento sobre el valor de la compra según el color de la bolita que el cliente saque al pagar en caja. Si la bolita es blanca no hay descuento, si es verde el descuento es del 10%, si es amarilla es del 25%, si es azul del 50% y si es roja del 100%. ¿Cuál es el importe final de la compra?

**Ejercicio 2204** : Calcular la paga neta de un trabajador conociendo el número de horas trabajadas, salario_hora y porcentaje de impuestos. Las horas que excedan de 40 se abonan al doble del salario_hora. Presentar resultado con 2 decimales.

**Ejercicio 2205** : La empresa paga semanalmente a sus trabajadores un salario base por hora trabajada. Calcular el sueldo semanal de un trabajador si las primeras 40 horas se pagan al salario base, de la hora 41 a 50 se pagan al doble del salario base y de la hora 51 en adelante se pagan al triple del salario base.

**Ejercicio 2206** : En un almacén los artículos se codifican de la forma “**nnnct**”, donde **nnn** es el número de artículo, **c** es el color (”R” para rojo, “A” para azul) y **t** es la talla (“P” para pequeña, “G” para grande y “X” para extragrande). A partir del código de artículo introducido, indicar cuál es el número de artículo, cual su color y cual su talla. Deberá mostrar el mensaje “no codificado” si se introducen valores no contemplados en el color o la talla.

**Ejercicio 2207** : Leer una hora (hora, minuto y segundo) y mostrar la hora que sería un segundo más tarde (hora introducida + 1 segundo) en el formato “hora:minuto:segundo”

**Ejercicio 2208** : Leer el peso de un objeto en Kg (número entero) y mostrar esa cantidad en otra unidad de medida de masa en función de la opción numérica seleccionada: (1) Hectogramos, (2) Decagramos, (3) Gramos, (4) Decigramos, (5) Centigramos y (6) Miligramos. Mostrar en pantalla un menú con las opciones posibles.

**Ejercicio 2209** : Leer por teclado una cadena de texto con un correo electrónico e indicar por pantalla si es correcto o incorrecto. Para ello, la cadena debe contener lo siguiente y en este orden : *una o varias palabras separadas por un punto, un símbolo “@”, una o varias palabras separadas por un punto, un punto y una palabra a elegir entre “com”, “es” o “net”*.

**Ejercicio 2210`** : Leer por teclado una cadena de texto con una fecha en formato “dd/mm/aaaa”. Escribir en pantalla un mensaje que indique si la fecha es correcta o incorrecta. Para que sea correcta debe cumplir lo siguiente: día = 1...28/30/31 (en función del mes), mes = 1...12 y año = 2000...2024. Ejemplo: 23/12/2022

# ESTRUCTURAS CÍCLICAS¶

## CONDICIONALES (WHILE)¶

Repite la ejecución del bloque de código mientras la expresión lógica condición sea cierta.

```
while condición :
 # bloque código

```

En Python no existe la estructura de repetición con condición al final (DO-WHILE). Se puede implementar con la estructura WHILE si nos aseguramos que la condición se cumpla antes del bucle.

```python
while condición :
  # bloque código
```

```python
while condición :
  # bloque código
```

```python
# Pregunta al usuario por un número hasta que introduce 0.
num = 1
while num != 0:
    num = int(input('Introduce un número: '))
    print('>>>',num)
```

```python
# Pregunta al usuario por un número hasta que introduce 0.
num = 1
while num != 0:
    num = int(input('Introduce un número: '))
    print('>>>',num)
```

```python
# Pregunta al usuario por un número hasta que introduce 0.
num = 1
while num != 0:
    num = int(input('Introduce un número: '))
    print('>>>',num)
```

## ITERATIVAS (FOR)¶

Repite la ejecución del bloque de código para cada elemento de la secuencia, asignado dicho elemento a i en cada repetición.

```
for i in secuencia/contenedor:
 # bloque código

```

Se utiliza fundamentalmente para recorrer secuencias o colecciones de objetos: listas, tuplas, rangos, conjuntos o diccionarios.

```python
for i in secuencia/contenedor:
  # bloque código
```

```python
for i in secuencia/contenedor:
  # bloque código
```

```python
lista=[]
for x in [1,2,3,6,7]:
    lista.append(str(x))
print(lista)
```

```python
lista=[]
for x in [1,2,3,6,7]:
    lista.append(str(x))
print(lista)
```

```python
lista=[]
for x in [1,2,3,6,7]:
    lista.append(str(x))
print(lista)
```

```python
for letra in 'Hola':
    if letra in 'aeiou':
        print(letra, end='*')
```

```python
for letra in 'Hola':
    if letra in 'aeiou':
        print(letra, end='*')
```

```python
for letra in 'Hola':
    if letra in 'aeiou':
        print(letra, end='*')
```

```python
for i in range(10):
    print('*')
```

```python
for i in range(10):
    print('*')
```

```python
for i in range(10):
    print('*')
```

### EJERCICIOS¶

#### Números¶

**Ejercicio 3001** : Sumar N números enteros leídos desde el teclado.

```python
N = int(input('N='))
suma = 0
for i in range(N):
    numero = int(input('numero='))
    suma = suma + numero
print(f'Suma = {suma}')
```

```python
N = int(input('N='))
suma = 0
for i in range(N):
    numero = int(input('numero='))
    suma = suma + numero
print(f'Suma = {suma}')
```

```python
N = int(input('N='))
suma = 0
for i in range(N):
    numero = int(input('numero='))
    suma = suma + numero
print(f'Suma = {suma}')
```

```python
N = int(input('N='))
suma = 0
contador = 0
while  contador<N   :
    numero = int(input('numero='))
    suma = suma + numero
    contador = contador + 1
print(f'Suma = {suma}')
```

```python
N = int(input('N='))
suma = 0
contador = 0
while  contador<N   :
    numero = int(input('numero='))
    suma = suma + numero
    contador = contador + 1
print(f'Suma = {suma}')
```

```python
N = int(input('N='))
suma = 0
contador = 0
while  contador<N   :
    numero = int(input('numero='))
    suma = suma + numero
    contador = contador + 1
print(f'Suma = {suma}')
```

**Ejercicio 3002** : Leer varios números enteros desde el teclado e imprimir los positivos. Finalizar la entrada de números con el valor cero.

**Ejercicio 3003** : Calcular el promedio de N notas de un alumno.

**Ejercicio 3004** : Pedir dos números enteros positivos mayores que cero. Mostrar todos los números que van desde el menor al mayor, la suma y la media de todos ellos.

**Ejercicio 3005** : Que escriba las tablas de multiplicar del 0 al 10

**Ejercicio 3006** : Que muestre los números del 1 al 100 en una tabla de 10x10

**Ejercicio 3007** : Leer 10 números y obtener de cada uno su cubo y su cuarta. Escribir la suma de todos los números.

**Ejercicio 3008** : Leer sexo de n personas. ¿Cuantos hombres y cuantas mujeres hay en un grupo?.

**Ejercicio 3009** : Un cliente al hacer la compra, cada vez que coge un artículo anota su precio, cantidad y calcula su coste. Va acumulando lo que gasta en todos los artículos hasta que decide dejar de comprar. Obtener el total de su compra.

**Ejercicio 3010** : Calcular el mínimo común múltiplo de dos números enteros positivos.

**Ejercicio 3011** : Calcular el factorial de un número.

```python
N = int(input('N='))
fac = 1
for x in range(1,N+1):
    fac = fac * x
print(f'El factorial de {N} es {fac}')
```

```python
N = int(input('N='))
fac = 1
for x in range(1,N+1):
    fac = fac * x
print(f'El factorial de {N} es {fac}')
```

```python
N = int(input('N='))
fac = 1
for x in range(1,N+1):
    fac = fac * x
print(f'El factorial de {N} es {fac}')
```

```python
def factorial(N):
    fac = 1
    for x in range(1,N+1):
        fac = fac * x
    return fac
N = int(input('N='))
print(f'El factorial de {N} es {factorial(N)}')
```

```python
def factorial(N):
    fac = 1
    for x in range(1,N+1):
        fac = fac * x
    return fac
N = int(input('N='))
print(f'El factorial de {N} es {factorial(N)}')
```

```python
def factorial(N):
    fac = 1
    for x in range(1,N+1):
        fac = fac * x
    return fac
N = int(input('N='))
print(f'El factorial de {N} es {factorial(N)}')
```

```python
# Funcion recursiva
def factorial(N):
    if N>1:
        return N * factorial(N-1)
    else:
        return 1
Z = int(input('Numero='))
print(factorial(Z))
```

```python
# Funcion recursiva
def factorial(N):
    if N>1:
        return N * factorial(N-1)
    else:
        return 1
Z = int(input('Numero='))
print(factorial(Z))
```

```python
# Funcion recursiva
def factorial(N):
    if N>1:
        return N * factorial(N-1)
    else:
        return 1
Z = int(input('Numero='))
print(factorial(Z))
```

**Ejercicio 3012** : Calcular el factorial de N números enteros positivos leídos desde el teclado.

**Ejercicio 3013** : Un número primo es un número natural mayor que 1 que tiene únicamente dos divisores positivos distintos: él mismo y el 1. Calcular el mayor número primo entre 1 y M.

```python
def es_primo(n):
    for i in range(2,n):
        if n%i==0:
            return False
    return True
x = M
while not es_primo(x):
    x = x-1
print(f'El primo mas grade entre 1 y {M} es {x}')
```

```python
def es_primo(n):
    for i in range(2,n):
        if n%i==0:
            return False
    return True
x = M
while not es_primo(x):
    x = x-1
print(f'El primo mas grade entre 1 y {M} es {x}')
```

```python
def es_primo(n):
    for i in range(2,n):
        if n%i==0:
            return False
    return True
x = M
while not es_primo(x):
    x = x-1
print(f'El primo mas grade entre 1 y {M} es {x}')
```

**Ejercicio 3014** : Se tienen N alumnos. Calcular la nota media, la nota más alta y la nota más baja de todo el grupo.

**Ejercicio 3015** : Calcular la distancia recorrida (metros) cada segundo por un cuerpo durante los primeros 10 segundos de caída libre, sabiendo que la distancia recorrida viene dada por la expresión: S=1/2*at2 (S distancia en metros, a: aceleración debida a la gravedad 9,8m/s2, t: tiempo en segundos)

#### Cadenas¶

**Ejercicio 3101** : Indicar cuantos dígitos pares tiene un número entero positivo N.

```python
N = input('N=')
contador = 0
for digito in N :
    if digito in '02468': # int(digito)%2 == 0
        contador = contador+1
print(contador)
```

```python
N = input('N=')
contador = 0
for digito in N :
    if digito in '02468': # int(digito)%2 == 0
        contador = contador+1
print(contador)
```

```python
N = input('N=')
contador = 0
for digito in N :
    if digito in '02468': # int(digito)%2 == 0
        contador = contador+1
print(contador)
```

**Ejercicio 3102** : Indicar si el número real introducido es correcto (solo puede contener dígitos, el punto decimal y el signo)

```python
def es_real(cadena):
    for c in cadena: # ['0','1',...]
        if c not in '0123456789.-':
            return False
    if cadena.count('.')>1:
            return False
    if cadena.count('-')>1:
            return False
    if '-' in cadena and cadena.index('-')!=0:
            return False
    return True

cadena = input('Numero real=')
if es_real(cadena):
    print('Es correcto')
else:
    print('Es incorrecto')
```

```python
def es_real(cadena):
    for c in cadena: # ['0','1',...]
        if c not in '0123456789.-':
            return False
    if cadena.count('.')>1:
            return False
    if cadena.count('-')>1:
            return False
    if '-' in cadena and cadena.index('-')!=0:
            return False
    return True

cadena = input('Numero real=')
if es_real(cadena):
    print('Es correcto')
else:
    print('Es incorrecto')
```

```python
def es_real(cadena):
    for c in cadena: # ['0','1',...]
        if c not in '0123456789.-':
            return False
    if cadena.count('.')>1:
            return False
    if cadena.count('-')>1:
            return False
    if '-' in cadena and cadena.index('-')!=0:
            return False
    return True

cadena = input('Numero real=')
if es_real(cadena):
    print('Es correcto')
else:
    print('Es incorrecto')
```

**Ejercicio 3103** : Introducir un número N e identificar si es un número palíndromo. (Un número palíndromo es un número natural que se lee igual de derecha a izquierda y de izquierda a derecha. Por ejemplo 1348431).

**Ejercicio 3104** : Introducir una frase en minúsculas y contar las vocales y las consonantes.

**Ejercicio 3105** : Contar las vocales que contiene el fichero “entrada.txt”.

**Ejercicio 3106** : Introducir una cadena de caracteres con varios números separados por un espacio. Crear el fichero “salida.txt” con los números separados por comas y con una coma al final.

**Ejercicio 3107** : Pedir por teclado una cadena de caracteres (frase) y crear un fichero llamado “salida.txt” con la frase repetida N veces. Cada frase en una línea distinta.

**Ejercicio 3108** : Leer los caracteres de un fichero de texto llamado “entrada.txt”, eliminar los espacios y escribirlos en otro fichero llamado “salida.txt”. Mostrar por pantalla el número total de espacios eliminados.

**Ejercicio 3109** : Pedir por teclado un número entero N y escribir en un fichero llamado “salida.txt” un cuadrado de NxN asteriscos (N líneas con N asteriscos cada una).

**Ejercicio 3110** : Leer los caracteres de un fichero de texto llamado “entrada.txt” y escribirlos en otro fichero llamado “salida.txt”. Mostrar por pantalla el número total de caracteres leídos/escritos.

**Ejercicio 3110** : Comparar el contenido de dos ficheros de texto e indicar si son iguales.

**Ejercicio 3112** : Escribir la frase en pantalla “Desea salir? (S/N)” hasta que el usuario pulse la tecla ‘S’ o ‘s’.

**Ejercicio 3113** : Pedir por teclado un número N>0. Reiterar la petición hasta que el número sea correcto (control de entrada).

**Ejercicio 3114** : Pedir por teclado un numero entero y verificar que es correcto. Reiterar la petición hasta que el número sea correcto(control de entrada).

**Ejercicio 3115** : Pedir por teclado un numero real y verificar que es correcto. Reiterar la petición hasta que el número sea correcto (control de entrada).

**Ejercicio 3116** : Pedir por teclado un DNI y verificar que es correcto (8 dígitos + 1 letra). Reiterar la petición hasta que sea correcto (control de entrada).

**Ejercicio 3117** : Comparar el contenido de dos ficheros de texto e imprimir en pantalla los caracteres que coinciden.

#### Listas¶

**Ejercicio 3201** : El fichero “palabras.txt” contiene varias palabras separadas por un espacio. Leer el fichero y crear una lista con las palabras.

**Ejercicio 3202** : El fichero “numeros-enteros.txt” contiene varios números enteros separados por comas. Leer el fichero y crear una lista con los números en formato entero.

```python
f.close()
lista1 = cadena.split(',')
lista2 = []
for x in lista1:
    lista2.append(int(x))
```

```python
f.close()
lista1 = cadena.split(',')
lista2 = []
for x in lista1:
    lista2.append(int(x))
```

```python
f.close()
lista1 = cadena.split(',')
lista2 = []
for x in lista1:
    lista2.append(int(x))
```

**Ejercicio 3202** : El fichero “numeros-reales.txt” contiene varios números reales separados por comas. Leer el fichero y crear una lista con los números en formato real con un máximo de 2 decimales.

##### 1 Lista¶

**Ejercicio 3200** : El fichero “palabras.txt” contiene varias palabras separadas por un espacio. Leer el fichero completo y guardarlo en una cadena.

**a)** Crear una lista con las palabras.

**b)** Crear un conjunto con las palabras.

**c)** Crear una lista con los caracteres.

**d)** Crear un conjunto con los caracteres.

**e)** Crear una lista de conjuntos donde cada uno contiene los caracteres de una palabra

```python
f = open('palabras.txt','r')
cadena = f.read()
f.close()
print(cadena)
lista1 = cadena.split(' ')
print(lista1)
set1 = set(lista1)
print(set1)
lista2 = list(cadena)
print(lista2)
set2 = set(cadena)
lista3 = list()
for p in lista1:
    lista3.append(set(p))
print(lista3)
lista4 = list(map(set,lista1))
print(lista4)
```

```python
f = open('palabras.txt','r')
cadena = f.read()
f.close()
print(cadena)
lista1 = cadena.split(' ')
print(lista1)
set1 = set(lista1)
print(set1)
lista2 = list(cadena)
print(lista2)
set2 = set(cadena)
lista3 = list()
for p in lista1:
    lista3.append(set(p))
print(lista3)
lista4 = list(map(set,lista1))
print(lista4)
```

```python
f = open('palabras.txt','r')
cadena = f.read()
f.close()
print(cadena)
lista1 = cadena.split(' ')
print(lista1)
set1 = set(lista1)
print(set1)
lista2 = list(cadena)
print(lista2)
set2 = set(cadena)
lista3 = list()
for p in lista1:
    lista3.append(set(p))
print(lista3)
lista4 = list(map(set,lista1))
print(lista4)
```

**Ejercicio 3202** : El fichero “numeros-enteros.txt” contiene varios números enteros separados por comas. Leer el fichero completo y guardarlo en una cadena.

**a)** Crear una lista con los números en formato entero.

**b)** Crear un conjunto con los números enteros en formato entero.

**c)** Mostrar en pantalla la suma de todos los números.

**d)** Mostrar en pantalla los números sin repetir y ordenados de menor a mayor.

**e)** Mostrar en pantalla la cantidad de veces que se repite cada número.

**f)** Mostrar en pantalla la cantidad de veces que se repite cada dígito.

**g)** Mostrar en pantalla los números insertando entre cada pareja la media de ambos (número real con dos decimales).

```python
f = open('numeros-enteros.txt','r')
cadena = f.read()
f.close()
print('cadena',cadena)
lista1 = cadena.split(' ')
print('lista1',lista1)
lista2 = list(map(int,lista1))
print('lista2',lista2)
set1 = set(lista2)
print('set1',set1)
print('suma',sum(lista2))
lista3 = list(set1)
lista3.sort()
print(lista3)
for n in lista3:
    print(f'{n} está {lista2.count(n)} veces')
set2 = set(cadena)
print('set2',set2)
for d in set2:
    if d != ' ':
        print(f'{d} está {cadena.count(d)} veces en la cadena')
lista5 = []
for i in range(len(lista2)-1):
    lista5.append(lista2[i])
    lista5.append((lista2[i]+lista2[i+1])/2)
lista5.append(lista2[i+1])
print(lista5)
```

```python
f = open('numeros-enteros.txt','r')
cadena = f.read()
f.close()
print('cadena',cadena)
lista1 = cadena.split(' ')
print('lista1',lista1)
lista2 = list(map(int,lista1))
print('lista2',lista2)
set1 = set(lista2)
print('set1',set1)
print('suma',sum(lista2))
lista3 = list(set1)
lista3.sort()
print(lista3)
for n in lista3:
    print(f'{n} está {lista2.count(n)} veces')
set2 = set(cadena)
print('set2',set2)
for d in set2:
    if d != ' ':
        print(f'{d} está {cadena.count(d)} veces en la cadena')
lista5 = []
for i in range(len(lista2)-1):
    lista5.append(lista2[i])
    lista5.append((lista2[i]+lista2[i+1])/2)
lista5.append(lista2[i+1])
print(lista5)
```

```python
f = open('numeros-enteros.txt','r')
cadena = f.read()
f.close()
print('cadena',cadena)
lista1 = cadena.split(' ')
print('lista1',lista1)
lista2 = list(map(int,lista1))
print('lista2',lista2)
set1 = set(lista2)
print('set1',set1)
print('suma',sum(lista2))
lista3 = list(set1)
lista3.sort()
print(lista3)
for n in lista3:
    print(f'{n} está {lista2.count(n)} veces')
set2 = set(cadena)
print('set2',set2)
for d in set2:
    if d != ' ':
        print(f'{d} está {cadena.count(d)} veces en la cadena')
lista5 = []
for i in range(len(lista2)-1):
    lista5.append(lista2[i])
    lista5.append((lista2[i]+lista2[i+1])/2)
lista5.append(lista2[i+1])
print(lista5)
```

**Ejercicio 3203** : El fichero “numeros-reales.txt” contiene varios números reales separados por comas. Leer el fichero completo y guardarlo en una cadena.

**a)** Crear una lista con los números en formato real.

**b)** Crear un conjunto con los números en formato real.

**c)** Crear una lista con los números en formato real con un máximo de 2 decimales.

##### Varias listas¶

**Ejercicio 3301** : El fichero "loteria.txt" contiene los resultados de un sorteo. Cada linea contiene separados por comas, el número premiado, el premio y la ciudad donde se vendió el número. Leer el fichero completo y guardarlo en una cadena.

**a)** Crear 3 listas independientes con los números, premios y ciudades. Los 3 datos de cada linea del fichero ocuparán la misma posición en las 3 listas.

**b)** Convertir a números enteros los elementos de la lista premios.

**c)** Crear una matriz de 2 dimensiones (lista de listas) que contenga el fichero "lotería.txt" completo.

**d)** Mostrar en pantalla el total de euros repartidos en premios.

**e)** Mostrar en pantalla el número de ciudades que han recibido algún premio.

**f)** Mostrar en pantalla la ciudad con mayor número de premios.

**g)** Mostrar en pantalla la ciudad donde se vendió el premio gordo.

**h)** Mostrar en pantalla la ciudad con mayor cantidad de euros en premios.

**i)** Mostrar en pantalla cuantas la ciudad con mayor número de premios.

**j)** Mostrar en pantalla la terminación más repetida en los números premiados.

```python
f = open('loteria.txt','r')
cadena = f.read()
f.close()
print(cadena)
lista1 = cadena.split('\n')
print('lista1',lista1)
numeros = []
premios = []
ciudades = list()
for c in lista1:
    lista2 = c.split(',')
    numeros.append(lista2[0])
    premios.append(int(lista2[1]))
    ciudades.append(lista2[2])
    print(lista2,numeros,premios,ciudades,sep='\n')
```

```python
f = open('loteria.txt','r')
cadena = f.read()
f.close()
print(cadena)
lista1 = cadena.split('\n')
print('lista1',lista1)
numeros = []
premios = []
ciudades = list()
for c in lista1:
    lista2 = c.split(',')
    numeros.append(lista2[0])
    premios.append(int(lista2[1]))
    ciudades.append(lista2[2])
    print(lista2,numeros,premios,ciudades,sep='\n')
```

```python
f = open('loteria.txt','r')
cadena = f.read()
f.close()
print(cadena)
lista1 = cadena.split('\n')
print('lista1',lista1)
numeros = []
premios = []
ciudades = list()
for c in lista1:
    lista2 = c.split(',')
    numeros.append(lista2[0])
    premios.append(int(lista2[1]))
    ciudades.append(lista2[2])
    print(lista2,numeros,premios,ciudades,sep='\n')
```

**Ejercicio 3302 [Práctica 4]`** : El fichero “multas.txt” contiene las multas impuestas a conductores por exceso de velocidad.
Cada línea contiene, separados por comas: matrícula del vehículo, velocidad registrada por el radar (número real) y velocidad máxima permitida (número real).

La cantidad impuesta en la multa es de 10 euros por km/h de exceso de velocidad: multa=10*(velocidad_registrada-velocidad_permitida).

**a)** Mostrar en pantalla la cantidad de coches que han sido multados.

**b)** Mostrar en pantalla el total en euros recaudados en multas.

**c)** Mostrar en pantalla la matrícula con la mayor multa.

**d)** Mostrar en pantalla la matrícula que ha cometido más infracciones.

**e)** Mostrar en pantalla cuantas multas se han impuesto fuera de zona urbana (velocidad_permitida>50).

**f)** Mostrar en pantalla cuanto se ha recaudado en zona urbana (velocidad_permitida<=50).

**g)** Dividir la franja de velocidades en tramos de 10Km/h y mostrar en pantalla cuantas multas se han impuesto en cada tramo.

**Ejercicio 3303** : Realizar un programa en Python que registre las personas que acceden a unas instalaciones. Para cada persona introducir por teclado su DNI y la hora de entrada. Al final del día, cuando se teclee un DNI=0, el programa mostrará en pantalla el DNI de cada persona que ha entrado junto a las horas que ha accedido al edificio.

**Ejercicio 3304 [Práctica 4]`** : El fichero “entrada.txt” contiene una sopa de letras de 5 líneas y 5 caracteres en cada línea. Introducir por teclado dos números X e Y (entre 0 y 4) y mostrar en pantalla el carácter que ocupa la fila X y columna Y.

#### Diccionarios¶

**Ejercicio 3401** : El fichero "loteria.txt" contiene los resultados de un sorteo. Cada linea contiene separados por comas, el número premiado, el premio y la ciudad donde se vendió el número. Leer el fichero completo y guardarlo en una cadena.

**a)** Crear un diccionario con la información del fichero. La clave de acceso será el número premiado y dará acceso al premio y la ciudad.

**b)** Cear un diccionario con la información del fichero. La clave de acceso será la ciudad y dará acceso a una lista con los premios vendidos en esa ciudad.

**c)** Cear un diccionario con la información del fichero. La clave de acceso la terminación del número premiado (último dígito) y dará acceso a una lista con los premios asociados a cada terminación.

**d)** Mostrar en pantalla el total de euros repartidos en premios.

**e)** Mostrar en pantalla el número de ciudades que han recibido algún premio.

**f)** Mostrar en pantalla la ciudad con mayor número de premios.

**g)** Mostrar en pantalla la ciudad donde se vendió el premio gordo.

**h)** Mostrar en pantalla la ciudad con mayor cantidad de euros en premios.

**i)** Mostrar en pantalla cuantas la ciudad con mayor número de premios.

**j)** Mostrar en pantalla la terminación más repetida en los números premiados.

**Ejercicio 3402 [Práctica 4]`** : El fichero “multas.txt” contiene las multas impuestas a conductores por exceso de velocidad.
Cada línea contiene, separados por comas: matrícula del vehículo, velocidad registrada por el radar (número real) y velocidad máxima permitida (número real).

La cantidad impuesta en la multa es de 10 euros por km/h de exceso de velocidad: multa=10*(velocidad_registrada-velocidad_permitida).

**a)** Mostrar en pantalla la cantidad de coches que han sido multados.

**b)** Mostrar en pantalla el total en euros recaudados en multas.

**c)** Mostrar en pantalla la matrícula con la mayor multa.

**d)** Mostrar en pantalla la matrícula que ha cometido más infracciones.

**e)** Mostrar en pantalla cuantas multas se han impuesto fuera de zona urbana (velocidad_permitida>50).

**e)** Mostrar en pantalla cuanto se ha recaudado en zona urbana (velocidad_permitida<=50).

**f)** Dividir la franja de velocidades en tramos de 10Km/h y mostrar en pantalla cuantas multas se han impuesto en cada tramo.

**Ejercicio 3403** : Realizar un programa en Python que registre las personas que acceden a unas instalaciones. Para cada persona introducir por teclado su DNI y la hora de entrada. Al final del día, cuando se teclee un DNI=0, el programa mostrará en pantalla el DNI de cada persona que ha entrado junto a las horas que ha accedido al edificio.

**Ejercicio 3404** : Disponemos de un fichero “entrada.txt” con los datos de los alumnos. Cada línea del fichero contiene el expediente, nombre y DNI de un alumno (separados por comas). Pedir por teclado un número de expediente y escribir en pantalla su Nombre y DNI. Si el expediente no existe, escribir el mensaje “Expediente erróneo”.

**Ejercicio 3405** : Crea un diccionario con la información meteorológica contenida en el fichero 'meteo.csv' (valores separados por comas). Cada linea contiene un registro con la fecha en formato 'ddmmaaaa' (ejemplo '12032024'), temperatura media, presión atmosférica media y humedad media del día. Utilizar la fecha como clave. A continuación, pedir una fecha en el formato indicado, buscarla en el diccionario y mostrar en pantalla los 3 datos meteorológicos registrados.

**Ejercicio 3406 [Práctica 4]`** : El fichero ‘temperaturas.txt’ contiene las temperaturas registradas (números reales) en el año 2022. El fichero contiene 12 lineas con las temperaturas de los 12 meses del año (la linea 1 corresponde al mes de Enero, la linea 2 a Febrero y así sucesivamente). Cada linea contiene las temperaturas de todos los días del mes separadas por un espacio.

**a)** Mostrar en pantalla la temperatura media más alta del año y el més donde se ha registrado.

**b)** Mostrar en pantalla el mes más caluroso con la temperatura media más alta.
**c)** Mostrar en pantalla el mes y día donde la temperatura media bajó de 10 grados

# FUNCIONES¶

Una función es un bloque de código que tiene asociado un nombre, de manera que cada vez que se quiera ejecutar el bloque de código basta con invocar el nombre de la función.

Para declarar una función se utiliza la siguiente sintaxis:

```
def nombre_funcion( ):
 # bloque código
 return

```

```python
def nombre_funcion( ):
    # bloque código
    return
```

```python
def nombre_funcion( ):
    # bloque código
    return
```

Por ejemplo:

```python
def bienvenida():
    print('¡Bienvenido a Python!')
    return
print(type(bienvenida))
bienvenida()
```

```python
def bienvenida():
    print('¡Bienvenido a Python!')
    return
print(type(bienvenida))
bienvenida()
```

```python
def bienvenida():
    print('¡Bienvenido a Python!')
    return
print(type(bienvenida))
bienvenida()
```

## Parámetros de una función¶

Una función puede recibir valores cuando se invoca a través de unas variables conocidas como **parámetros** que se definen entre paréntesis en la declaración de la función.

En el cuerpo de la función se pueden usar estos parámetros como si fuesen variables.

```python
def bienvenida(nombre):
    print('¡Bienvenido a Python', nombre + '!')
    return
bienvenida('Alfredo')
```

```python
def bienvenida(nombre):
    print('¡Bienvenido a Python', nombre + '!')
    return
bienvenida('Alfredo')
```

```python
def bienvenida(nombre):
    print('¡Bienvenido a Python', nombre + '!')
    return
bienvenida('Alfredo')
```

## Argumentos de la llamada a una función¶

Los valores que se pasan a la función en una llamada o invocación concreta de ella se conocen como **argumentos** y se asocian a los **parámetros** de la declaración de la función.

Los argumentos se pueden indicar de dos formas:

- **Argumentos posicionales`** : Se asocian a los parámetros de la función en el mismo orden que aparecen en la definición de la función.
- **Argumentos por nombre`** : Se indica explícitamente el nombre del parámetro al que se asocia un argumento de la forma parametro = argumento.

```python
def bienvenida(nombre, apellido):
  print('¡Bienvenido a Python', nombre, apellido + '!')
  return
bienvenida('Alfredo', 'Sánchez')
bienvenida(apellido = 'Sánchez', nombre = 'Alfredo')
```

```python
def bienvenida(nombre, apellido):
  print('¡Bienvenido a Python', nombre, apellido + '!')
  return
bienvenida('Alfredo', 'Sánchez')
bienvenida(apellido = 'Sánchez', nombre = 'Alfredo')
```

```python
def bienvenida(nombre, apellido):
  print('¡Bienvenido a Python', nombre, apellido + '!')
  return
bienvenida('Alfredo', 'Sánchez')
bienvenida(apellido = 'Sánchez', nombre = 'Alfredo')
```

## Retorno de una función¶

Una función puede devolver un objeto de cualquier tipo tras su invocación. Para ello el objeto a devolver debe escribirse detrás de la palabra reservada **return**.

Si return no devuelve ningún objeto, la función no devolverá nada (**None**).

Si finaliza la ejecución del bloque de la función sin encontrar ningún return, la función finaliza y devuelve nada (**None**)

```python
def area_triangulo(base, altura):
  return base * altura/2
print(area_triangulo(2))
print(area_triangulo(4, 5))
```

```python
def area_triangulo(base, altura):
  return base * altura/2
print(area_triangulo(2))
print(area_triangulo(4, 5))
```

```python
def area_triangulo(base, altura):
  return base * altura/2
print(area_triangulo(2))
print(area_triangulo(4, 5))
```

## Argumentos por defecto¶

En la definición de una función se puede asignar a cada parámetro un argumento por defecto, de manera que si se invoca la función sin proporcionar ningún argumento para ese parámetro, se utiliza el argumento por defecto.

```python
def bienvenida(nombre, lenguaje = 'Python'):
  print('Bienvenido',nombre,'al lenguaje',lenguaje)
  return
x = bienvenida('Alf')
print(x)
bienvenida('Alf', 'Java')
```

```python
def bienvenida(nombre, lenguaje = 'Python'):
  print('Bienvenido',nombre,'al lenguaje',lenguaje)
  return
x = bienvenida('Alf')
print(x)
bienvenida('Alf', 'Java')
```

```python
def bienvenida(nombre, lenguaje = 'Python'):
  print('Bienvenido',nombre,'al lenguaje',lenguaje)
  return
x = bienvenida('Alf')
print(x)
bienvenida('Alf', 'Java')
```

## Pasar un número indeterminado de argumentos¶

Es posible pasar un número variable de argumentos a un parámetro. Esto se puede hacer de dos formas:

***parametro** : Se antepone un asterisco al nombre del parámetro y en la invocación de la función se pasa el número variable de argumentos separados por comas. Los argumentos se guardan en una **lista** que se asocia al parámetro.

**`**parametro`** : Se anteponen dos asteriscos al nombre del parámetro y en la invocación de la función se pasa el número variable de argumentos por pares **nombre = valor**, separados por comas. Los argumentos se guardan en un **diccionario** que se asocia al parámetro.

```python
def sumar(*numero):
    print(type(numero),numero)
    return sum(numero)

print(sumar(2,3))
print(sumar(1,5,6,7,33))
```

```python
def sumar(*numero):
    print(type(numero),numero)
    return sum(numero)

print(sumar(2,3))
print(sumar(1,5,6,7,33))
```

```python
def sumar(*numero):
    print(type(numero),numero)
    return sum(numero)

print(sumar(2,3))
print(sumar(1,5,6,7,33))
```

```python
def menu(**platos):
    print(platos)
    for nombre, descripcion in platos.items():
        print(f"{nombre}: {descripcion}")

# Ejemplo de llamada:
menu(entrante="Ensalada mixta", plato_principal="Pollo al horno", postre="Tarta de queso")
```

```python
def menu(**platos):
    print(platos)
    for nombre, descripcion in platos.items():
        print(f"{nombre}: {descripcion}")

# Ejemplo de llamada:
menu(entrante="Ensalada mixta", plato_principal="Pollo al horno", postre="Tarta de queso")
```

```python
def menu(**platos):
    print(platos)
    for nombre, descripcion in platos.items():
        print(f"{nombre}: {descripcion}")

# Ejemplo de llamada:
menu(entrante="Ensalada mixta", plato_principal="Pollo al horno", postre="Tarta de queso")
```

## Ámbito de los parámetros y variables de una función¶

Los parámetros y las variables declaradas dentro de una función son de **ámbito local**, mientras que las definidas fuera de ella son de ámbito **ámbito global**.

Tanto los parámetros como las variables del ámbito local de una función sólo están accesibles durante la ejecución de la función, es decir, cuando termina la ejecución de la función estas variables desaparecen y no son accesibles desde fuera de la función.

```python
def bienvenida(nombre):
  lenguaje = 'Python'
  print('¡Bienvenido a', lenguaje, nombre + '!')
  return
bienvenida('Alf')
print(lenguaje)
```

```python
def bienvenida(nombre):
  lenguaje = 'Python'
  print('¡Bienvenido a', lenguaje, nombre + '!')
  return
bienvenida('Alf')
print(lenguaje)
```

```python
def bienvenida(nombre):
  lenguaje = 'Python'
  print('¡Bienvenido a', lenguaje, nombre + '!')
  return
bienvenida('Alf')
print(lenguaje)
```

```python
x=[10]
def cuadrado(p):
    p.append(67)
    print(x)
    return
cuadrado(x)
print('fuera=',x)
```

```python
x=[10]
def cuadrado(p):
    p.append(67)
    print(x)
    return
cuadrado(x)
print('fuera=',x)
```

```python
x=[10]
def cuadrado(p):
    p.append(67)
    print(x)
    return
cuadrado(x)
print('fuera=',x)
```

Si en el ámbito local de una función existe una variable que también existe en el ámbito global, durante la ejecución de la función la variable global queda eclipsada por la variable local y no es accesible hasta que finaliza la ejecución de la función.

```python
lenguaje = 'Java'
def bienvenida():
  lenguaje = 'Python'
  print('¡Bienvenido a', lenguaje )
  return
bienvenida()
print(lenguaje)
```

```python
lenguaje = 'Java'
def bienvenida():
  lenguaje = 'Python'
  print('¡Bienvenido a', lenguaje )
  return
bienvenida()
print(lenguaje)
```

```python
lenguaje = 'Java'
def bienvenida():
  lenguaje = 'Python'
  print('¡Bienvenido a', lenguaje )
  return
bienvenida()
print(lenguaje)
```

## Paso de argumentos por referencia¶

En Python el paso de argumentos a una función es siempre **por referencia**, es decir, se pasa una referencia al objeto del argumento, de manera que cualquier cambio que se haga dentro de la función mediante el parámetro asociado afectará al objeto original, siempre y cuando este sea mutable.

```python
def añade_asignatura(curso, asignatura):
  curso.append(asignatura)
  return
primer_curso = ['Matemáticas', 'Física']
añade_asignatura(primer_curso, 'Química')
print(primer_curso)
```

```python
def añade_asignatura(curso, asignatura):
  curso.append(asignatura)
  return
primer_curso = ['Matemáticas', 'Física']
añade_asignatura(primer_curso, 'Química')
print(primer_curso)
```

```python
def añade_asignatura(curso, asignatura):
  curso.append(asignatura)
  return
primer_curso = ['Matemáticas', 'Física']
añade_asignatura(primer_curso, 'Química')
print(primer_curso)
```

## Funciones recursivas¶

Una función recursiva es una función que en su cuerpo contiene una llama a si misma.

Se utiliza en **problemas que pueden descomponerse en subproblemas más pequeños de la misma naturaleza**.

Para garantizar el **final** de una función recursiva, las sucesivas llamadas tienen que reducir el grado de complejidad del problema, hasta que este pueda resolverse directamente sin necesidad de volver a llamar a la función.

```python
def factorial(n):
  if n == 0:
    return 1
  else:
    return n*factorial(n-1)
factorial(5)
```

```python
def factorial(n):
  if n == 0:
    return 1
  else:
    return n*factorial(n-1)
factorial(5)
```

```python
def factorial(n):
  if n == 0:
    return 1
  else:
    return n*factorial(n-1)
factorial(5)
```

**Los riesgos de la recursión** : Aunque la recursión permite resolver las tareas recursivas de forma más natural, hay que tener cuidado con ella porque suele consumir bastante memoria, ya que cada llamada a la función crea un nuevo ámbito local con las variables y los parámetros de la función. En muchos casos es más eficiente resolver la tarea recursiva de forma iterativa usando bucles.

## Programación funcional¶

En Python las funciones son objetos de primera clase, es decir, que pueden pasarse como argumentos de una función, al igual que el resto de los tipos de datos.

```python
def aplica(funcion, argumento):
  return funcion(argumento)
def cuadrado(n):
  return n*n
def cubo(n):
  return n**3
aplica(cuadrado, 5)
aplica(cubo, 5)
```

```python
def aplica(funcion, argumento):
  return funcion(argumento)
def cuadrado(n):
  return n*n
def cubo(n):
  return n**3
aplica(cuadrado, 5)
aplica(cubo, 5)
```

```python
def aplica(funcion, argumento):
  return funcion(argumento)
def cuadrado(n):
  return n*n
def cubo(n):
  return n**3
aplica(cuadrado, 5)
aplica(cubo, 5)
```

### EJERCICIOS¶

#### Números¶

#### Cadenas¶

**Ejercicio 4101** : Crea una función recursiva que invierta una cadena.

```python
def invertir(cadena):
    if len(cadena)==1:
        return cadena
    else:
        return cadena[-1] + invertir(cadena[0:len(cadena)-1])
```

```python
def invertir(cadena):
    if len(cadena)==1:
        return cadena
    else:
        return cadena[-1] + invertir(cadena[0:len(cadena)-1])
```

```python
def invertir(cadena):
    if len(cadena)==1:
        return cadena
    else:
        return cadena[-1] + invertir(cadena[0:len(cadena)-1])
```

#### Listas¶

**Ejercicio 4201** : Crea una función recursiva que elimine los elementos repetidos de una lista sin cambiar el orden original

#### Diccionarios¶

# MODULOS¶

Cualquier fichero con código de Python reutilizable se conoce como **módulo** o **librería**.

Los módulos suelen contener **funciones reutilizables**, pero también pueden definir **variables** con datos simples o compuestos (listas, diccionarios, etc), o cualquier otro código válido en Python.

Python permite importar un módulo completo o sólo algunas partes de él. Cuando se importa un módulo completo, el intérprete de Python ejecuta todo el código que contiene el módulo, mientras que si solo se importan algunas partes del módulo, solo se ejecutarán esas partes.

## Importación completa de módulos (import)¶

**import M** : Ejecuta el código que contiene M y crea una referencia a él, de manera que pueden invocarse un objeto o función f definida en él mediante la sintaxis M.f.

**import M as N** : Ejecuta el código que contiene M y crea una referencia a él con el nombre N, de manera que pueden invocarse un objeto o función f definida en él mediante la sintaxis N.f. Esta forma es similar a la anterior, pero se suele usar cuando el nombre del módulo es muy largo para utilizar un alias más corto.

## Importación parcial de módulos (from import)¶

**from M import f, g, ...** : Ejecuta el código que contiene M y crea referencias a los objetos f, g, ..., de manera que pueden ser invocados por su nombre.

De esta manera para invocar cualquiera de estos objetos **no hace falta precederlos por el nombre del módulo**, basta con escribir su nombre.

**from M import** : Ejecuta el código que contiene M y crea referencias a todos los objetos públicos (aquellos que no empiezan por el carácter _) definidos en el módulo, de manera que pueden ser invocados por su nombre.

Cuando se importen módulos de esta manera hay que tener cuidado de que no haya coincidencias en los nombres de funciones, variables u otros objetos.

```python
import calendar
print(calendar.month(2019, 4))
from math import *
print(cos(pi))
```

```python
import calendar
print(calendar.month(2019, 4))
from math import *
print(cos(pi))
```

```python
import calendar
print(calendar.month(2019, 4))
from math import *
print(cos(pi))
```

## Módulos de la librería estándar¶

Viene con una biblioteca de módulos predefinidos que no necesitan instalarse.

Algunos de los más utilizados son:

- **sys`** : Funciones y parámetros específicos del sistema operativo.
- **os`** : Interfaz con el sistema operativo.
- **os.path`** : Funciones de acceso a las rutas del sistema.
- **io`** : Funciones para manejo de flujos de datos y ficheros.
- **string`** : Funciones con cadenas de caracteres.
- **datetime`** : Funciones para fechas y tiempos.
- **math`** : Funciones y constantes matemáticas.
- **statistics`** : Funciones estadísticas.
- **random`** : Generación de números pseudo-aleatorios.

## Otras librerías¶

Estas librerías no vienen en la distribución estándar de Python y necesitan instalarse.

También puede optarse por la distribución **Anaconda** que incorpora la mayoría de estas librerías.

- **NumPy`** : Funciones matemáticas avanzadas y arrays.
- **SciPy`** : Más funciones matemáticas para aplicaciones científicas.
- **matplotlib`** : Análisis y representación gráfica de datos.
- **Pandas`** : Funciones para el manejo y análisis de estructuras de datos.
- **Request`** : Acceso a internet por http.