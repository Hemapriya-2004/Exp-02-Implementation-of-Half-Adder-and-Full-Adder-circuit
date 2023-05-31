# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by:R.HEMAPRIYA 
RegisterNumber:212221230036
*/

## HALF ADDER

module Adder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 

## FULL ADDER

module FullAdder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```
### Output:
## HALF ADDER
## TRUTH TABLE
![231674977-5adf488c-1388-4753-9512-7cfc868a3c59](https://user-images.githubusercontent.com/94184828/232230888-3439e1dc-17e7-4223-99c3-caa6fdbfbd91.png)
## RTL
![231675013-160477f4-cb65-4eef-aa91-95bfd6a68db4](https://user-images.githubusercontent.com/94184828/232230895-623408fa-19ed-4e0c-a232-2198d7283eab.png)
## TIMING DIAGRAM
![output](https://github.com/Hemapriya-2004/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/blob/main/i1.png)
## FULL ADDER

![231675144-d70b786b-690e-4ffd-9ad5-7a54097c5cc5](https://user-images.githubusercontent.com/94184828/232230923-248fa731-31ca-4b07-b76d-c0c4c8b4fa49.png)

## RTL
![231675204-a0e69240-1e04-443e-80f0-04666b2df148](https://user-images.githubusercontent.com/94184828/232230936-abf822ff-8c5d-4af9-bad7-739549a6b5e2.png)
## TIMING DIAGRAM
![output](https://github.com/Hemapriya-2004/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/blob/main/i1.png)



### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
