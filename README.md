# ARITHMETIC-LOGIC-UNIT-ALU-
* Company*: CODTECH IT SOLUTION
* NAME*:KARANAM UDAYKUMAR
* INTERN ID*: CT12WX115
* DOMAIN*: VLSI
* DURATION*: 3 MONTHS
* MENTOR*: NEELA SANTHOSH




# DESCRIPTION FOR THE PROJECT ( ARITHMETIC LOGIC UNIT )

![1](https://github.com/user-attachments/assets/957db10b-c711-47ab-8e8a-4d1f6092c272)

Basic ALU Design Supporting Addition, Subtraction, AND, OR, and NOT Operations
An Arithmetic Logic Unit (ALU) is a fundamental component of digital systems, responsible for performing arithmetic and logical operations. This description outlines a basic ALU design that supports addition, subtraction, AND, OR, and NOT operations.
![2](https://github.com/user-attachments/assets/07940b95-631e-4eb0-b053-f4d2e26223d2)

#ALU Operations
The ALU will support the following operations:

1. Addition: Performs arithmetic addition of two operands.
2. Subtraction: Performs arithmetic subtraction of two operands.
3. AND: Performs bitwise AND operation on two operands.
4. OR: Performs bitwise OR operation on two operands.
5. NOT: Performs bitwise NOT operation on a single operand.

ALU Design
The ALU design will consist of the following components:

1. Arithmetic Circuit: Performs addition and subtraction operations.
2. Logic Circuit: Performs AND, OR, and NOT operations.
3. Multiplexer: Selects the output of the arithmetic or logic circuit based on the operation code.

#Operation Codes
The ALU will use operation codes to determine which operation to perform. The operation codes will be as follows:

1. 000: Addition
2. 001: Subtraction
3. 010: AND
4. 011: OR
5. 100: NOT


## VERILOG CODE :

module ALU_1 (A,B,Op, alu_out);
input [3:0]A, B;
input [2:0] Op;
output reg [3:0] alu_out;
always@(*)
begin
case (Op)
      3'b000: alu_out= 0;
      3'b001: alu_out= A+B; 
      3'b010: alu_out= A-B;
      3'b011: alu_out= A&B;
      3'b100: alu_out= A|B;
      3'b101: alu_out= ~A;
      3'b110: alu_out= ~B;
      default: alu_out= 0;
  endcase
end   
endmodule 



## TESTBENCH CODE

module tb_alu(A,B,op,alu_out);
reg [3:0]A,B;
reg [2:0]op ;
wire [3:0] alu_out;
initial
begin
  op=3'b000; A=3'b0011; B=3'b0001;
  #10;
  op=3'b001; A=3'b0011; B=3'b0001;
  #10;
  op=3'b010; A=3'b0011; B=3'b0001;
  #10;
  op=3'b011; A=3'b0011; B=3'b0001;
  #10;
  op=3'b100; A=3'b0011; B=3'b0001;
  #10;
  op=3'b101; A=3'b0011; B=3'b0001;
  #10;
 end
endmodule




#ALU Implementation
The ALU can be implemented using Verilog HDL. The implementation will involve designing the arithmetic and logic circuits, multiplexer, and operation code decoder.

#Benefits
The basic ALU design supporting addition, subtraction, AND, OR, and NOT operations provides a fundamental building block for digital systems. It can be used in a variety of applications, including:

1. Microprocessors: The ALU is a critical component of microprocessors, performing arithmetic and logical operations.
2. Digital Signal Processing: The ALU can be used in digital signal processing applications, such as filtering and convolution.
3. Cryptography: The ALU can be used in cryptographic applications, such as encryption and decryption.

#Conclusion
In conclusion, a basic ALU design supporting addition, subtraction, AND, OR, and NOT operations provides a fundamental building block for digital systems. The ALU design can be implemented using Verilog HDL and can be used in a variety of applications.


# OUTPUT

![Image](https://github.com/user-attachments/assets/adfc0613-4cee-4917-a3bd-a34f933ed024)
![Image](https://github.com/user-attachments/assets/28fb8bdd-6af2-418b-9fab-5cbd76dbd559)
