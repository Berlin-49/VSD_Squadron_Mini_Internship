# VSD_Squadron_Mini_Internship
## Week 1
### RISCv GNU TOOL

* Cloning using Git Repo https://github.com/riscv-collab/riscv-gnu-toolchain
<img src="https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/cb4fe601-e4b1-4229-96f9-760ea70bcb7f" width="700" height="500"><br>
* installing Linux and New Lib<br>
<img src="https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/9b9bbb01-f2cd-4050-952f-ac88cf89710e" width="700" height="500"><br>
<img src="https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/2f4dea8f-8b57-40c3-9e01-44fa3caacca3" width="700" height="500"><br>

*RISCV GCC testing<br> 
<img src="https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/c94ac7e4-bf68-497d-bbd1-f831b53307a3" width="700" height="500"><br>

  
### INSTALLING YOSYS OPENSOURCE 

* $ git clone https://github.com/YosysHQ/yosys.git<br>
* $ cd yosys<br>
* $ sudo apt-get install build-essential clang bison flex \
      libreadline-dev gawk tcl-dev libffi-dev git \
      graphviz xdot pkg-config python3 libboost-system-dev \
      libboost-python-dev libboost-filesystem-dev zlib1g-dev
* $ make config-gcc<br>
* $ make<br> 
* $ sudo make install<br>
<img src="https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/2ccdef93-5e0f-4602-9ef0-c60eef17f1d8" width="700" height="500"><br>

### INSTALLING IVERILOG

git clone from git hub repo of [Iverilog](https://github.com/steveicarus/iverilog)

<img src="https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/47c2e9a8-f8fe-4529-8f29-ed08f43d6a5f" width="700" height="500"><br>

### INSTALLING GTK WAVE

*sudo update sudo apt install gtkwave<br>
<img src="https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/ec675688-9293-4ea2-b78e-511aa128fd69" width="700" height="500"><br>
<img src="https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/26d5dfbb-113f-4ff2-8497-465a1f467d3d" width="700" height="500"><br>

## Week 2
### RISC-V Instruction Set
The RISC-V instruction set architecture (ISA) has garnered significant attention in both academia and industry due to its open-source nature, scalability, and versatility. This literature survey delves into the core instruction sets of RISC-V, namely R, I, S, B, U, and J, providing insights into their functionalities, design principles, and applications.
#### R INSTRUCTION TYPE
![image](https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/55ea95db-cb8f-4d1c-b844-e4ff156da18b)
*	Opcode (7 bits): Specifies the operation to be performed (e.g., addition, subtraction).
*	Source Register 1 (5 bits): Identifies the first source register for the operation.
*	Source Register 2 (5 bits): Identifies the second source register for the operation.
*	Destination Register (5 bits): Specifies the destination register to store the result.
*	Function Code (6 bits): Further specifies the operation within the opcode category (e.g., type of arithmetic operation).
In the RISC-V ISA, R-type instructions have a fixed format consisting of fields for the opcode, source register operands (typically two), destination register, and function code. These instructions are designed for efficient execution and simplicity, aligning with the RISC (Reduced Instruction Set Computing) philosophy of favoring a smaller, more streamlined instruction set.
R-type instructions cover a wide range of operations, including addition, subtraction, bitwise logical operations (AND, OR, XOR), shifts, and comparisons. They are integral to the core functionality of the processor, providing the groundwork for higher-level operations and algorithms.

####  I INSTRUCTION TYPE
![image](https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/1d3df2f1-93e6-4f7f-87f1-0c0d174f296b)
*	Opcode (7 bits): Indicates the operation to be executed (e.g., load, store, arithmetic operation).
*	Source Register (5 bits): Specifies the source register for the operation.
*	Destination Register (5 bits): Indicates the destination register for storing results or address computations.
*	Immediate Value (12 bits): Represents an immediate value used in the operation (e.g., constant, offset).

I-type instructions in RISC-V primarily handle immediate values and memory operations. They include operations such as loading/storing data from/to memory, arithmetic operations with immediate values, and branching based on immediate conditions. I-type instructions are crucial for manipulating data and controlling program flow in RISC-V processors.

#### S INSTRUCTION TYPE
![image](https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/b0eef1d0-214f-4e01-afb4-32cfca5b41a1)
* opcode: The opcode field specifies the operation to be performed, which in this case is 01000.
* imm[11:5]: These bits are part of the immediate value.
* rs2: This field specifies the register operand 2, or the source register.
* rs1: This field specifies the register operand 1, or the base register.
* funct3: This field is used to specify additional bits that help define the operation of the instruction.
* Imm[4:0]: These bits are part of the immediate value.

S-type instructions enable efficient data transfer between registers and memory. These instructions facilitate storing data from a register to memory, with an immediate offset specified within the instruction. S-type instructions play a vital role in memory management and data manipulation tasks in RISC-V architectures.

#### B INSTRUCTION TYPE
![image](https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/cba0bb7c-0519-4044-aedb-9483c56681b1)
* opcode: The opcode field specifies the operation to be performed. In the case of the B instruction, the opcode is 01101.
* imm[11]: This bit is used to extend the immediate value.
* imm[4:1]: These bits are part of the immediate value.
* rs1: This field specifies the register operand 1.
* rs2: This field specifies the register operand 2.
* funct3: This field is used to specify additional bits that help define the operation of the instruction.
* Imm[11:5]: These bits are part of the immediate value

Branch instructions, categorized as B-type instructions, are essential for implementing conditional and unconditional branches in RISC-V programs. These instructions enable control flow modifications based on various conditions, allowing for the execution of loops, conditional statements, and function calls. B-type instructions contribute to the flexibility and versatility of RISC-V software implementations.

#### U INSTRUCTION TYPE
![image](https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/5d63d001-fdf1-49e0-aa1d-6ead6b039bd5)
* opcode: The opcode field specifies the operation to be performed, which in this case is 00100.
* rd: This field specifies the destination register.
* imm[31:12]: These bits are part of the immediate value.

RISC-V U-type instructions, also known as upper immediate instructions, provide a mechanism for encoding larger immediate values within the instruction itself. These instructions are primarily used for initializing large constants or memory addresses during program execution. U-type instructions enhance the expressiveness and flexibility of RISC-V code by enabling direct representation of extended immediate values.

#### J INSTRUCTION
![image](https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/fbb7ccfa-26f4-49e1-9048-e81bbd6443f7)
* opcode: The opcode field specifies the operation to be performed, which in this case is 11011.
* imm[20]: This bit is used to extend the immediate value.
* imm[10:1]: These bits are part of the immediate value.
* imm[11]: This bit is used to extend the immediate value.
* imm[19:12]: These bits are part of the immediate value.
  
J-type instructions, also referred to as jump instructions, facilitate unconditional jumps or subroutine calls within RISC-V programs. These instructions enable efficient branching to target addresses specified within the instruction, allowing for the implementation of function calls, exception handling, and other control flow mechanisms. J-type instructions play a crucial role in program control and organization in RISC-V architectures.

### RISC-V INSTRUCTION SET OPERATION EXAMPLE
#### ADD r6,r2,r1 (R)
Addition operation by R-type instruction format, r6 is the destination register that will hold the sum of values stored in registers r2 and r1.r6 = 00110, r2 = 00010,r1 = 00100,func3 = 000,func7 = 0000000,Opcode for ADD = 0110011:<br>
32-bit instruction: 0000000_00100_00010_000_00110_01100111
#### SUB r7,r1,r2 (R)
Subtraction operation are performed using the R-type instruction format; hence, this instruction belongs to the R-type instruction set.
r7 is the destination register that will hold the result of subtracting the value stored in register r2 from the value stored in register r1.
r7 = 00111,r1 = 00100,r2 = 00010,func3 = 000,func7 = 0100000,Opcode for SUB = 0110011,<br>
32-bit instruction: 0100000_00010_00100_000_00111_0110011
#### AND r8, r1,r3 (R)
All arithmetic and logical operations are performed using the R-type instruction format; hence, this instruction belongs to the R-type instruction set.r8 is the destination register that will hold the result of bitwise AND operation between the values stored in registers r1 and r3.
rd = r8 = 01000, rs1 = r1 = 00110, rs2 = r3 = 01100, func3 = 111, func7 = 0000000, Opcode for AND = 0110011<br>
32-bit instruction: 0000000_01100_00110_111_01000_0110011
#### OR r9, r2, r5 (R) 
All arithmetic and logical operations are performed using the R-type instruction format; hence, this instruction belongs to the R-type instruction set.r9 is the destination register that will hold the result of bitwise OR operation between the values stored in registers r2 and r5.
rd = r9 = 01001, rs1 = r2 = 00010, rs2 = r5 = 01110, func3 = 110, func7 = 0000000, Opcode for OR = 0110011<br>
32-bit instruction: 0000000_01110_00010_110_01001_0110011
#### XOR r10, r2, r5 (R) 
All arithmetic and logical operations are performed using the R-type instruction format; hence, this instruction belongs to the R-type instruction set.
r10 is the destination register that will hold the result of bitwise XOR operation between the values stored in registers r2 and r5.
Opcode for XOR = 0110011, rd = r10 = 01010, r2 = 00010, r5 = 01110, func3 = 100, func7 = 0000000<br>
32-bit instruction: 0000000_01110_00010_100_01010_0110011
#### SLT r11, r2, r4 (R) 
All arithmetic and logical operations are performed using the R-type instruction format; hence, this instruction belongs to the R-type instruction set.
r11 is the destination register that will hold the result of the comparison between the values stored in registers r2 and r4.
Opcode for SLT = 0110011, r11 = 01011, r2 = 00010, r4 = 00100, func3 = 010, func7 = 0000000<br>
32-bit instruction: 0000000_00100_00010_010_01011_0110011
#### ADDI r12, r4, 5 (I)
The ADDI operation adds an immediate value (10 in this case) to the value stored in register r4, and stores the result in register r12.
Opcode for ADDI = 0010011,  r12 = 01100,  r4 = 00010, Immediate Value = 5 (encoded as 000000000010 in binary, 5 in decimal)<br>
32-bit instruction: 000000000010_00010_01100_0010011
#### SW r3, r1, 2 
This instruction stores the value in register r3 to the memory address computed by adding the immediate offset 2 to the value in register r1.
Opcode for SW = 0100011,  r1 = 00001,  r3 = 00011, Immediate Offset = 2, func3 = 010<br>
32-bit instruction: 0000000_00011_00001_010_00010_0100011
#### LW r13, r1, 2 
This instruction loads the value from memory at the address computed by adding the immediate offset 2 to the value in register r1 and stores it in register r13.
Opcode for LW = 0000011,  r13 = 01101, r1 = 00001, Immediate Offset = 2, func3 = 010<br>
32-bit instruction: 0000000_00001_01101_010_00010_0000011
#### BEQ r0,r0,r15 
BEQ r0, r0, r15  
This instruction branches to the address specified by the value in register r15 if the values in registers r0 and r0 (which are always zero) are equal.
Opcode for BEQ = 1100011,  r0 = 00000, r0 = 00000, Offset = Address of r15 - Address of the next instruction ,func3 = 000<br>
32-bit instruction: <offset>_00000_00000_000_11000_1100011
#### SLL r15,r1,r2(2) 
This instruction performs a logical left shift on the value in register r1 by the amount specified in register r2 (shift amount 2) and stores the result in register r15.
Opcode for SLL = 0111011,  r15 = 01111, r1 = 00001 ,  r2 = 00010,func3 = 001 (corresponding to shift left logical), func7 = 0000000 <br>
32-bit instruction: 0000000_00010_00001_001_01111_0111011
#### SRL r16,r14,r2(2) 
This instruction performs a logical right shift on the value in register r14 by the amount specified in register r2 (shift amount 2) and stores the result in register r16.
Opcode for SRL = 0111011, r16 = 10000, r14 = 01110,  r2 = 00010, func3 = 101 (corresponding to shift right logical), func7 = 0000000<br>
32-bit instruction: 0000000_00010_01110_101_10000_0111011

## WEEK 03
### Compilation of C Program using RISCV Compiler
#### Writing C Program
Use Leafpad Editor to write C-program<br>
<img src="https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/06d7918c-9526-4f27-8f55-e918ff78d1d1" width="700" height="500"><br>
#### Compilation and Execution
Compile and run the program using gcc program_name.c<br>
./a.out<br>
Compile the above program using RISCV GCC compiler by following above instruction<br>
$ riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o program_name.o program_name.c<br>
<img src="https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/8b71437b-1ebc-43e7-9734-4df57d57d915" width="700" height="500"><br>
Now in new terminal we have to open assembly code to verify out result
$ riscv64-unknown-elf-objdump -d program_name.o 
<img src="https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/6f9a9693-16c1-4b15-97a4-0b33dab0def5" width ="700" height="500"><br>
As we are looking for assembly code related to procedural block "main"<br>
$ riscv64-unknown-elf-objdump -d program_name.o | less<br>
: /main<br>
<img src="https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/59cf94dd-40db-4198-a35a-8b42a1f6ff41" width="700" height="500"><br>

## WEEK 04
### RISC V COMPILATION
#### Compiling C program using riscv compiler
to compile and run program using riscv compiler<br>
code to be used "spike pk sum1ton.o"<br>
<img src ="https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/3227b00b-24d8-429d-8952-a4af41127e63" width="700" height="500"><br>
Assembly language code for respective main procedural block<br>
<img src ="https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/e4b9337f-7244-4241-b95c-3f32885853a8" width="700" height="500"><br>
#### Clarifying Data generated by RISCV Compiler
By entering "until pc 0 10158", we can get data present in register a2 with series on pressing enter key RISCV command will get final output which is<br>
having similar data present during C program compilation.<br>
<img src = "https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/dbb57488-24af-45d8-aed7-3060303e14f8" width="700" height="500"><br>




















