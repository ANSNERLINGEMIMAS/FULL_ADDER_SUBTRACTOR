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
FULL ADDER
![Screenshot 2025-04-07 141723](https://github.com/user-attachments/assets/57e8e5cf-8ee7-428f-a781-6fd024a2b820)

FULL SUBTRACTOR
![Screenshot 2025-04-07 141742](https://github.com/user-attachments/assets/7076b4af-1196-420d-beae-72efc934631c)


**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
```
exp4a
module exp4a(sum, cout, a, b, cin);
    output sum;
    output cout;
    input a;
    input b;
    input cin;

	 wire w1,w2,w3;
	 assign w1=a^b;
	 assign w2=a&b;
	 assign w3=w1&cin;
	 assign sum=w1^cin;
	 assign cout=w2|w3;
endmodule

exp4b
module exp4b(df, bo, a, b, bin);
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
```
Developed by: ANS NERLING EMIMA SRegisterNumber:212224020027
*/

**RTL Schematic**
![exp4a](https://github.com/user-attachments/assets/49c0aa92-b244-4c7d-bcf5-845403b2cf4f)

![exp4b](https://github.com/user-attachments/assets/0aa9147e-2840-48f2-a035-3ae2082d3a4f)



**Output Timing Waveform**
![Screenshot 2025-04-07 140838](https://github.com/user-attachments/assets/cfaa0de5-1dd1-480f-8112-1a571a36fa8b)

![Screenshot 2025-04-07 141447](https://github.com/user-attachments/assets/2a932624-d991-47f7-baf4-10df472665e0)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



