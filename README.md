# Programming-DSA-using-Python-Week-3-Programming-Assignment

Write a function contracting(l) that takes as input a list of integer l and returns True if the absolute difference between each adjacent pair of elements strictly decreases.

def contracting(l):

  for z in range(0,len(l)-3):

A=abs(l[z+2]-l[z+1])

B=abs(l[z+1]-l[z])

if A<B:continue
   
   else:
   
   return (False) 
  
  return (True)
  
  print(contracting([9,2,7,3,1]))
  
print(contracting([-2,3,7,2,-1]))

print(contracting([10,7,4,1]))

In a list of integers l, the neighbours of l[i] are l[i-1] and l[i+1]. l[i] is a hill if it is strictly greater than its neighbours and a valley if it is strictly less than its neighbours.
Write a function counthv(l) that takes as input a list of integers l and returns a list [hc,vc] where hc is the number of hills in l and vc is the number of valleys in 





