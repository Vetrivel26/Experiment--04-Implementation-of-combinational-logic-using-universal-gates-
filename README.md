# Experiment--04-Implementation-of-combinational-logic-using-universal-gates-
 ## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.
F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate


## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory

## Procedure

1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.


## Program:
/*
Program to design a Implementation of combinational logic using universal gates-  and verify its truth table in quartus using Verilog programming.
Developed by: VETRIVEL S
RegisterNumber:  212221240060

## F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate

module Combination(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R;
assign P = C&(~B)&(~A);
assign Q = D&(~C)&(~A);
assign R = (~C)&B&(~A);
assign F = (~P&~Q&~R);
endmodule

## F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate

module norcombination(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R,S;
assign P = C&(~B)&A;
assign Q = D&(~C)&A;
assign R = C&(~B)&A;
assign S = ~(P|Q|R);
not(F,S);
endmodule 
*/

## Output:
F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
## Truthtable
![t1](https://user-images.githubusercontent.com/95363138/167691146-fac95c73-4cbd-47f4-a627-cddebb0ce75f.png)
##  RTL realization
![d1](https://user-images.githubusercontent.com/95363138/167691183-aee7d0c8-5da6-4b1b-aaa3-81cbf6650318.png)
## Timing diagram 
![td1](https://user-images.githubusercontent.com/95363138/167691207-9c9ea46b-ffd5-4096-bb66-7ff4d3a30fe6.png)
## Truthtable
![t2](https://user-images.githubusercontent.com/95363138/167691277-59432976-237b-4886-9c9f-f56b86a6734d.png)
## RTL realization
![d2](https://user-images.githubusercontent.com/95363138/167691357-53a3ea5b-fa44-461d-92ae-4ee2805b89a6.png)
## Timing diagram
![td2](https://user-images.githubusercontent.com/95363138/167691445-c0598963-6741-4315-9c1b-91a38e488323.png)
## Result:
 Thus implementation of logic functions using NAND and NOR gates is done and its operation is verified in Quartus using Verilog programming.
