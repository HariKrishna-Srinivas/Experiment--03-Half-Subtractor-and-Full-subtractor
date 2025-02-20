# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure:

Write the detailed procedure here 
1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output to represnt onre for differnce and the other for borrow.

5.End the verilog program using keyword endmodule.

## Program:
~~~
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: M.Harikrishna
RegisterNumber: 212221230059

Half Subractor:
module exp3(output B,D, input X,Y);
assign D = (X ^ Y);
assign B = (~X & Y);
endmodule

Full Subractor:
module exp3(X,Y,Z,B,D);
input X,Y,Z;
output B,D;
assign D = (X^Y^Z);
assign B = (~X&(Y^Z)|(Y&Z));
endmodule

~~~
## Output:
HALF SUBTRACTOR
Logic Symbol
![image](https://user-images.githubusercontent.com/94882905/196426249-890f236a-ed0e-4a95-a4b1-e10c7e94ba48.png)

## Truthtable
![image](https://user-images.githubusercontent.com/94882905/196426367-6283cc6f-01ad-4434-b755-6fbe59d19899.png)



##  RTL realization
![image](https://user-images.githubusercontent.com/94882905/196426440-0edb33a7-4382-44ef-832c-a9afb925735e.png)


## Timing diagram 
![image](https://user-images.githubusercontent.com/94882905/196426515-e4704939-a423-4354-9bb8-5cf0003c6b06.png)

FULL SUBTRACTOR
Logic Symbol

![image](https://user-images.githubusercontent.com/94882905/196426681-e8ae9153-4a1e-410b-af52-70cb6b922c02.png)

Truthtable
![image](https://user-images.githubusercontent.com/94882905/196426806-8b01dd73-609a-473c-bf4d-072d1d52a173.png)

RTL realization
![image](https://user-images.githubusercontent.com/94882905/196426977-00129bb2-0346-493e-b600-981f861b3240.png)

Timing diagram
![image](https://user-images.githubusercontent.com/94882905/196427130-532c574e-33d3-40c9-9e4b-013271be36b3.png)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
