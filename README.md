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

## Procedure



Write the detailed procedure here 


## Program:
```
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Meetha Prabhu 
RegisterNumber: 21222240065
Half-Subtractor :

module experiment4(output B,D, input X,Y);
assign D = (X^Y);
assign B = (~X&Y); 
endmodule

Full-Subtractor:
module experiment4(X,Y,Z,Borrow,Difference);
input X,Y,Z;
output Borrow,Difference;
assign Difference = (X^Y^Z);
assign Borrow =(~X&(Y^Z)|(Y&Z));
endmodule
```
*/

##  RTL realization
Half-Subtractor
![image](https://user-images.githubusercontent.com/119401038/230594707-ea71a6f7-6fd8-4eca-9558-a44a25c7f18b.png)

Full-Subtractor
![image](https://user-images.githubusercontent.com/119401038/230595177-3645af34-8588-4236-8464-7ff0263a0219.png)

Timing Diagram:

Half Subtractor:

![image](https://github.com/Meetha22003992/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119401038/d88a814a-1936-453c-ac89-89c27bb6f974)


Full Subtractor:

![image](https://github.com/Meetha22003992/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119401038/35a4a8e3-972b-425a-85b2-170f5d6eadb5)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
