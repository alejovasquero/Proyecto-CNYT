
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
    

> # Pruebas Complejo
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
    
   ![Resultados](CTEST.PNG)








> # Pruebas Matriz
    a) test_deberiaSumarVectores():  Verifica que la suma de vectores sea correcta
    b) test_deberiaInversoVector(): Verifica que el inverso aditivo de vectores sea correcto
    c) test_deberiaMultiplicarEscalarVector():   Verifica que la multiplicación por un escalat sea correcta
    d) test_deberiaSumarMatrices(): Verifica que la suma de matrices sea correcta
    e) test_deberiaInversoMatriz():  Verifica que el inverso aditivo de una matriz sea correcto
    f) test_deberiaMultiplicarEscalarMatriz():  Verifica que la multiplicación de una matriz por un escalar sea correcta
    g) test_deberiaTransponerMatriz():  Verifica que la transpuesta de una matriz sea correcta
    h) test_deberiaConjugar():   Verifica que la matriz conjugada de una matriz sea correcta
    i) test_deberiaAdjuntaMatriz():  Verifica que la adjunta de una matriz sea correcta
    j) test_deberiaProductoMatriz(): Verifica que la multiplicación entre matrices sea correcta
    k) test_deberiaAccion():  Verifica que la acción de una matriz sobre un vector sea correcta
    l) test_deberiaProductoInterno():  Verifica que el producto interno entre 2 vectores sea correcto
    m) test_deberiaNormaVector():  Verifica que la norma de un vector sea correcta
    n) test_deberiaDistancia(): Verifica que la distancia entre 2 vectores sea correcta
    ñ) test_deberiaSerUnitaria():  Verifica que verifique correctamente matrices unitarias
    o) test_deberiaSerHermitiana():  Verifica que verifique correctamente matrices hermitianas 
    p) test_deberiaProductoTensor():  Verifica que el producto tensor entre 2 matrices funciones correctamente
 ![Resultados](MTEST.PNG)
       

> # Información dirigida al usuario
> Para utilizar las clases o pruebas tenga en cuenta la siguientes pasos:
>>  1)  Correr las otras librerías que sean requeridas, como complejo o matriz
>>  ![IMPORTAR1](CORRER.PNG)
>>  2) Importar las librerías de python, como math, numpy, etc.
>>  ![IMPORTAR2](LIBRERIAS.PNG)
>>  3) Ejecutar la clase que desee utilizar. En el caso de pruebas ejecuta el bloque y obtiene el resultado
>>  ![correr](CLASE.PNG)
>>  ![PRUEBA](PRUEBA.PNG) 
>>  4) Listo para usar(instanciación y ejecución de servicios de las clases)




c) Clase Systems(SISTEMAS_CLA_PROB_CUAN.ipynb)
Representa un sistema de dinámica con propiedades probabilisticas, clásicas o cuánticas

class Systems:
    Atributos: Repsesentan los posibles estados que pueden tomar los sistemas dinámicos
    	- CLASSIC: Dinámica clásica
    	- PROBABILISTIC: Dinámica probabilistica
    	- QUANTUM: Dinámica cuántica
    	- SLIT_QU: Dinámica de rendija cuántica
    	- SLIT_PROB: Dinámica de rendija probabilistica
    Métodos:
    INVALID_SYSTEM = "The system is not valid"
    INCORRECT_FORMAT = "The matriz doesn't match de system format"
    INVALID_VECTOR = "The vector is not valid"
    @staticmethod
    def verifySystem(matrix, systemType):
        ans = False
        if(systemType==Systems.CLASSIC):
            ans = Systems.verifyClassic(matrix)
        elif(systemType==Systems.PROBABILISTIC):
            ans = Systems.verifyProbabilistic(matrix)
        elif(systemType==Systems.QUANTUM):
            ans = Systems.verifyQuantum(matrix)
        else: 
            raise Exception(Systems.INVALID_SYSTEM)
        return ans
    
    @staticmethod
    def verifyClassic(matrix):
        isValid = True
        one = Complejo(1,0)
        zero = Complejo(0,0)
        columnSum = Complejo(0,0)
        j = 0
        while(j<matrix.columnas and isValid):
            i=0
            columnSum=Complejo(0,0)
            while(i<matrix.filas and isValid):
                isValid = isValid and (matrix[i,j]==one or matrix[i,j]==zero)
                columnSum+=matrix[i,j]
                i+=1
            isValid= isValid and columnSum==one
            j+=1
        return isValid
            
    @staticmethod
    def verificarColumnasEstocasticas(matrix):
        isValid = True
        one = Complejo(1,0)
        zero = Complejo(0,0)
        columnSum = Complejo(0,0)
        j = 0
        while(j<matrix.columnas and isValid):
            i=0
            while(i<matrix.filas and isValid):
                s = matrix[i,j].parteReal
                isValid = isValid and matrix[i,j].parteImaginaria==0 and s>=0 and s<=1
                columnSum+=matrix[i,j]
                i+=1
            isValid= isValid and columnSum==one
            columnSum=Complejo(0,0)
            j+=1
        
        return isValid
    
    @staticmethod
    def verificarFilasEstocasticas(matrix):
        isValid = True
        one = Complejo(1,0)
        zero = Complejo(0,0)
        columnSum = Complejo(0,0)
        i = 0
        while(i<matrix.filas and isValid):
            j=0
            while(j<matrix.columnas and isValid):
                s = matrix[i,j].parteReal
                isValid = isValid and matrix[i,j].parteImaginaria==0 and s>=0 and s<=1
                columnSum+=matrix[i,j]
                j+=1
            isValid= isValid and columnSum==one
            columnSum=Complejo(0,0)
            i+=1
        return isValid
    
    
    @staticmethod
    def verifyProbabilistic(matrix):
        return Systems.verificarFilasEstocasticas(matrix) and Systems.verificarColumnasEstocasticas(matrix)
    
    @staticmethod
    def verifyQuantum(matrix):
        return matrix.esUnitaria()
    
    
    @staticmethod
    def verifyVector(state0, systemType):
        ans= state0.columnas==1
        if(systemType==Systems.CLASSIC):
            ans = ans and Systems.verifyClassic(state0)
        elif(systemType==Systems.PROBABILISTIC):
            ans = ans and Systems.verificarColumnasEstocasticas(state0)
        elif(systemType==Systems.QUANTUM):
            prueba=Matriz(state0.filas,1)
            for i in range(state0.filas):
                prueba[i,0]=state0[i,0]*(state0[i,0].conjugado())
                
            
            ans = ans and Systems.verificarColumnasEstocasticas(prueba)
        else: 
            raise Exception(Systems.INVALID_VECTOR)
        return ans
    
    def __init__(self, systemType, matrix: Matriz, state0, clicks, statesA=None, statesB=None, assembled=False):
        self.state = [True, None, None]
        self.statesA=statesA
        self.statesB=statesB
        self.assembled=assembled
        self.type=None
        #[0]=isValid system, [1]=matriz^clicks, [2]=state0->final[t]
        if(systemType!=Systems.SLIT_QU and systemType!=Systems.SLIT_PROB and (not Systems.verifySystem(matrix, systemType) or matrix.filas==0 or matrix.filas!=matrix.columnas 
           or matrix.filas!=state0.filas)):
            self.state[0]=False
        else:
            
            self.state[1]=matrix**clicks
            self.state[2]=self.state[1]*state0
            self.type=systemType
   
    def success(self):
        return self.state[0]==True and self.state[1]!=None and self.state[2]!=None
    
    
    @staticmethod
    def obtainType(matrix):
        ans = -1
        if(Systems.verifyClassic(matrix)):
            ans = Systems.CLASSIC
        elif(Systems.verifyProbabilistic(matrix)):
            ans = Systems.PROBABILISTIC
        elif(Systems.verifyQuantum(matrix)):
            ans = Systems.QUANTUM
        return ans
    
    
    @staticmethod
    def assembleSystems(systemA, viA, systemB, viB, t):
        assembled = systemA.productoTensor(systemB)
        statei = viA.productoTensor(viB)
        return Systems(Systems.obtainType(systemA), assembled, statei, t, viA.filas, viB.filas, True)
    
    @staticmethod
    def fullSlits(matrix, slits, typeS):
        t=1/slits
        if(typeS==Systems.SLIT_QU):
            t=t**0.5
        for i in range(1, slits+1):
            matrix[i,0]=Complejo(t,0)
    
    @staticmethod
    def fullTargets(matrix, slits,targets, vector):
        begin=slits+1
        final=begin+2*targets+1
        
        for j in range(1, slits+1):
            for i in range(begin, final):
                
                matrix[i,j]=vector[i%begin,0]
            begin+=targets+1
            final=begin+2*targets+1
            
    @staticmethod
    def fullReturn(matrix, slits,targets):
        begin=slits+1
        for i in range(begin, matrix.filas):
            matrix[i,i]=Complejo(1,0)
    
    @staticmethod
    def doubleSlit(slits, targets, vector):
        prob=Systems.verifyVector(vector, Systems.PROBABILISTIC)
        quan=Systems.verifyVector(vector, Systems.QUANTUM)
        
        if(vector.filas!=2*targets+1 or vector.columnas!=1 or not (prob or quan)):
            raise Exception("Vector invalid")
        n=1+slits+(slits+targets*(slits+1))
        typeS=-1
        if(prob):
            typeS=Systems.SLIT_PROB
        else:
            typeS=Systems.SLIT_QU
        matrix=Matriz(n,n)
        Systems.fullSlits(matrix, slits, typeS)
        Systems.fullTargets(matrix, slits,targets, vector)
        Systems.fullReturn(matrix, slits, targets)
        state0=Matriz(n,1)
        state0[0,0]=Complejo(1,0)
        
        return Systems(typeS, matrix, state0, 2)
        
    def obtenerDatos(self):
        ans=[]
        if(self.type==Systems.QUANTUM or self.type==Systems.SLIT_QU):
            for i in range(self.state[2].filas):
                ans.append(self.state[2][i,0].modulo()**2)
        else:
            for i in range(self.state[2].filas):
                ans.append(self.state[2][i,0].parteReal)
        
        return ans
    def showGraphic(self):
        fig = plt.figure()
        
        ax=fig.add_subplot(111)
        datos=self.obtenerDatos()
        xx=range(len(datos))
        letter=[str(i) for i in range(len(datos))]
        ax.bar(xx, datos , color=(0,1,0), align="center")
        ax.set_xticks(xx)
        ax.set_xticklabels(letter)
        plt.show()
    

