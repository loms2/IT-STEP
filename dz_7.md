import random
a=random.randint(1,100)
b=random.randint(1,100)
def warp(foo):
    def warper( a, b):
        try:
         a=float(a)
         b=float(b)
        except Exception as ex :
            print(ex)
        else:
         print("__________________________________________")
         foo( a, b)
         print("__________________________________________")
    return warper
@warp
def add(a, b):
    print(a + b)
add(36,"12")
