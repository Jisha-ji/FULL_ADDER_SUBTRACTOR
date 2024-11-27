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

![image](https://github.com/user-attachments/assets/0cdf9cfc-be0d-43ab-b196-46600871b585)

**Procedure**

1.Type the program in Quartus software.
2.Compile and run the program.
3.Generate the RTL schematic and save the logic diagram.
4.Create nodes for inputs and outputs to generate the timing diagram.
5.For different input combinations generate the timing diagram.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: Jisha Bossne SJ RegisterNumber: 24900154
*/
```
module fa(A,B,Cin,sum,carry);
input A,B,Cin;
output sum,carry;
assign sum=(A^B^Cin);
assign carry=(A&B)|((A^B)&Cin);
endmodule
```
```
module fs(A,B,Bin,diff,borr);
input A,B,Bin;
output diff,borr;
assign diff=(A^B^Bin);
assign borr=((~A&B)|(~(A^B)&Bin));
endmodule
```
**RTL Schematic**

Full-adder:
![image](https://github.com/user-attachments/assets/dd7065ca-346c-4c03-a016-784ba46aef68)


Full-subtractor:
![image](https://github.com/user-attachments/assets/a1fd6fbd-7fe4-4ffe-9489-6d8b1a44b3ce)


**Output Timing Waveform**

Full-adder:

![Screenshot (28)](https://github.com/user-attachments/assets/11d04851-09d1-4b30-a778-e8fc61e6910f)

Full-subtractor:

![funct4a](https://github.com/user-attachments/assets/691a8611-dd90-42a0-b81a-ea6361d581fb)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



