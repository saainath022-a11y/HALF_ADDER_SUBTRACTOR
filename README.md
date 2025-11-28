# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**
**Hald Adder**
<img width="424" height="249" alt="388823715-5ddc52ef-d125-4442-8265-139c2bb7c6e7" src="https://github.com/user-attachments/assets/799c48cf-ce95-4c99-b73d-d7bc174c9a14" />
**Full Subtractor**
<img width="436" height="248" alt="388822335-83ec047b-4a5b-42ea-ac00-af7c49740ea2" src="https://github.com/user-attachments/assets/d5d795a2-d24d-4a4e-9ac5-11f8da375274" />

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```
module ex4 (a,b,c,x,y,z,sum,dif,car,bor);
input a,b,c,x,y,z;
output sum,dif,car,bor;
assign sum = a^b^c;
assign car = a&b | a&c | b&c;
assign dif = x^y^z;
assign bor = ~x&z | ~x&y | y&z;
endmodule


```

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by:SAAINATH B RegisterNumber:25016015

**RTL Schematic**
<img width="1920" height="1080" alt="Screenshot (57)" src="https://github.com/user-attachments/assets/7235290e-8fa3-4697-855f-8642c4c2c6db" />

**Output/TIMING Waveform**
<img width="1920" height="1080" alt="Screenshot (58)" src="https://github.com/user-attachments/assets/cf4466d7-5d48-4117-a755-73667142f012" />

**Result:**
Thus the Half Adder and Half Subtractor are studied and the truth tables are verified

