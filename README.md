### Ex. No. : 2 
### Date: 31.3.23 
# Implementation of Combinational logic circuit using Verilog HDL
## Aim:
To implement the following Boolean functions using Verilog HDL and to verify the truth table.
1. F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
2. F2=xy’z+x’y’z+w’xy+wx’y+wxy

## Components Required:
1.	Laptop with Quartus software and modelsim software.

## Theory:
Combinational Logic Circuits are memoryless digital logic circuits whose output at any instant in time depends only on the combination of its inputs.
The outputs of Combinational Logic Circuits are only determined by the logical function of their current input state, logic “0” or logic “1”, at any given instant in time.

![image](https://github.com/rvinifa/ex.2/assets/133735746/949815d3-0912-49c7-81c0-eea1c148d48e)

The result is that combinational logic circuits have no feedback, and any changes to the signals being applied to their inputs will immediately have an effect at the output. In other words, in a Combinational Logic Circuit, the output is dependant at all times on the combination of its inputs. Thus, a combinational circuit is memoryless.

## Procedure:
1.	Type the program in Quartus software.
2.	Compile and run the program.
3.	Generate the RTL schematic and save the logic diagram.
4.	Create nodes for inputs and outputs to generate the timing diagram.
5.	For different input combinations, generate the timing diagram.

## Simplification:
![f1 ex2](https://github.com/BALA291/ex.2/assets/120717501/d0adf6a0-b171-42fa-9b94-8a8541fbb3b1)

![f2 ex2](https://github.com/BALA291/ex.2/assets/120717501/c0f55a97-727f-4e40-a63e-1af94d91a01c)

## Truth Table:
![f1 ex2 t](https://github.com/BALA291/ex.2/assets/120717501/38570151-47b6-4fb6-96f9-3090480b4915)


## Program:
```
module ex2(a,b,c,d,F1,F2);
input a,b,c,d;
output F1,F2;
wire p,q,r,s,t,u,v,x,y,w;
not(p,c);
not(t,b);
not(u,d);
not(y,a);
and(q,p,d);
and(r,a,c);
and(s,b,c); 
or(F2,q,r,s);
and(v,t,u);
and(w,a,b,p);
and(x,y,b,d);
or(F1,v,w,x);
endmodule
```

## RTL Schematic:

![logic ex2](https://github.com/BALA291/ex.2/assets/120717501/87f8eacc-7fb1-47b7-9ef8-6f526d8b4457)


## Timing Diagram:

![waveform ex2](https://github.com/BALA291/ex.2/assets/120717501/011baaa8-e7e0-4b24-ad95-ab8f05519227)


## Result:

Thus the given Boolean functions are implemented in Verilog HDL and the truth table are verified.



