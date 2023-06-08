### Experiment--02-Implementation-of-combinational-logic
### Implementation of combinational logic gates

### AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming. 
F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 
F2=xy’z+x’y’z+w’xy+wx’y+wxy

### Equipments Required:
1.Hardware – PCs, Cyclone II , USB flasher
2.Software – Quartus prime

### Theory:
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

1.AND gate The AND gate is an electronic circuit that gives a high output (1) only if all its inputs are high. A dot (.) is used to show the AND operation i.e. A.B or can be written as AB Y= A.B

2.OR gate The OR gate is an electronic circuit that gives a high output (1) if one or more of its inputs are high. A plus (+) is used to show the OR operation. Y= A+B

### Logic Diagram:

### Procedure:
1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.

### Program:
```
/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 
Developed by: S.SHANMATHI 
RegisterNumber: 212222100049
*/
module logic(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire A1,A2,A3,A4,A5,B1,B2,B3,B4,B5;
assign A1=((~a)&(~b)&(~c)&(~d));
assign A2=(a&(~c)&(~d));
assign A3=((~b)&c&(~d));
assign A4=((~a)&b&c&d);
assign A5=(b&(~c)&d);
assign B1=(x&(~y)&z);
assign B2=((~x)&(~y)&z);
assign B3=((~w)&x&y);
assign B4=(w&(~x)&y);
assign B5=(w&x&y);
assign f1=A1|A2|A3|A4|A5;
assign f2=B1|B2|B3|B4|B5;
endmodule
```



### RTL realization:
![combilogic1](https://user-images.githubusercontent.com/121215739/234776673-b7a5ef09-5f27-40c6-ae87-a7633af82e04.png)
![combilogic2](https://user-images.githubusercontent.com/121215739/234776690-bffe1289-66bb-4746-bbf9-3e86a6489353.png)


### Truth Table:
![truthtable](https://user-images.githubusercontent.com/121215739/234778196-86915610-ab49-47ff-b6aa-f50976aaffa2.jpg)

### Result:
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
