# to-check-prime-or-not
import math
def isprime(inputnum):
    if(inputnum<=1):
        return False
    for i in range(2,inputnum):
        if(inputnum%i==0):
            return False
    return True    
def isprime2(inputnum):
    if(inputnum<=1):
        return False
    for i in range(2,inputnum//2+1):
        if(inputnum%i==0):
            return False
    return  True  
def isprime3(inputnum):
    if(inputnum<=1):
        return False
    for i in range(2,math.ceil(math.sqrt(inputnum))+1): #ceil(2.1)=3 floor(2.8)=2
        if(inputnum%i==0):
            return False
    return  True  
def isprime4(inputnum):
    if(inputnum<=1 or (inputnum>=4 and (inputnum%2==0 or inputnum%3==0))):
        return False
    k=1
    a,b=6*k-1,6*k+1 #this will give all prime no's
    while(a<=math.ceil(math.sqrt(inputnum)) or b<=math.ceil(math.sqrt(inputnum))):#we have to check upto sqrt(n)

                       
        if(inputnum%a==0 or inputnum%b==0):
                return False
        k+=1
        a,b=6*k-1,6*k+1
    return True
    
inputnum=int(input())

print(isprime4(inputnum))    

#if we use math.floor it will be giving wrong output for numbers 2 and 3

