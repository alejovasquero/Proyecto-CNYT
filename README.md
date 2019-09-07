# **Ciencias Curso CNYT Ciencias naturales y tecnología**
> _**Proyecto #1: Calculadora de matrices complejas**_\
> _**4 de Septiembre de 2019**_\
> _**David Alejandro Vasquez Carreño**_


- Se definieron las siguientes clases con los siguientes métodos
    a) Clase Complejo: print(a) imprime el complejo con precisión de 2 decimales
    
        TOLERANCIA: Representa la distancia minima al definir igualdades entre reales
        Se presentará la operación y la manera de hacerla en la librería.
        Sea a y b números complejos representados en python, con parte real y parte imaginaria, teniendo las siguientes operaciones(a = Complejo(a,b) es igual a = a+bi):
		1)  Suma         (a+b)
		2)  Producto            (a*b)
		3)  Resta              (a-b)
		4)  División             (a/b, excepcion si b=0)
		5)  Módulo            (a.modulo())
		6)  Conjugado            (a.conjugado())
		7)  Conversión entre representaciones polar y cartesiano        (a.polares() y a.cartesianas())
		8)  Retornar la fase de un número complejo.        (a.polares() par ordenado con modulo y fase, de tipo complejo)
	
	b) Clase Matriz: (a = Matriz(filas, columnas, [[]*columnas]*filas) donde cada elemento es un tupla con dos numeros(pares ordernados) [[(2,2)],[(1,1)]] matriz 2x1)
	
		1) Suma de vectores complejos     (a+b)
		2) Inverso aditivo de vector complejo      (a.inversa())
		3) Multiplicación de escalar por vector complejo       (a*c donde c es un escalar, c*a resultará en error)
		4) Suma de matrices complejas      (a+b)
		5) Inverso aditivo de matriz compleja      (a.inversa())
		6) Multiplicación de escalar por matriz compleja     (a*d donde d es el escalar, d*a resultará en error)
		7) Transpuesta de matriz compleja     (a.transpuesta())
		8) Conjugada de matriz compleja     (a.conjugada())
		9) Adjunta (daga) de matriz compleja      (a.adjunta())
		10) Producto de matrices complejas      (a*b, tener en cuenta los tamaños, de lo contrario excepción de usuario)
		11) Acción de matriz compleja sobre vector complejo     (b.accion(a) donde b es un vector y a es una matriz compatible)
		12) Producto interno de vectores complejos     (a.productoInterno(b) donde a y b son vectores del mismo tamaño)
		13) Norma de vector complejo     (a.norma())
		14) Distancia entre dos vectores complejos       (a.distancia(b) donde a y b son vectores y del mismo tamaño)
		15) ¿Es la matriz compleja una matriz unitaria?      (a.esUnitaria() -> bool)
		16) ¿Es la matriz compleja una matriz hermitiana?      (esHermitiana() -> bool)
		17) Producto tensorial de matrices complejas       (a.productoTensor(b))
    

> # Pruebas
	a) test_deberiaSumarZero():  Verifica que la suma de complejos de (0,0)
    b) test_deberiaSumarBien():  Verifica que la suma de complejos sea correcta
    c) test_deberiaRestarZero():  Verifica que la resta de complejos de (0,0)
	d) test_deberiaRestarBien(): Verifica que la resta de complejos sea correcta
    e) test_deberiaMultiplicarBien(): Verifica que la multiplicación de complejos sea correcta
    f) test_deberiaDarexcepcionZero(): Verifica que al dividir entre 0 se genere un error
	g) test_deberiaDividirBien():  Verifica que la division de complejos sea correcta
    h) test_deberiaModulo():  Verifica ciertos vectores con sus respectivos modulos, verificando que si coincidan los resultados
    i) test_deberiaConjugado():  Verifica el conjugado de ciertos vectores especiales
    j) test_deberiaPolar():  Verifica que la forma polar de un Complejo sea correcta
    k) test_deberiaCartesiano():  Verifica que la forma cartesiana de un Complejo sea correcta
        


d) Información dirigida al usuario: Cómo usar el contenido del repositorio (librería y pruebas o
documento Jupyter Notebook).
