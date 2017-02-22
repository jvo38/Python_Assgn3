#Jimmy Vo
#Jimmyvo866@gmail.com
#CPSC 223P
#Assignment 3

import math
# Two-dimensional Cartesian coordinate

class Cartesian2D:
    def __init__(self,a,b):
        self.x = a
        self.y = b

    def __str__(self):
        return '(%f, %f)' % (self.x, self.y)
    
    def __sub__(self,other):
        return Cartesian2D(self.x - other.x, self.y - other.y) 

    def __add__(self,other):
        return Cartesian2D(self.x + other.x, self.y + other.y)

    def length(self):
        return (math.sqrt((self.x - 0)**2 + (self.y - 0)**2)) #distance formula

    def normalize(self):
        q = (math.sqrt((self.x)**2 + (self.y)**2)) #to find the unit length vector
        return (self.x/q, self.y/q)

class dot:
    def __init__(self,a,b):
        self.x = a
        self.y = b

def main( ):
    a = Cartesian2D(2.3, 3.4) #objects to Cartesian2D, coordinates
    b = Cartesian2D(4.5, 1.8)
    c = Cartesian2D(8.1, 0.3)
    print("The distance from a to b is {}".format(b.__sub__(a)))
    print("The distance from b to c is {}".format(c.__sub__(b)))

    d = a + b
    print("a + b = ({},{})".format(d.x, d.y))
    d = c - b
    print("c - b = ({}, {})".format(d.x, d.y))
    print("The length of a is {}".format(a.length())) #distance to origin
    print("The length of b is {}".format(b.length()))
    print("The length of c is {}".format(c.length()))

    # the normalize method returns a unit length vector
    unita = a.normalize()
    unitb = b.normalize()
    unitc = c.normalize()
    # unpacking tuple and changing them to objects to type Cartesian2D
    j,k = unita
    unita = Cartesian2D(j, k)
    l,m = unitb
    unitb = Cartesian2D(l,m)
    o,p = unitc
    unitc = Cartesian2D(o,p)
    print("The length of unit a is {}".format(unita.length()))
    print("The length of unit b is {}".format(unitb.length()))
    print("The length of unit c is {}".format(unitc.length()))

    if a == b:
        print('Somehow a is equal to b?')
    else:
        print('a is not equal to b')
    s = 4
    d = unita.length() * s
    print(d)
    d = Cartesian2D(d,0)
    print("The length of d is {}".format(d.length()))
    e = unitb.length() * s
    f = dot(a, b)
    g = dot(unita, unitb)
    h = dot(d, e)
    print("dot(a, b) = {}".format(f))
    print("dot(unita, unitb) = {}".format(g))
    print("dot(d, e) = {}".format(h))


if __name__ == "__main__":
    main()
