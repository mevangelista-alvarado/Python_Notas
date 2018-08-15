# Introducción a Sympy 

**[SymPy](https://www.sympy.org/es/)** es una biblioteca escrita en Python, cuyo objetivo es reunir todas las características de un [sistema de álgebra computacional ](https://es.wikipedia.org/wiki/Sistema_de_%C3%A1lgebra_computacional "Sistema de álgebra computacional") (CAS por sus siglas en inglés),  
 * Ser fácilmente extensible;
 *  Mantener el código todo lo simple que sea posible. 

SymPy no requiere ninguna biblioteca externa, salvo para soporte gráfico.

## Proyectos que utilizan Sympy

-   **[galgebra](https://github.com/brombo/galgebra)** : Álgebra Geométrica 
-   **[Modelado estadístico simbólico](https://www.researchgate.net/publication/260585491_Symbolic_Statistics_with_SymPy/)** : adición de operaciones estadísticas a modelos físicos complejos.
-   **[pyneqsys](https://github.com/bjodah/pyneqsys)** : Resuelve numéricamente sistemas definidos simbólicamente de ecuaciones no lineales.
-   **[ChemPy](https://github.com/bjodah/chempy)** : un paquete útil para la química escrita en Python.
-   **[Spyder](https://www.spyder-ide.org/)** : El entorno de desarrollo científico de Python, un Python equivalente a Rstudio o MATLAB; la compatibilidad completa con SymPy se puede habilitar en las [Consolas IPython](https://docs.spyder-ide.org/ipythonconsole.html) de Spyder.

# ¿Qué es la Computación Simbólica?

La computación simbólica trata simbólicamente el cálculo de objetos matemáticos, es decir, que los objetos matemáticos se representan exactamente y no aproximadamente, además las expresiones matemáticas con variables no evaluadas se dejan en forma simbólica.

## Aprendamos con el siguiente ejemplo

Queremos calcular la raíz cuadrada de 4, para esto utilizamos python con la función incorporada ```sqrt()``` de la siguiente manera:
    ```>>>import math ```
    ```>>>math.srqt(4) ```
    ```2.0 ```
Ahora queremos calcular la raíz cuadrada de 8, entonces:
    ```>>>math.srqt(8) ```
    ```2.82842712475 ```
 
Se tiene que ```2.82842712475``` es un resultado aproximado, pero  no es la raíz cuadrada exacta de 8, es más la raíz cuadrada real de 8 no puede representarse con un decimal finito, ya que es un número irracional.  

Si todo lo que nos importaba era la forma decimal de la raíz cuadrada de 8, estaríamos listos.

Pero supongamos que queremos ir más allá, para esto recordemos que 

$$\sqrt(8) =  \sqrt(4\cdot 2) =2\sqrt(2).$$

Nos sería difícil deducir esto del resultado anterior.

 Aquí es donde entra la computación simbólica. Con un sistema de computación simbólico como SymPy, las raíces cuadradas de los números que no son cuadrados perfectos quedan sin evaluar por defecto, veamos.
 
 ```>>>import sympy ```
  ```>>>sympy.sqrt(8) ```
  ```2*sqrt(2) ```


## ¿Cómo defino símbolos?

El ejemplo nos muestra cómo podemos manipular números irracionales usando exactamente SymPy,  pero es mucho más poderoso que eso. 

Los sistemas de computación simbólica como SymPy, son capaces de calcular expresiones simbólicas con variables.

Así en SymPy, las variables se definen utilizando `symbols`. A diferencia de muchos sistemas de manipulación simbólica, las variables en SymPy deben definirse antes de ser utilizadas.

Empecemos definiendo una expresión simbólica, por ejemplo,  la expresión matemática x+2yx+2y.

`>>> import sympy`
`>>> x = sympy.symbols('x') `
`>>> y = sympy.symbols('y') `
`>>> expresion = x + 2*y `
`>>> expresion`
`x + 2*y `

**Observación**
Después de definir a `x` y `y` como  variables simbólicas, las escribimos de igual manera como si fueran variables ordinarias de python.

**¿Qué ocurre al hacer lo siguiente? **
`>>> x*expresion`

$x(x+2y)$ ó $x^{2} +2xy$

El resultado es `x*(x+2y)`, esto nos dice que la mayoría de las simplificaciones no se realizan automáticamente en Sympy.

Esto se debe a que podríamos preferir la forma factorizada $x(x+2y)$ o podríamos preferir la forma expandida $x^2+2xy$. Ambas formas son útiles en diferentes circunstancias y tenemos funciones para ir de una forma a la otra

`>>> import sympy`
`>>> expresion_expandida = sympy.expand(x*expresion)`
`>>> expresion_expanida`
`x**2 + 2*x*y`
`>>> expresion_factores=sympy.factor(expresion_expandidad)`
`>>> x*(x+2*y)`
 
## Descubriendo el poder
El poder real de SymPy es la capacidad de hacer todo tipo de cálculos simbólicamente. 

SymPy puede simplificar expresiones, calcular derivados, integrales y límites, resolver ecuaciones, trabajar con matrices y etc y además de  hacerlo de forma simbólica. 

Aquí hay una pequeña muestra del  poder simbólico que SymPy es capaz de hacer, esperando despertar tu apetito.

* Preparamos el entorno de trabajo
	 * Definimos las variables simbólicas 
	 `>>> from sympy import *`
	 * Definimos una salida bonita utilizando caracteres unidecode.
	 `>>> init_printing(use_unicode=True)`
* Derivadas,
	*  $\frac{d(sin(x)e^x)}{dx}$
	 `>>> diff(sin(x)*exp(x), x)`

* Integrales
	* $\int_{\infty}^{-\infty}\sin(x^2) dx$
		`>>> integrate(sin(x**2),  (x,  -oo,  oo))`
	*  $\int e^x\sin(x) + e^x\cos(x)dx$
		`>>> integrate(exp(x)*sin(x) + exp(x)*cos(x), x)`

 * Limites
	 * $\lim_{x\to 0}\frac{\sin(x)}{x}$
	 `>>> solve(x**2 - 2, x)`

 * Soluciones
	 * Polinomios ($x^2-2=0$) 
	 `>>> solve(x**2 - 2, x)`
	 * EDOs ($y''-y=e^t$)
	  `>>> y = Function('y')`
	`>>> dsolve(Eq(y(t).diff(t, t) - y(t), exp(t)), y(t))`
	* Eigenvalores $\begin{array}{cc}
1 &2 \\ 
2 & 2
\end{array}$ 
	 `>>> Matrix([[1,  2],  [2,  2]]).eigenvals()`
 
## ¿Por qué Sympy?

Hay muchos sistemas de álgebra computacional por ahí.[Este](http://en.wikipedia.org/wiki/List_of_computer_algebra_systems) artículo de Wikipedia enumera muchos de ellos. ¿Qué hace que SymPy sea una mejor opción que las alternativas?

En primer lugar, SymPy es completamente gratuito. Es de código abierto y está licenciado bajo la licencia liberal BSD, por lo que puede modificar el código fuente e incluso venderlo si lo desea. Esto contrasta con los sistemas comerciales populares como Maple o Mathematica que cuestan cientos de dólares en licencias.

En segundo lugar, SymPy usa Python. La mayoría de los sistemas de álgebra informática inventan su propio idioma.

Una última característica importante de SymPy es que puede usarse como un módulo. 

