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

## Truthtable
<img width="513" height="398" alt="image" src="https://github.com/user-attachments/assets/907b0987-c815-4da0-81cb-483fe0c1dd5a" />

**Procedure**

01. Type the program in Quartus software.

02. Compile and run the program.

03. Generate the RTL schematic and save the logic diagram.

04. Create nodes for inputs and outputs to generate the timing diagram.

05. For different input combinations generate the timing diagram.

**Program:**

 Developed by:Venkatesan R RegisterNumber: 212224230299
```
module EXP4(a,b,sum, cin, carry, bin, BO, DIFF);
input a,b,cin, bin;
output sum, carry, BO, DIFF;
assign sum=(a^b^cin);
assign carry=((a&b)|(b&cin)|(a&cin));
assign diff=(a^b^bin);
assign BO=((~a&b)|(~a&bin)|(b&bin));
endmodule
```

## RTL Schematic
<img width="813" height="642" alt="Screenshot 2025-09-16 143433" src="https://github.com/user-attachments/assets/15662e03-563a-4244-99cf-e6971ff969ae" />

## Output Timing Waveform
<img width="1919" height="458" alt="Screenshot 2025-09-16 143627" src="https://github.com/user-attachments/assets/aec11f67-1402-4ec5-add7-be7b355301a9" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



