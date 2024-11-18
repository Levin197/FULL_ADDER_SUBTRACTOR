# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Truthtable**
![baf9fc4a-5201-4f70-ae3b-2bd7f06af0c3](https://github.com/user-attachments/assets/6c9ea44f-bde3-4755-bff1-8a1dcb723e0f)

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
![d1b561f3-5a31-44fd-832f-31a5a808d3d9](https://github.com/user-attachments/assets/347c36f0-bb0e-4828-b3d0-58b597a78487)

**Program:**
module unit22(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
wire s1,c1,c2;
xor (s1,a,b);
and(c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);
endmodule


module unit23 (df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL Schematic**
![unit22](https://github.com/user-attachments/assets/b27edc81-082b-4ca8-8c7b-4e4077173ce8)
![WhatsApp Image 2024-11-18 at 14 20 21](https://github.com/user-attachments/assets/80d21cf6-c867-4cfc-a86b-212d27b6eace)

**Output Timing Waveform**
![Screenshot 2024-11-18 141119](https://github.com/user-attachments/assets/48a4f5f8-8fba-43ea-936f-e9c93c2cbede)
![19a7a95d-0059-47f7-8d43-aa03aa9d90f6](https://github.com/user-attachments/assets/b2d3e81e-5465-4eb2-94ea-a313e2b00b7c)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



