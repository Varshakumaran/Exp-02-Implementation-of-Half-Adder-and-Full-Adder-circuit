Name: varsha.k

ref no: 23005952

# Exp 02 Implementation of Half Adder and Full Adder circuit

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

## Program
module project_3(sum,carry,a,b); 
input a,b; 
output sum,carry; 
xor sum1(sum,a,b); 
and carry1(carry,a,b); 
endmodule

## RTL
![image](https://github.com/vasanthkumarch/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979367/af10e619-ba48-4571-8ae2-be32a323e99b)

## Timing Diagram
![image](https://github.com/vasanthkumarch/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979367/83ae0bd1-7e01-4ba8-9326-0389ce1c584e)

## Truth TABLE
![image](https://github.com/vasanthkumarch/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979367/e0317f3b-ae4c-41d8-8f27-0c299d1d6527)

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
## Full Adder:
module project_3_2(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b | b&c | a&c;
endmodule


### Output:
### RTL
![image](https://github.com/vasanthkumarch/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979367/223a33fd-ae37-4499-b4bf-d9041c894ece)

### TIMING DIAGRAM
![image](https://github.com/vasanthkumarch/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979367/f13cdfde-2903-4311-a88f-f355f2deba77)


### TRUTH TABLE 
![image](https://github.com/vasanthkumarch/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979367/6379982d-5747-480e-8419-61efb99c1054)

### Result:
Thus the given logic functions are implemented and their operations are verified using verilog programming
