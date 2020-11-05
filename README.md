# Boolean Operators w/ Numpy

And
- True and True ---> True
- True and False ---> False
- False and True ---> False
- False and False ---> False

Or
- True or True ---> True
- True or False ---> True
- False or True ---> True
- False or False ---> False

Not
- not Ture ---> False
- not False ---> True

Numpy
print(bmi) ---> array([21.852, 20.975, 21.75, 24.747, 21.441])
bmi > 21 and bmi < 22 ---> Value Error

- logical_and()
- logical_or()
- logical_not()

np.logical_and(bmi>21, bmi<22) ---> array([True, False, True, False, True])
bmi[np.logical_and(bmi>21, bmi<22)] ---> array([21.852, 21.75, 21.441])
