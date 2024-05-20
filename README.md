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

## WEEK 05

### Writing Verilog code and Testbench Code to check Functionality

 #### Verilog Code

 ```
module iiitb_rv32i(clk,RN,NPC,WB_OUT);
input clk;
input RN;
//input EN;
integer k;
wire  EX_MEM_COND ;

reg 
BR_EN;

//I_FETCH STAGE
reg[31:0] 
IF_ID_IR,
IF_ID_NPC;                                

//I_DECODE STAGE
reg[31:0] 
ID_EX_A,
ID_EX_B,
ID_EX_RD,
ID_EX_IMMEDIATE,
ID_EX_IR,ID_EX_NPC;      

//EXECUTION STAGE
reg[31:0] 
EX_MEM_ALUOUT,
EX_MEM_B,EX_MEM_IR;                        

parameter 
ADD=3'd0,
SUB=3'd1,
AND=3'd2,
OR=3'd3,
XOR=3'd4,
SLT=3'd5,

ADDI=3'd0,
SUBI=3'd1,
ANDI=3'd2,
ORI=3'd3,
XORI=3'd4,

LW=3'd0,
SW=3'd1,

BEQ=3'd0,
BNE=3'd1,

SLL=3'd0,
SRL=3'd1;


parameter 
AR_TYPE=7'd0,
M_TYPE=7'd1,
BR_TYPE=7'd2,
SH_TYPE=7'd3;


//MEMORY STAGE
reg[31:0] 
MEM_WB_IR,
MEM_WB_ALUOUT,
MEM_WB_LDM;                      


output reg [31:0]WB_OUT,NPC;

//REG FILE
reg [31:0]REG[0:31];                                               
//64*32 IMEM
reg [31:0]MEM[0:31];                                             
//64*32 DMEM
reg [31:0]DM[0:31];   


//assign EX_MEM_COND = (EX_MEM_IR[6:0]==BR_TYPE) ? 1'b1 : 1'b0;
                     //1'b1 ? (ID_EX_A!=ID_EX_RD) : 1'b0;

always @(posedge clk or posedge RN) begin
    if(RN) begin
    NPC<= 32'd0;
    //EX_MEM_COND <=1'd0;
    BR_EN<= 1'd0; 
    REG[0] <= 32'h00000000;
    REG[1] <= 32'd1;
    REG[2] <= 32'd2;
    REG[3] <= 32'd3;
    REG[4] <= 32'd4;
    REG[5] <= 32'd5;
    REG[6] <= 32'd6;
    end
    //else if(EX_MEM_COND)
    //NPC <= EX_MEM_ALUOUT;

    //else if (EX_MEM_COND)begin
    //NPC = EX_MEM_COND ? EX_MEM_ALUOUT : NPC +32'd1;
    //NPC <= EX_MEM_ALUOUT;
    //EX_MEM_COND = BR_EN;
    //NPC = BR_EN ? EX_MEM_ALUOUT : NPC +32'd1;
    //BR_EN = 1'd0;
    //EX_MEM_COND <= 1'd0;
    //end
    else begin
    NPC <= BR_EN ? EX_MEM_ALUOUT : NPC +32'd1;
    BR_EN <= 1'd0;
    //NPC <= NPC +32'd1;
    //EX_MEM_COND <=1'd0;
    IF_ID_IR <=MEM[NPC];
    IF_ID_NPC <=NPC+32'd1;
    end
end

always @(posedge RN) begin
    //NPC<= 32'd0;
MEM[0] <= 32'h02208300;         // add r6,r1,r2.(i1)
MEM[1] <= 32'h02209380;         //sub r7,r1,r2.(i2)
MEM[2] <= 32'h0230a400;         //and r8,r1,r3.(i3)
MEM[3] <= 32'h02513480;         //or r9,r2,r5.(i4)
MEM[4] <= 32'h0240c500;         //xor r10,r1,r4.(i5)
MEM[5] <= 32'h02415580;         //slt r11,r2,r4.(i6)
MEM[6] <= 32'h00520600;         //addi r12,r4,5.(i7)
MEM[7] <= 32'h00209181;         //sw r3,r1,2.(i8)
MEM[8] <= 32'h00208681;         //lw r13,r1,2.(i9)
MEM[9] <= 32'h00f00002;         //beq r0,r0,15.(i10)
MEM[25] <= 32'h00210700;         //add r14,r2,r2.(i11)
//MEM[27] <= 32'h01409002;         //bne r0,r1,20.(i12)
//MEM[49] <= 32'h00520601;         //addi r12,r4,5.(i13)
//MEM[50] <= 32'h00208783;         //sll r15,r1,r2(2).(i14)
//MEM[51] <= 32'h00271803;         //srl r16,r14,r2(2).(i15) */

//for(k=0;k<=31;k++)
//REG[k]<=k;
/*REG[0] <= 32'h00000000;
REG[1] <= 32'd1;
REG[2] <= 32'd2;
REG[3] <= 32'd3;
REG[4] <= 32'd4;
REG[5] <= 32'd5;
REG[6] <= 32'd6;
REG[7] = 32'd7;
REG[6] = 32'd6;
REG[7] = 32'd7;
REG[8] = 32'd8;
REG[9] = 32'd9;
REG[10] = 32'd10;
REG[11] = 32'd11;
REG[12] = 32'd12;
REG[13] = 32'd13;
REG[14] = 32'd14;
REG[15] = 32'd15;
REG[16] = 32'd16;
REG[17] = 32'd17;*/
/*end
else begin
    if(EX_MEM_COND==1 && EX_MEM_IR[6:0]==BR_TYPE) begin
    NPC=EX_MEM_ALUOUT;
    IF_ID=MEM[NPC];
    end

    else begin
    NPC<=NPC+32'd1;
    IF_ID<=MEM[NPC];
    IF_ID_NPC<=NPC+32'd1;
    end
end*/
end
//I_FECT STAGE

/*always @(posedge clk) begin

//NPC <= rst ? 32'd0 : NPC+32'd1;

if(EX_MEM_COND==1 && EX_MEM_IR[6:0]==BR_TYPE) begin
NPC=EX_MEM_ALUOUT;
IF_ID=MEM[NPC];
end

else begin
NPC<=NPC+32'd1;
IF_ID<=MEM[NPC];
IF_ID_NPC<=NPC+32'd1;
end
end*/


//FETCH STAGE END

//I_DECODE STAGE 
always @(posedge clk) begin

ID_EX_A <= REG[IF_ID_IR[19:15]];
ID_EX_B <= REG[IF_ID_IR[24:20]];
ID_EX_RD <= REG[IF_ID_IR[11:7]];
ID_EX_IR <= IF_ID_IR;
ID_EX_IMMEDIATE <= {{20{IF_ID_IR[31]}},IF_ID_IR[31:20]};
ID_EX_NPC<=IF_ID_NPC;
end
//DECODE STAGE END

/*always@(posedge clk) begin
if(ID_EX_IR[6:0]== BR_TYPE)
EX_MEM_COND <= EN;
else
EX_MEM_COND <= !EN;
end*/


//EXECUTION STAGE

always@(posedge clk) begin

EX_MEM_IR <=  ID_EX_IR;
//EX_MEM_COND <= (ID_EX_IR[6:0] == BR_TYPE) ? 1'd1 :1'd0;


case(ID_EX_IR[6:0])

AR_TYPE:begin
    if(ID_EX_IR[31:25]== 7'd1)begin
    case(ID_EX_IR[14:12])

    ADD:EX_MEM_ALUOUT <= ID_EX_A + ID_EX_B;
    SUB:EX_MEM_ALUOUT <= ID_EX_A - ID_EX_B;
    AND:EX_MEM_ALUOUT <= ID_EX_A & ID_EX_B;
    OR :EX_MEM_ALUOUT <= ID_EX_A | ID_EX_B;
    XOR:EX_MEM_ALUOUT <= ID_EX_A ^ ID_EX_B;
    SLT:EX_MEM_ALUOUT <= (ID_EX_A < ID_EX_B) ? 32'd1 : 32'd0;

    endcase
    end
    else begin
        case(ID_EX_IR[14:12])
        ADDI:EX_MEM_ALUOUT <= ID_EX_A + ID_EX_IMMEDIATE;
        SUBI:EX_MEM_ALUOUT <= ID_EX_A - ID_EX_IMMEDIATE;
        ANDI:EX_MEM_ALUOUT <= ID_EX_A & ID_EX_B;
        ORI:EX_MEM_ALUOUT  <= ID_EX_A | ID_EX_B;
        XORI:EX_MEM_ALUOUT <= ID_EX_A ^ ID_EX_B;
        endcase
    end

end

M_TYPE:begin
    case(ID_EX_IR[14:12])
    LW  :EX_MEM_ALUOUT <= ID_EX_A + ID_EX_IMMEDIATE;
    SW  :EX_MEM_ALUOUT <= ID_EX_IR[24:20] + ID_EX_IR[19:15];
    endcase
end

BR_TYPE:begin
    case(ID_EX_IR[14:12])
    BEQ:begin 
    EX_MEM_ALUOUT <= ID_EX_NPC+ID_EX_IMMEDIATE;
    BR_EN <= 1'd1 ? (ID_EX_IR[19:15] == ID_EX_IR[11:7]) : 1'd0;
    //BR_PC = EX_MEM_COND ? EX_MEM_ALUOUT : 1'd0; 
end
BNE:begin 
    EX_MEM_ALUOUT <= ID_EX_NPC+ID_EX_IMMEDIATE;
    BR_EN <= (ID_EX_IR[19:15] != ID_EX_IR[11:7]) ? 1'd1 : 1'd0;
end
endcase
end

SH_TYPE:begin
case(ID_EX_IR[14:12])
SLL:EX_MEM_ALUOUT <= ID_EX_A << ID_EX_B;
SRL:EX_MEM_ALUOUT <= ID_EX_A >> ID_EX_B;
endcase
end

endcase
end


//EXECUTION STAGE END
		
//MEMORY STAGE
always@(posedge clk) begin

MEM_WB_IR <= EX_MEM_IR;

case(EX_MEM_IR[6:0])

AR_TYPE:MEM_WB_ALUOUT <=  EX_MEM_ALUOUT;
SH_TYPE:MEM_WB_ALUOUT <=  EX_MEM_ALUOUT;

M_TYPE:begin
case(EX_MEM_IR[14:12])
LW:MEM_WB_LDM <= DM[EX_MEM_ALUOUT];
SW:DM[EX_MEM_ALUOUT]<=REG[EX_MEM_IR[11:7]];
endcase
end

endcase
end

// MEMORY STAGE END


//WRITE BACK STAGE
always@(posedge clk) begin

case(MEM_WB_IR[6:0])

AR_TYPE:begin 
WB_OUT<=MEM_WB_ALUOUT;
REG[MEM_WB_IR[11:7]]<=MEM_WB_ALUOUT;
end

SH_TYPE:begin
WB_OUT<=MEM_WB_ALUOUT;
REG[MEM_WB_IR[11:7]]<=MEM_WB_ALUOUT;
end

M_TYPE:begin
case(MEM_WB_IR[14:12])
LW:begin
WB_OUT<=MEM_WB_LDM;
REG[MEM_WB_IR[11:7]]<=MEM_WB_LDM;
end
endcase
end



endcase
end
//WRITE BACK STAGE END

endmodule
```

#### Testbench Code

```
module iiitb_rv32i_tb;

reg clk,RN;
wire [31:0]WB_OUT,NPC;

iiitb_rv32i rv32(clk,RN,NPC,WB_OUT);


always #3 clk=!clk;

initial begin 
RN  = 1'b1;
clk = 1'b1;

$dumpfile("iiitb_rv32i.vcd");
$dumpvars(0, iiitb_rv32i_tb.clk, iiitb_rv32i_tb.RN, iiitb_rv32i_tb.WB_OUT, iiitb_rv32i_tb.NPC,
               iiitb_rv32i_tb.rv32.ID_EX_A, iiitb_rv32i_tb.rv32.ID_EX_B,
               iiitb_rv32i_tb.rv32.ID_EX_IR, iiitb_rv32i_tb.rv32.ID_EX_RD);
  
  
  #5 RN = 1'b0;
  
  #300 $finish;

end
endmodule
```

#### Compilation of code 
As we are using Icarus Verilog, the file has to be compiled sing below code, in order to get desired waveform.
Waveform can be generated using GTK wave as shown below cmd.

```
$ iverilog -o Riscv.v Riscv_tb.v
$ vvp output Risc_wav
$ gtkwave iiitb_rv32i.vcd
```
![WhatsApp Image 2024-05-15 at 21 54 06(1)](https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/bf485520-136d-4b40-8d05-738286fe3823)

#### Instruction Set Analysis


```
add r6,r2,r1
```
![WhatsApp Image 2024-05-15 at 21 54 06(1)](https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/bf485520-136d-4b40-8d05-738286fe3823)

## WEEK 06

### Implementing Grey Code using given VSD mini Squadron RISC-V Processor 

#### Grey Code

Grey code, also known as reflected binary code, is a binary numeral system where two successive values differ in only one bit. This is often used in digital communications, coding theory, and various other <br> applications where it's important to minimize errors during transitions between consecutive values.<br>

In Grey code, each binary numeral is arranged such that adjacent values differ by only one bit. This property is useful in applications such as rotary encoders where it ensures that only one bit changes at a time as <br>the encoder moves through its positions, thus reducing the likelihood of misreadings due to noise or other errors.<br>

#### Code Implemented

```
#include <ch32v00x.h>

// Define GPIO pins for the LEDs
#define LEDS (GPIO_Pin_0 | GPIO_Pin_1 | GPIO_Pin_2 | GPIO_Pin_3)

// Gray code sequence for numbers 0 to 9
const uint8_t grayCode[10] = {0x0, 0x1, 0x3, 0x2, 0x6, 0x7, 0x5, 0x4, 0xC, 0x9};

// Function to initialize GPIO pins
void GPIO_Config(void) {
    GPIO_InitTypeDef GPIO_InitStructure;
    RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOC, ENABLE);

    // Configure LEDs on port C as output
    GPIO_InitStructure.GPIO_Pin = LEDS;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_PP;
    GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz;
    GPIO_Init(GPIOC, &GPIO_InitStructure);
}

// Simple delay function
void delay(uint32_t count) {
    while(count--) {
        __NOP(); // Do nothing (NOP instruction)
    }
}

int main(void) {
    GPIO_Config(); // Configure the GPIO

    while(1) {
        for(int i = 0; i < 10; i++) {
            // Display Gray code on LEDs
            GPIO_Write(GPIOC, (GPIO_ReadOutputData(GPIOC) & ~LEDS) | grayCode[i]);
            delay(2000000); // 2-second delay (adjust count as needed for your clock speed)
        }
    }
}
```

#### Components Required 
* VSD Mini Squadron
* 4 Resistor 220 ohm
* 4 LED
* Jumperwire

#### Circuit Diagram
![Greycode](https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/d11deee7-bc7c-49a3-9806-3c69e6e5876a)

![Untitled](https://github.com/Berlin-49/VSD_Squadron_Mini_Internship/assets/97489606/76b6258b-396c-4b20-a350-4a3202ef0468)


#### Demo video
https://drive.google.com/drive/folders/1KVjx5o0_UxJC28ukT-WPIo2IOa9Bjpne


















