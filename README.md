Name: Sai Darshan

Register Number: 2212221240047

# Experiment--02-Implementation-of-combinational-logic

 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
 
 
 
## Equipments Required:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime


## Theory
 
# Logic Diagram
Using NOR gates NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

## Procedure
1.Using NAND gates and wires contruct.

2.Construct the same for using NOR gates and wires.

3.Find RTL and Timing Diagram for both the expressions.

4.End the program.

## Program:
```
module exp2(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire x1,x2,x3,x4,x5;


assign x1=(~A)&(~B)&(~C)&(~D);
assign x2=(A)&(~C)&(~D);
assign x3=(~B)&(C)&(~D);
assign x4=(~A)&(B)&(C)&(D);
assign x5=(B)&(~C)&(D);

assign F1=x1|x2|x3|x4|x5;
endmodule

```
## Truth Table

![image](https://github.com/SaiDarshan2003/Experiment--02-Implementation-of-combinational-logic-/assets/94692595/d18d6192-041f-4616-b104-88c1e83c1302)

## RTL
![Screenshot 2023-08-26 083352](https://github.com/SaiDarshan2003/Experiment--02-Implementation-of-combinational-logic-/assets/94692595/865bcda9-a7ab-45bb-845a-9a4f8b360d14)

## Timing Diagram
![Screenshot 2023-08-26 094521](https://github.com/SaiDarshan2003/Experiment--02-Implementation-of-combinational-logic-/assets/94692595/2b8a0299-9efb-4c8a-a944-2447913d4214)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
