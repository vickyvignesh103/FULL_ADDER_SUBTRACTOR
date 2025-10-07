# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flas

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
![WhatsApp Image 2025-10-07 at 10 21 08_f6585e61](https://github.com/user-attachments/assets/3d5be001-52a2-4185-ad03-ea2d41e033f2)
![WhatsApp Image 2025-10-07 at 10 21 44_f7830ea3](https://github.com/user-attachments/assets/b09b741b-dd14-43d4-9146-a1c7e8bbd8ee)

**Procedure**

Write the detailed procedure here

**Program:**
module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/ module fs(a, b, bin, difference, borrow);
    input a, b, bin;
    output difference, borrow;

    assign difference = (a ^ b) ^ bin;
    assign borrow = ((~a & b) | (bin & ~(a ^ b)));

endmodule

**RTL Schematic**
<img width="639" height="297" alt="Screenshot 2025-10-07 101352" src="https://github.com/user-attachments/assets/2cd0ea1f-74c0-425e-8775-aa6d6b98077c" />
<img width="659" height="245" alt="Screenshot 2025-10-07 103755" src="https://github.com/user-attachments/assets/9535fdf6-e0f3-4655-9f45-9288b75773a7" />

**Output Timing Waveform**
<img width="1919" height="984" alt="Screenshot 2025-10-07 101716" src="https://github.com/user-attachments/assets/5934945e-ad59-40fd-9c9f-62141c9fc08d" />
<img width="1919" height="997" alt="Screenshot 2025-10-07 104039" src="https://github.com/user-attachments/assets/7b86a6fa-a509-4540-a1d4-52f45ace09a8" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



