# DC-Position-Control-System
## Aim:
To control the position of motor having the following specifications using MATLAB.<br>
(J)     moment of inertia of the rotor =    0.02 kg.m^2<br>
(b)     motor viscous friction constant =    0.002 N.m.s<br>
(Ktf)    motor torque constant   =           1.5 N.m/Amp<br>
(Ra)    armature resistance  =              2 Ohm<br>
(La)     armature inductance  =              0.5 H<br>
(Kb)      back emf constant = 0.5<br>
## Apparatus Required:
Computer with MATLAB software
## Theory: 


## Procedure:
1.	Open MATLAB software
2.	Open a new script file.
3.	Type the program.
4.	Save and Execute the program.
5.	Analyse the output in open loop and closed loop.

## Program
```
ktf=0.0274
j = 3.2284e-6
b = 3.5077e-6
rf = 4
lf = 2.75e-6
s = tf('s')
ol_sys = ktf/((j*s*s+b*s)*(rf+lf*s))
subplot(2,1,1)
step(ol_sys)
title("open loop response")
cl_sys = feedback(ol_sys,1)
subplot(2,1,2)
step(cl_sys)
title ("closed loop response")
```
## Output

<img width="2109" height="874" alt="image" src="https://github.com/user-attachments/assets/84545574-ca3b-4780-b61c-d43e59431c93" />

## Result
Thus, the position of dc motor is controlled using MATLAB. 
