# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. */
```
Developed by:  Rishab p doshi
RegisterNumber: 212224240134
```
```
Full adder

module exp31(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=(a^b^cin);
assign carry=((a&b)|((a^b)&cin));
endmodule
```
```
Full subtractor

module exp32(a,b,bin,diff,borr);
input a,b,bin;
output diff,borr;
assign diff=((~a&b)|(~(a^b)&bin));
assign borr=((~a&b)|(b&bin)|(~a&bin));
endmodule
```
**RTL Schematic**
### Full Adder
![image](https://github.com/user-attachments/assets/055b68c5-adce-4069-9868-cbef6568e798)

### Full Subtractor
![image](https://github.com/user-attachments/assets/7ca03269-2687-4b7f-b3ba-6f38c2d6b607)


**Output Timing Waveform**

### Full Adder
![image](https://github.com/user-attachments/assets/090b1719-4f36-4212-9f70-34de627f6e44)

### Full Subtractor

![image](https://github.com/user-attachments/assets/0a744f63-9704-45a0-927c-61632ecf630d)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



