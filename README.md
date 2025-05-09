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


![WhatsApp Image 2025-04-23 at 14 17 22_bd8c8f56](https://github.com/user-attachments/assets/f5561a71-51c9-4bc7-a5b0-301d696d8631)
![WhatsApp Image 2025-04-23 at 14 17 36_a45dba96](https://github.com/user-attachments/assets/84b92f74-9d3c-490b-8613-3598bdd4b4ad)



**Procedure**
```
Write the detailed procedure here
Full Adder: 
1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit.
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation.
5.Implement the design on the target device and program it.

Full Subtractor: 
1.Follow the same steps as for the full adder.
2.Draw the full subtractor circuit using schematic design. 
3.The circuit includes XOR, AND, OR gates to perform subtraction.
4.Compile, simulate, implement, and program the design similarly to the full adder.
```
**Program:**
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: G P HARIESH RegisterNumber:212224040100
*/
FULL-ADDER
module hari(sum, cout, a, b, cin);
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

FULL SUBTRACTOR
module exp4a(df, bo, a, b, bin);
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
**RTL Schematic**
![Screenshot (111)](https://github.com/user-attachments/assets/b59156d9-cacf-47ac-ad96-27c04e370b21)

![Screenshot (113)](https://github.com/user-attachments/assets/b8446902-7dc2-42f2-a14e-f3b6baba63ad)

**Output Timing Waveform**
![Screenshot (112)](https://github.com/user-attachments/assets/a9ada48c-49a7-4e80-99d2-566f610b9c1d)

![Screenshot (114)](https://github.com/user-attachments/assets/cb37fea8-32e3-44e7-9f4a-ac94325be980)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



