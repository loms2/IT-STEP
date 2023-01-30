result = []
def divider(a, b):
   if a < b:
      raise ValueError
   if b > 100:
      raise IndexError
   try:
      return a/b
   except Exception as e:
      raise e
try:
   data = {10: 2, 2: 5, "123": 4, 18: 0, 8 : 4}
except Exception:
   print("Wrong dict")
for key in data:
 try:
    res = divider(key, data[key])
    result.append(res)
 except ValueError:
    print("A is bigger that B")
 except IndexError:
  print("B is bigger than 100")
 except ZeroDivisionError:
  print("Zero division")
 except TypeError:
  print("Type error")

print(result)
