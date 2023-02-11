import time
def Rapid_exponentiation(a,n):
    c = 1
    for i in range(len(bin(n))-2):
        n -= 2**i#В мене не вийшло зробити швидше через це піднесення. Я попробував максимально то скоротити бо з попередніми варіантами були проблеми цей самий вдалий
        c *= a**(2**i)
def Exponentiation(a,n):
    a ** n
a = int(input(">>> "))
n = int(input(">>> "))
t = time.time()
Rapid_exponentiation(a,n)
print(time.time()-t)
t = time.time()
Exponentiation(a,n)
print(time.time()-t)
