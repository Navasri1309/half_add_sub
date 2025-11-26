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

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

 Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
```
Developed by:NAVASRI.B
RegisterNumber:25006773
```
```
module half_adder(
    input  wire a, b,     
    output wire sum,     
    output wire carry    
);

    assign sum   = a ^ b;  
    assign carry = a & b;  

endmodule
```
```
module half_subtractor (
    input  wire a, b,        
    output wire diff, borrow  
);

    assign diff   = a ^ b;    
    assign borrow = ~a & b;   

endmodule

```

**RTL Schematic**

<img width="891" height="457" alt="Screenshot 2025-11-26 132645" src="https://github.com/user-attachments/assets/e952ad02-ecf2-4fb4-8afc-ea9801e041bd" />

<img width="921" height="386" alt="Screenshot 2025-11-26 133010" src="https://github.com/user-attachments/assets/b77b5f8e-71c4-4ce4-8608-5ec15ae0d49a" />

**Output/TIMING Waveform**

<img width="1920" height="1140" alt="Screenshot 2025-11-26 133437" src="https://github.com/user-attachments/assets/c5e48766-0211-4e31-a54b-5d2d88d40ec3" />

<img width="1920" height="1140" alt="Screenshot 2025-11-26 133955" src="https://github.com/user-attachments/assets/c23951a2-ad42-4742-94e9-188b5e77309b" />

**Result:**

Designed a half adder and half subtractor circuit and verified in truth table in Quartus using verilog programming
