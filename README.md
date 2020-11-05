# If & elif & else

Conditional Statement
if, elif, else

- Only if
if condition :
  expression

z = 4
if z % 2 == 0 :
  print("z is even")
---> z is even


z = 4
if z % 2 == 0 :
  print("checking "+str(z))
  print("z is even")
---> checking 4
---> z is even

z = 5
if z % 2 == 0 :
  print("checking "+str(z))
  print("z is even")
---> since the condition is false, so there is no comeout

- If with else
if condition :
  expression
else :
  expression

z = 5
if z % 2 == 0 :
  print("z is even")
else :
  print("z is odd")

---> z is odd

- If with elif, and else

if condition :
  expression
elif condition:
  expression
else :
  expression

z = 3

if z % 2 == 0 :
  print("z is divisible by 2")
elif z % 3 == 0:
  print("z is divisible by 3")
else:
  print("z is neither divisible by 2 nor by 3")

---> z is divisible by 3


