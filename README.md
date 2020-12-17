# euler-project-5

import math

dic={}
n=int(input())

for i in range(2,n):
    t=0
    for j in range(2,i):
        if i%j==0:
            t+=1
    if t==0:
        dic[i]=1

for i in dic.keys():
    for j in range(1,100):
        if pow(i,j)>n:
            dic[i]=j-1
            break
print(dic)
mul=1
for k,v in dic.items():
    mul*=pow(k,v)
print(mul)
