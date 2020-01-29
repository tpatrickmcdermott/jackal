---
layout: post
title:  "Solving Simple of Equations"
date:   2019-11-16 23:10:34 -0500
categories: javascript algebra basic-math
---
The purpose of solving a system of equations is the determine the point at which line segments intersect. For an equation in the form of `ax + by = c`, where `x` and `y` are the variables we're solving for, and `a,b,c` are contants. For an equation with 2 variables, solving is a pretty simple matter of substitution.  

Solve the following system:
```
    x + 2y =  13
   3x +  y = -11

  1. Isolate x in the first equation:
    x = 13 - 2y

  2. Substitute x into the second equation, and simplify:
        3(13 - 2y) - y = -11
    -->   39 - 6y  + y = -11
    -->       -5y      = -50
    -->        -y      =  10

  3. Substitute y back into the first equation
        x + 2(10) = -11
    --> x +   20  =  13
    --> x         =  -7

  So the solution (intersection point) for [x,y] is [-7,10]
```  
