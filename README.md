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

full adder:

<img width="500" height="281" alt="image" src="https://github.com/user-attachments/assets/88bdb637-b2e4-468a-90ee-d4880eb54925" />


full subtractor:

<img width="361" height="236" alt="image" src="https://github.com/user-attachments/assets/ac9abecc-daff-4f10-b5ef-587d649626e9" />


**Procedure**

Write the detailed procedure here

**Program:**

full adder:
```
module fulladder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum=(a^b^c);
assign carry=(a & b)|(b & c)|(c & a);
endmodule
```
full subtractor:

```
module fullsub(a,b,c,dif,bor);
input a,b,c;
output dif,bor;
assign dif=a^b^c;
assign bor=(~a&b)|(b&c)|(~a&c);
endmodule
```


/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL Schematic**

full adder:

<img width="1334" height="877" alt="image" src="https://github.com/user-attachments/assets/af45abf9-934f-4c64-962a-77983f654ff2" />


full subtractor:

<img width="1233" height="766" alt="image" src="https://github.com/user-attachments/assets/e1170523-9ee4-4859-9b45-28c674592a91" />




**Output Timing Waveform**

full adder:

<img width="1920" height="1125" alt="image" src="https://github.com/user-attachments/assets/8b40a038-bd31-4de8-a9f9-18e353e879d9" />

full subtractor:

<img width="1920" height="1128" alt="image" src="https://github.com/user-attachments/assets/732ddd33-97da-429d-a2ff-e394e3eb82ef" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



