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
 
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
```
HALF ADDER  

module HalfAdder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule  

FULL ADDER  

module FullAdder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule 
```

Developed by: Adhithya M R
RegisterNumber:  212222240002

Logic symbol


![Screenshot (8)](https://user-images.githubusercontent.com/121557017/211144326-1577e59c-846f-4c49-8ca5-c8ef6e6fe8e6.png)


RTL realization

 Output:
 
 HALFAADER
  
 ![Screenshot (1)](https://user-images.githubusercontent.com/121557017/211144407-20f20114-731f-4bf7-941f-d9c71c1938c2.png)


FULLADDER

![Screenshot (2)](https://user-images.githubusercontent.com/121557017/211144284-aaa660c1-6d8f-41db-b6e1-ee6f4af68420.png)

 
 RTL
 TIMING DIAGRAM

HALFADDER
![Screenshot (11)](https://user-images.githubusercontent.com/121557017/211144550-2a30a7d3-ec8f-43bd-bcfe-033d28603e56.png)

FULLADDER

![Screenshot (13)](https://user-images.githubusercontent.com/121557017/211144645-274f8455-3fad-4f94-bd23-a480404e71da.png)

TRUTH TABLE 

HALFADDER

![Screenshot (9)](https://user-images.githubusercontent.com/121557017/211144749-1be6a19e-cce0-4a0a-ba9d-8a9002825425.png)


FULLADDER

![Screenshot (12)](https://user-images.githubusercontent.com/121557017/211144794-f2431619-1b89-4e89-bf9f-83a53f9e9704.png)

 Result:
     Thus the Implementation of Halfadder Fulladder Circuit are studied and the truthtable for different logic gates are verified
