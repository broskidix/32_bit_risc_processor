# 32_bit_Risc_processor
In this project I have a design a 32 bit risc processor based on harvard architecture . i have write Verilog code for the this processor and simulate it on vivado.

In the Verilog code there is many modules,

     (1)	ALU
     
     (2)	ALU control
     
     (3)	Instruction memory
     
     (4)	Data memory 
     
     (5)	Register file
     
     (6)	Data path
     
     (7)	Risc processor
     
     (8)	Risc processor control unit.
     
     (9)   testbench
     
# Instruction set -

In this processor there is 3 types of instructions are designed.

(1)	Memory access instruction

(2)	Data processing instruction

(3)	Control flow instruction



# Memory access instruction –

1. Load Word:
   
               LD ws, offset(rs1) ws:=Mem16[rs1 + offset]

2. Store Word:
   
               ST rs2, offset(rs1) Mem16[rs1 + offset]=rs2
   
# Data processing instruction –

1. Add:
 
              ADD  ws, rs1, rs2       ws:=rs1 + rs2
   
2. Subtract:
   
               SUB ws, rs1, rs2    ws:=rs1 – rs2
   
 3. Invert (1‘s complement):
  
               INV ws, rs1 ws:=!rs1
    
4. Logical Shift Left:
 
               LSL ws, rs1, rs2 ws:=rs1 << rs2
   
5. Logical Shift Right:
 
               LSR ws, rs1, rs2 ws:=rs1 >> rs2
    
6. Bitwise AND:
 
               AND ws, rs1, rs2 ws:=rs1 • rs2
    
7. Bitwise OR:
 
              OR ws, rs1, rs2 ws:=rs1 | rs2
    
8. Set on Less Than:
 
             SLT ws, rs1, rs2 ws:=1 if rs1 < rs2; ws:=0 if rs1 ≥ rs2
    
# Control flow instruction –

1. Branch on Equal:
 
           BEQ rs1, rs2, offset
   
           Branch to (PC + 2 + (offset << 1)) when rs1 = rs2
   
2. Branch on Not Equal:
   
           BNE rs1, rs2, offset
   
           Branch to (PC + 2 + (offset << 1)) when rs1 != rs2
   
3. Jump:

          JMP offset Jump to {PC [31:27], (offset << 1)}

# Instruction format-
![](https://github.com/broskidix/32_bit_risc_processor/blob/main/Screenshot%202024-09-02%20at%2015.56.01.png)



# processor control design -
![](https://github.com/broskidix/32_bit_risc_processor/blob/main/Screenshot%202024-09-02%20at%2015.55.10.png)

# ALU control design -
![](https://github.com/broskidix/32_bit_risc_processor/blob/main/Screenshot%202024-09-02%20at%2015.54.56.png)

