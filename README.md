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
Full Adder
<img width="305" height="406" alt="Screenshot 2025-12-18 092214" src="https://github.com/user-attachments/assets/dc4e1f63-0d57-4b23-8a78-1a054b4d8635" />

Subtractor
<img width="394" height="435" alt="Screenshot 2025-12-18 092307" src="https://github.com/user-attachments/assets/343bb398-8432-4475-bd89-5a3ab74d6225" />

**Procedure**
1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.


**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Full adder:

module full_sum(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor g1(sum,a,b,c);
assign carry=((a & b)|( b & c )|(c & a));
endmodule

Full Subtractor:

module full_sub(a,b,c,diff,borr);
input a,b,c;
output diff,borr;
xor g1(diff,a,b,c);
assign borr=((~a & b)|( b & c )|(~a &)c);
endmodule

Developed by:R Dinesh Karthick
RegisterNumber:25018555


**RTL Schematic**
Full Adder
<img width="1611" height="845" alt="image" src="https://github.com/user-attachments/assets/a323a2f5-dd6c-4372-a9ed-c0a11dcf2dab" />

Subtractor
<img width="1523" height="824" alt="image" src="https://github.com/user-attachments/assets/6fbf13a4-f87d-4a32-8aaf-6da72d22bdb9" />

**Output Timing Waveform**
Full Adder 
<img width="1917" height="538" alt="image" src="https://github.com/user-attachments/assets/012d20c1-7059-4b49-a627-a23ab85e1b88" />

Subtractor
<img width="1914" height="628" alt="image" src="https://github.com/user-attachments/assets/5cb2a5d2-b9f4-492a-ae62-3cd6b8c499f0" />

**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



