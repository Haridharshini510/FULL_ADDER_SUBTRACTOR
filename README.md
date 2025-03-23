Name: Haridharshini J

Register number: 212224040098

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
Full adder

![full-adder2](https://github.com/user-attachments/assets/f1b97b90-99c1-40fa-b822-952e78abf5b5)

Full subtractor

![full-subtractor2](https://github.com/user-attachments/assets/6b8be48d-26bf-4699-bd95-8ed1857adb8f)



**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**

    module ex3(a, b, c, sum, carry, diff, borrow);

    input a, b, c;
    
    output sum, carry, diff, borrow;
    
    xor g1(sum, a, b, c);  
    
    or  g2(carry, (a & b), (b & c), (c & a)); 
    
    xor g3(diff, a, b, c);   
    
    not g4(na, a);  
    
    and g5(w5, na, b); 
    
    and g6(w6, na, c); 
    
    and g7(w7, b, c);
    
    or  g8(borrow, w5, w6, w7);
    endmodule

**RTL Schematic**

![Screenshot (363)](https://github.com/user-attachments/assets/30ae4579-798c-4948-b280-fb433c097a8c)

**Output Timing Waveform**

![Screenshot (363)](https://github.com/user-attachments/assets/a1bfd5fa-9169-44ea-8e9b-223a5f2c9c0a)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



