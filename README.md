Name. Ranpise Anmol 
Roll No. SEL66
Date. 03/03/2025

Input

# -*- coding: utf-8 -*-
"""
Created on Thu Apr  3 15:06:59 2025

@author: EL-COMP LAB-2
"""

"Program for 4th order RK method"


def f(t,i):
    return(20-5*i)

t0=float(input("Enter the initial value of time t\t"))
i0=float(input("Enter the initial value of time i\t"))
t=float(input("Enter the final value of time t\t"))

h=float(input("Enter the step size h \t"))

n=(t-t0)/h

i=0
while(i<n):
    print("Applying %d iteration"%(i+1))
    k1=h*f(t0,i0)
    k2=h*f(t0+h/2,i0+k1/2)
    k3=h*f(t0+h/2,i0+k2/2)
    k4=h*f(t0+h,i0+k3)
    k=1/6*(k1+2*k2+2*k3+k4)
    i1=i0+k
    t1=t0+h
    i=i+1
    print("the value of current i at t=%f is %f"%(t1,i1))



Output

Enter the initial value of time t	0
Enter the initial value of time i	0
Enter the final value of time t	0.1
Enter the step size h 	0.1
Applying 1 iteration
the value of current i at t=0.100000 is 1.572917





