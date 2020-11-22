def Método_da_Bissecção(f,a,b):
    it = 1
    m = 0
    fb = f(b)
    fa = f(a)
    fm = f(m)
    if f(a)*f(b) >= 0:
        print('Intervalo não é valido')    
        exit()
    while b - a > 10**-5:
        soma = b - a 
        print('=-' *100)
        print(it,'|',a,'|' , m,'|' ,b, '|',f(a),'|' , f(m),'|' ,f(b), '|',soma)
        print('=-' *100)
        m = (b+a)/2
        if f(a) * f(m) <= 0 :
            b = m
            fb = f(m)
        else:
            a = m
            fa = f(m)
        it += 1 
    print('O total de iterações foram',  it)
    print(f'A aproximação para raiz é {(m)}')
    print(it,'|',a,'|' , m,'|' ,b, '|',f(a),'|' , f(m),'|' ,f(b), '|',soma)
    
    import math
def sec(a):
    a = 1/math.cos*1/math.cos

def método_de_newton(f,fd, xi):
    e = 10**-5
    k = 0
    km = 10
    f0 = f(xi)
    dr = 0
    while k <= km or f0 > e and dr > e:
        k += 1
        x = xi - (f0/fd(xi))
        dr = x - xi
        if dr < 0:
            dr = -dr
        print('=-' *100)
        print(k,'|',xi ,'|',f0, '|',fd(xi),'|', x,'|', dr)
        print('=-' *100)
        xi = x
        f0 = f(xi)
    print(x)
    print(k)
