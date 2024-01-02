## Name: varsha.k

## ref number: 23005952

# Exp 02 Implementation of Half Adder and Full Adder circuit:
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
# Program:
# Half adder:
```
module exp3(sum, carry,a,b); 
input a,b; 
output sum,carry; 
xor sum1(sum,a,b); 
and carry1(carry,a,b); 
endmodule
```
# full adder:
```
module fulladder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b | b&c | a&c;
endmodule
```

# RTL realisation:
# Half Adder:
![image](https://github.com/Varshakumaran/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979367/6422ea4e-c4b9-495b-ae95-2a4aea82ce4a)
# Full Adder:
![image](https://github.com/Varshakumaran/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979367/fa95f593-9b97-487c-936d-c086f7659e8c)

### TIMING DIAGRAM
# Half Adder:
![image](https://github.com/Varshakumaran/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979367/67923fcf-95b0-433d-ae6f-17757770736a)
# Full Adder:
![image](https://github.com/Varshakumaran/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979367/fea0a5be-d72e-4b78-8ca8-ce09d347044e)

### TRUTH TABLE :
# Half Adder:
![image](https://github.com/Varshakumaran/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979367/7eb3c113-28cb-4388-9f66-0f3853bd9413)
# Full Adder:
![image](https://github.com/Varshakumaran/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979367/61c60d0c-2c50-4286-9c31-c5460ade0e87)

### Result:
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
