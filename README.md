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
![full adder](https://github.com/user-attachments/assets/3c64b77c-f49a-4046-b3d4-3534eef8a8f8)

![full sub](https://github.com/user-attachments/assets/96fd6aa5-0ae7-47b4-ad85-c15b77ab6f4b)

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
# Developed by: LAKSHMIDHAR  N       RegisterNumber: 24900046
    module exp4(sum,cout,a,b,cin);
    output sum;
    output cout;
    input a;
    input b;
    input cin;
    wire s1,c1,c2;
    xor(s1,a,b);
    and(c1,a,b);
    xor(sum,s1,cin);
    and(c2,s1,cin);
    or(cout,c2,c1);
    endmodule


    module exp4a(df,bo,a,b,bin);
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


**RTL Schematic**
FULL - ADDER
![Screenshot 2024-11-19 102047](https://github.com/user-attachments/assets/15732982-7c94-4373-808a-cbb2d5d81b11)
FULL - SUBTRACTOR
![exp4a rtl](https://github.com/user-attachments/assets/46a060a0-7cf4-4691-801e-573e8ea6e5fc)


**Output Timing Waveform**
FULL - ADDER
![Screenshot 2024-11-19 102336](https://github.com/user-attachments/assets/eabc3f9a-246e-43ff-a16e-d91cdd710768)

FULL - SUBTRACTOR
![Screenshot 2024-11-19 103046](https://github.com/user-attachments/assets/82bbb205-f8a1-4c0f-82ba-b90fa7d290b0)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



