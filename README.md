# gas-molecular

from vpython import * 
from numpy.random import * 

scene.autoscale = True 
# ball という名前の sphere をつくる 
wallR = box(pos=vector(6,0,0), size=vector(0.2,12,12), color=color.red) 
wallL = box(pos=vector(-6,0,0), size=vector(0.2,12,12), color=color.green)
wallU=box(pos=vector(0,6,0), size=vector(12,0.2,12), color=color.yellow)
wallD=box(pos=vector(0,-6,0), size=vector(12,0.2,12), color=color.blue)
wallB=box(pos=vector(0,0,-6), size=vector(12,12,0.2), color=color.orange)
a=[]


for j in range(100000):
    for i in range (10):
        a.append(sphere(pos=vector(i*0.5,0,0), radius=0.3, color=color.cyan)
        a[i].velocity = vector(10*randn(),10*randn(),10*randn())
        deltat = 0.005 #時間の刻み 
        t = 0 

        
        a[i].pos = a[i].pos + a[i].velocity*deltat 
        rate(2000) 
        
        if a[i].pos.x >= 6 :
            a[i].velocity.x = a[i].velocity.x * (-1)
        if a[i].pos.x <= -6 :
             a[i].velocity.x = a[i].velocity.x * (-1)
    
        if a[i].pos.y >= 6 :
            a[i].velocity.y = a[i].velocity.y * (-1)
        
        if a[i].pos.y <= -6 :
            a[i].velocity.y= a[i].velocity.y * (-1)    
        
        if a[i].pos.z>= 6 :
            a[i].velocity.z =a[i].velocity.z * (-1)
        
        if a[i].pos.z <= -6 :
            a[i].velocity.z= a[i].velocity.z * (-1)
        
        
        
        

