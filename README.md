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

![WhatsApp Image 2024-12-21 at 09 58 41_c5d10d83](https://github.com/user-attachments/assets/55971062-14db-4220-843a-af1109575130)

![WhatsApp Image 2024-12-21 at 09 59 00_9c3ece0c](https://github.com/user-attachments/assets/d0927c21-69a1-42fa-9014-a15d140260f8)


**Procedure**

1. Type the program in Quartus software.

2. Compile and run the program.

3. Generate the RTL schematic and save the logic diagram.
 
4. Create nodes for inputs and outputs to generate the timing diagram.

5. For different input combinations generate the timing diagram.

**Program:**

i)FULL ADDER

module fa(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule

ii)FULL SUBTRACTOR

module fs(a,b,bin,difference,borrow);

input a,b,bin;

output difference,borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));

endmodule


**RTL Schematic**

![WhatsApp Image 2024-12-23 at 08 25 28_6becfe7a](https://github.com/user-attachments/assets/9b747d90-db99-4bc3-b23a-58f4f461fdd3)

![WhatsApp Image 2024-12-23 at 08 24 11_08f1e0de](https://github.com/user-attachments/assets/702189c6-601c-4109-9015-273388724899)


**Output Timing Waveform**

![WhatsApp Image 2024-12-23 at 08 26 40_7fab6558](https://github.com/user-attachments/assets/0af15a02-d901-42e0-bb81-349d90f24280)

![WhatsApp Image 2024-12-23 at 08 29 24_1d4768b6](https://github.com/user-attachments/assets/89077a3f-b5de-48e1-b16e-e6a117a80d9f)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



