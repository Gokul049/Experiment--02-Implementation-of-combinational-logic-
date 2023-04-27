# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
 

## Logic Diagram
## Procedure
## Program:

```
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by:Gokul T 
RegisterNumber:212222050015  
*/
 
module cpmbine(a,b,c,d,f);
input a,b,c,d;
output f;
wire p,q,r;
assign p=(~c & b & a);
assign q=(~d & c & c & a);
assign r=(c & ~b & a);
assign f=(~(~p & ~q & ~r));
endmodule

module combine1(a,b,c,d,f);
input a,b,c,d;
output f;
wire p,q,r;
assign p=(c & ~b & a);
assign q=(d & ~c & a);
assign r=(c & ~b & a);
assign f=((p | q & |r));
endmodule
```
## RTL realization

## Output:
## RTL
![image](https://user-images.githubusercontent.com/131269675/234775476-1ad07c02-4b90-459f-bb09-4d1ff16d8ad9.png)
![image](https://user-images.githubusercontent.com/131269675/234775495-039b110a-dafd-479f-bb3b-4bf2abf8752a.png)


## Timing Diagram
![image](https://user-images.githubusercontent.com/131269675/234775522-01375501-8862-4ee6-b946-d1d9f2e1dcc7.png)
![image](https://user-images.githubusercontent.com/131269675/234775545-97477a0a-6e36-48c0-bc3e-3e24c0a23f06.png)


## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
