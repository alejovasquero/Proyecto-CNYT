# **Ciencias Curso CNYT Ciencias naturales y tecnología
> _**Proyecto #1: Calculadora de matrices complejas**_\
> _**4 de Septiembre de 2019**_\
> _**David Alejandro Vasquez Carreño**_


- Se definieron las siguientes clases con los siguientes métodos
    1) Complejo
        TOLERANCIA: Representa la distancia minima al definir igualdades entre reales
        
        **__init__(self, parteReal: float, parteImaginaria: float, cartesiana=True)**\
            Constructor: Recibe 3 parametros, minimo 2. El primero es la parte real del complejo, el segundo es la parte Compleja
            y el 3 es opcional, indica si está dado en coordenadas cartesianas. True si está en cartesianas, False de lo contrario.
            Por defecto es cartesianas.
        

    
    
    @staticmethod
    def multiplicacion(a, b):
        a1 , b1 = a.parteReal, a.parteImaginaria
        a2, b2 = b. parteReal, b.parteImaginaria
        return Complejo(a1*a2 - b1*b2, a1*b2 + b1*a2)
    
    @staticmethod
    def resta(a, b):
        return Complejo(a.parteReal - b.parteReal, a.parteImaginaria - b.parteImaginaria)
    
    
    def modulo(self):
        if(self.cartesiana == True):
            a = self
        else : 
            a = self.cartesianas()
        return math.sqrt((a.parteReal)**2 + (a.parteImaginaria)**2)
    
    #divide el complejo por un real
    def divisionEscalar(self, divisor):
        return Complejo(self.parteReal/divisor, self.parteImaginaria/ divisor)
    
    def multiplicacionEscalar(self, multiplo):
        return Complejo(self.parteReal*multiplo, self.parteImaginaria*multiplo)
    
    def conjugado(self):
        return Complejo(self.parteReal, -self.parteImaginaria)
    
    @staticmethod
    def division(a,b):
        #Al dividir a/b nos vamos a basar en la multiplicacion por el conjugado con divisor igual el cuadrado del modulo de b
        divisor = b.modulo()**2
        respuesta =  Complejo.multiplicacion(a, b.conjugado())
        respuesta = respuesta.divisionEscalar(divisor)
        return respuesta
    
    @staticmethod
    def gradosARadianes(grado):
        return grado*math.pi/180
    
    @staticmethod
    def radianesAGrados(radian):
        return radian*180/math.pi
    
    @staticmethod
    def obtenerAngulo(x,y):
        ans = math.atan2(y,x)
        #Retorna en angulo de radianes positivo entre 0 y 2*pi
        if(ans<0):
            ans+=2*math.pi
        return ans%(2*math.pi)
    
    
    def polares(self):
        if(self.cartesianas == False):
            ans = Complejo(self.parteReal, self.parteImaginaria)
        else:
            angulo = Complejo.obtenerAngulo(self.parteReal,self.parteImaginaria)
            ans = Complejo(self.modulo(), Complejo.radianesAGrados(angulo), False)
        return ans
        
        
    #Vamos a suponer que el complejo ya está en polares    
    def cartesianas(self):
        if(self.cartesiana == True):
            ans = Complejo(self.parteReal, self.parteImaginaria)
        else:
            fase = Complejo.gradosARadianes(self.parteImaginaria)
            ans = Complejo(self.parteReal*math.cos(fase), self.parteReal*math.sin(fase))
            
        return ans
    def __mul__(self,b):
        if(type(b) is float or type(b) is int):
            return self.multiplicacionEscalar(b)
        else:
            return self.multiplicacion(self,b)
    def __rmul__(self,b):
        return self.__mul__(b)
    def __sub__(self,b):
        return self.resta(self,b)
            
    def __div__(self,b):
        return self.division(self,b)
    def __truediv__(self,b):
        return self.division(self,b)
    @staticmethod
    def complejoDe(tupla):
        
        return Complejo(float(tupla[0]), float(tupla[1]))
    
    def __eq__(self, other):
        a = self.cartesianas()
        b = other.cartesianas()
        return abs(a.parteReal-b.parteReal)<Complejo.TOLERANCIA and abs(a.parteImaginaria-b.parteImaginaria)<Complejo.TOLERANCIA
    
    def __ne__(self,other):
        return not self.__eq__(other)
    
        



c) Breve descripción de las pruebas realizadas. Tener en cuenta realizar las pruebas contenidas
en este documento y pruebas adicionales siguiendo su criterio.
d) Información dirigida al usuario: Cómo usar el contenido del repositorio (librería y pruebas o
documento Jupyter Notebook).
