# PythonPracticas

# Cree la clase
##Cree una clase para derivación numérica de una función cualquiera. use la siguiente definicio:#3
$\frac{df(x)}{dx}= lim_{\Delta x /rightarrow 0}\frac{f(x+\Delta x) - f(x)}{\Delta x}$
Líneas de código para el proyecto de programación científica 
https://gitlab.com/sroldanvasco/intro-programacion-cientifica

Para calcular f(x) 
              f'(x)

$\frac{df(x)}{dx}= lim_{\Delta x /rightarrow 0}\frac{f(x+\Delta x) - f(x)}{\Delta x}$


f(x) = 4x{
class Derivada:
    def __init__(self, func, deltax = 1e-6):
        self.deltax = deltax
        self.f = func
    def evaldf(self, x):
        return (self.f(x+self.deltax)-self.f(x))/self.deltax

myfunc = lambda x: 4*x**2+3*x+5
dydx = Derivada (myfunc)

resultado: la derivada de 4x**2+3x+5 en x=0.5, es  7.00000400044587

para llamar a la función:


class Derivad2:
    def __init__(self, func, deltax = 1e-6):
        self.deltax = deltax
        self.f = func
    def __call__(self, x):
        return (self.f(x+self.deltax)-self.f(x))/self.deltax

myfunc = lambda x: 4*x**2+3*x+5
dydx = Derivad2 (myfunc)

print(f'la derivada de 4x**2+3x+5 en x=0.5, es  {dydx(.5)}')
resultado: la derivada de 4x**2+3x+5 en x=0.5, es  7.00000400044587
