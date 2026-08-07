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
Kt = 0.0274;<br>
Rf = 4;<br>
Lf = 2.75e-6;<br>
J = 3.2284e-6;<br>
B = 3.5077e-6;<br>
S = tf('s');<br>
ol_Sys = Kt/((Rf+Lf*S)*(J*S*S+B*S));<br>
subplot(2,1,1)<br>
step(ol_Sys)<br>
title('open loop response')<br>
cl_Sys = feedback(ol_Sys,1);<br>
subplot(2,1,2)<br>
step(cl_Sys)<br>
title('closed loop response')<br>

## Output
![WhatsApp Image 2025-10-08 at 08 54 22_75b0a7b4](https://github.com/user-attachments/assets/a5da5e3e-eb73-413a-8576-98d47821d59e)
![WhatsApp Image 2025-10-08 at 08 53 46_6efd49f0](https://github.com/user-attachments/assets/a5123dde-3918-49ca-887e-f06eaed9e149)





## Result
Thus, the position of dc motor is controlled using MATLAB. 
