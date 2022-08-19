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

def counthv(l):
  
  hill_count,valley_count=0,0
  
  if len(l)>2:
  
  for i in range(1,len(l)-1):
  
  if l[i]>l[i-1] and l[i]>l[i+1]:
  
  hill_count+=1
  
  elif l[i]<l[i-1] and l[i]<l[i+1]:
  
  valley_count+=1
  
  return ([hill_count,valley_count])

print(counthv([1,2,1,2,3,2,1]))

print(counthv([1,2,3,1]))

print(counthv([3,1,2,3]))

A square n×n matrix of integers can be written in Python as a list with n elements, where each element is in turn a list of n integers, representing a row of the matrix. For instance, the matrix

  1  2  3
  4  5  6
  7  8  9
would be represented as [[1,2,3], [4,5,6], [7,8,9]].

Write a function leftrotate(m) that takes a list representation m of a square matrix as input, and returns the matrix obtained by rotating the original matrix counterclockwize by 90 degrees. For instance, if we rotate the matrix above, we get

  3  6  9
  2  5  8    
  1  4  7

Your function should not modify the argument m provided to the function rotate().

def leftrotate(m):
    ans=list()
    for a in range(len(m)):
        ans.append([])
        for b in range(len(m)):
            ans[a].append(m[b][len(m)-a-1])
    return(ans)  

import ast

def parse(inp):
  inp = ast.literal_eval(inp)
  return (inp)

fncall = input()
lparen = fncall.find("(")
rparen = fncall.rfind(")")
fname = fncall[:lparen]
farg = fncall[lparen+1:rparen]

if fname == "contracting":
  arg = parse(farg)
  print(contracting(arg))

if fname == "counthv":
  arg = parse(farg)
  print(counthv(arg))

if fname == "leftrotate":
  arg = parse(farg)
  savearg = arg
  ans = leftrotate(arg)
  if savearg == arg:
    print(ans)
  else:
    print("Side effect")





