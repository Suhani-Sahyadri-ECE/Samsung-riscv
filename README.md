# RISC-V Talent Development Program Powered by SAMSUNG along with VLSI System Design (VSD)
This is a VSD Squadron-Mini Internship Program which explores the RISC-V processor architecture and 
deeply learn about VLSI Design using the open source tools.The instructor and guide for this 
internship program is Mr.Kunal Ghosh,Co-Founder of VSD. 

# BASIC DETAILS

## Name:Suhani D
## College:Sahyadri College Of Engineering And Management,Adyar,Mangaluru.
## Email ID:dsuhani2004@gmail.com or suhani.ec22@sahyadri.edu.in
## Linkedin:Suhani D
<details>
<summary># Task 1 :Installation of RISC-V toolchain using VDI link
## Installation of leafpad
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/014b68a93b6f9afcb197c9db4b31f95b56f6532f/TASK1/leafpad%20install.png)
## Terminal of c
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/014b68a93b6f9afcb197c9db4b31f95b56f6532f/TASK1/terminal%20of%20cbased.png)
## Output of c terminal
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/014b68a93b6f9afcb197c9db4b31f95b56f6532f/TASK1/output%20of%20c.png)
## Terminal of risc
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/014b68a93b6f9afcb197c9db4b31f95b56f6532f/TASK1/riscterminal.png)
## Output of risc
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/014b68a93b6f9afcb197c9db4b31f95b56f6532f/TASK1/risc.png)
  </summary>
</details>
# Task 2 :Simulation of SPIKE
## Evenodd code
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/d978fa8c89f40b4273210b89d0750476d2bb41a5/Task2/evenodd%20code.png)
## o1 of evenodd code
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/d978fa8c89f40b4273210b89d0750476d2bb41a5/Task2/o1%20even.o.png)
## object dump of o1 evenodd code
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/d978fa8c89f40b4273210b89d0750476d2bb41a5/Task2/objdump%20o1.png)
## object dump of ofast evenodd code
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/d978fa8c89f40b4273210b89d0750476d2bb41a5/Task2/objdump%20ofast.png)
## ofast of evenodd code
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/d978fa8c89f40b4273210b89d0750476d2bb41a5/Task2/ofast%20even.o.png)
## spike simulation review
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/d978fa8c89f40b4273210b89d0750476d2bb41a5/Task2/spike%20sim%20review.png)
## spike simulation
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/d978fa8c89f40b4273210b89d0750476d2bb41a5/Task2/spikesim.png)

# Task 3 :RISC-V Instruction types
## 15 instructions
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/20836ab0752ddd92bf859bf1d96791e5ebc5c93a/Task3/ofast%20obj.png)
# 15 RISC-V Instructions Breakdown
## **1. lui a0, 0x2B**  
*Opcode (U-Type):* 0110111  
*Registers:* rd = a0 (00101)  
*Immediate:* 0x2B (0000000000101011)  

| imm[31:12]  | rd (a0) | opcode  |
|-------------|---------|---------|
| 0000000000101011 | 00101 | 0110111 |

---

## **2. addi sp, sp, -32**  
*Opcode (I-Type):* 0010011  
*Registers:* rs1 = sp (00010), rd = sp (00010)  
*Immediate:* -32 (1111111110000000)  

| imm[11:0] | rs1 (sp) | funct3 | rd (sp) | opcode  |
|-----------|-----------|--------|---------|---------|
| 1111111110000000 | 00010 | 000 | 00010 | 0010011 |

---

## **3. addi a0, a0, -976**  
*Opcode (I-Type):* 0010011  
*Registers:* rs1 = a0 (00101), rd = a0 (00101)  
*Immediate:* -976 (1111111111101000)  

| imm[11:0] | rs1 (a0) | funct3 | rd (a0) | opcode  |
|-----------|-----------|--------|---------|---------|
| 1111111111101000 | 00101 | 000 | 00101 | 0010011 |

---

## **4. sd ra, 24(sp)**  
*Opcode (S-Type):* 0100111  
*Registers:* rs1 = sp (00010), rs2 = ra (00001)  
*Immediate:* 24 (split as imm[11:5] = 0000000, imm[4:0] = 11000)  

| imm[11:5] | rs2 (ra) | rs1 (sp) | funct3 | imm[4:0] | opcode  |
|-----------|-----------|-----------|--------|---------|---------|
| 0000000 | 00001 | 00010 | 011 | 11000 | 0100111 |

---

## **5. jal ra, 10438**  
*Opcode (J-Type):* 1101111  
*Registers:* rd = ra (00001)  
*Immediate:* 10438 (split as imm[20] = 0, imm[19:12] = 00101001, imm[11] = 0, imm[10:1] = 0101001110)  

| imm[20] | imm[10:1] | imm[11] | imm[19:12] | rd (ra) | opcode  |
|---------|-----------|--------|-----------|---------|---------|
| 0 | 0101001110 | 0 | 00101001 | 00001 | 1101111 |

---

## **6. lui a0, 0x2B**  
*Opcode (U-Type):* 0110111  
*Registers:* rd = a0 (00101)  
*Immediate:* 0x2B (0000000000101011)  

| imm[31:12]  | rd (a0) | opcode  |
|-------------|---------|---------|
| 0000000000101011 | 00101 | 0110111 |

---

## **7. addi a1, sp, 12**  
*Opcode (I-Type):* 0010011  
*Registers:* rs1 = sp (00010), rd = a1 (00110)  
*Immediate:* 12 (0000000001100)  

| imm[11:0] | rs1 (sp) | funct3 | rd (a1) | opcode  |
|-----------|-----------|--------|---------|---------|
| 0000000001100 | 00010 | 000 | 00110 | 0010011 |

---

## **8. lw a1, 12(sp)**  
*Opcode (I-Type):* 0000011  
*Registers:* rs1 = sp (00010), rd = a1 (00110)  
*Immediate:* 12 (0000000001100)  

| imm[11:0] | rs1 (sp) | funct3 | rd (a1) | opcode  |
|-----------|-----------|--------|---------|---------|
| 0000000001100 | 00010 | 010 | 00110 | 0000011 |

---

## **9. andi a5, a1, 1**  
*Opcode (I-Type):* 0010011  
*Registers:* rs1 = a1 (00110), rd = a5 (01101)  
*Immediate:* 1 (0000000000001)  

| imm[11:0] | rs1 (a1) | funct3 | rd (a5) | opcode  |
|-----------|-----------|--------|---------|---------|
| 0000000000001 | 00110 | 111 | 01101 | 0010011 |

---

## **10. bnez a5, 0x100fc**  
*Opcode (B-Type):* 1100011  
*Registers:* rs1 = a5 (01101), rs2 = zero (00000)  
*Immediate:* 0x100fc (split as imm[12] = 1, imm[10:5] = 000100, imm[4:1] = 1111, imm[0] = 0)  

| imm[12] | imm[10:5] | imm[4:1] | imm[0] | rs2 (zero) | rs1 (a5) | funct3 | opcode  |
|---------|-----------|----------|--------|------------|-----------|--------|---------|
| 1 | 000100 | 1111 | 0 | 00000 | 01101 | 001 | 1100011 |

---

## **11. li a0, 0**  
*Opcode (I-Type):* 0010011  
*Registers:* rs1 = zero (00000), rd = a0 (00101)  
*Immediate:* 0 (0000000000000)  

| imm[11:0] | rs1 (zero) | funct3 | rd (a0) | opcode  |
|-----------|-----------|--------|---------|---------|
| 0000000000000 | 00000 | 000 | 00101 | 0010011 |

---

## **12. j 0x100ec**  
*Opcode (J-Type):* 1101111  
*Registers:* rd = zero (00000)  
*Immediate:* 0x100ec (split as imm[20] = 0, imm[19:12] = 00010000, imm[11] = 0, imm[10:1] = 0001111100)  

| imm[20] | imm[10:1] | imm[11] | imm[19:12] | rd (zero) | opcode  |
|---------|-----------|--------|-----------|-----------|---------|
| 0 | 0001111100 | 0 | 00010000 | 00000 | 1101111 |

---

## **13. auipc a5, 0xFFFF0**  
*Opcode (U-Type):* 0010111  
*Registers:* rd = a5 (01111)  
*Immediate:* 0xFFFF0 (1111111111110000)  

| imm[31:12] | rd (a5) | opcode  |
|------------|---------|---------|
| 1111111111110000 | 01111 | 0010111 |

---

## **14. addi a5, a5, -268**  
*Opcode (I-Type):* 0010011  
*Registers:* rs1 = a5 (01111), rd = a5 (01111)  
*Immediate:* -268 (1111111111010100)  

| imm[11:0] | rs1 (a5) | funct3 | rd (a5) | opcode  |
|-----------|-----------|--------|---------|---------|
| 1111111111010100 | 01111 | 000 | 01111 | 0010011 |

---

## **15. beqz a5, 0x10124**  
*Opcode (B-Type):* 1100011  
*Registers:* rs1 = a5 (01111), rs2 = zero (00000)  
*Immediate:* 0x10124 (split as imm[12] = 0, imm[10:5] = 000101, imm[4:1] = 0010, imm[0] = 0)  

| imm[12] | imm[10:5] | imm[4:1] | imm[0] | rs2 (zero) | rs1 (a5) | funct3 | opcode  |
|---------|-----------|----------|--------|------------|-----------|--------|---------|
| 0 | 000101 | 0010 | 0 | 00000 | 01111 | 000 | 1100011 |

---
# Task 4 :Functional simulation of RISC-V core verilog and netlist
## Steps:
## > Download the gtkwave and iverilog using commands
![img alt](https://github.com/user-attachments/assets/23fa7154-26a8-4e91-9772-d8a6309df545)
![img alt](https://github.com/user-attachments/assets/f7348491-9795-421b-8432-4bcb71b972f4)
## > Copy the code from the reference github repo and paste it in your verilog and testbench files.
## > To run and simulate the verilog code, enter the following command in the terminal:
![img alt](https://github.com/user-attachments/assets/a31b84d3-11fd-4e50-802a-b6229c48a7e4)
![img alt](https://github.com/user-attachments/assets/46acad70-81c1-4d9b-98cb-6262b95681c8)
## >To see the simulation waveform in GTKWave, enter the following command:
![img alt](https://github.com/user-attachments/assets/6c4dd9c0-21dc-43f1-a9d7-16c3d7831fea)
## >The output waveform 
### Instruction 1:add r6,r2,r1
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/184f770b31201eee0599171d614c1a23fdb62835/Task4/ADD.png)
### Instruction 2:addi r12,r4,r5
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/184f770b31201eee0599171d614c1a23fdb62835/Task4/ADDI.png)
### Instruction 3:and r8,r1,r3
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/184f770b31201eee0599171d614c1a23fdb62835/Task4/and.png)
### Instruction 4:beq r0,r0,r15
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/184f770b31201eee0599171d614c1a23fdb62835/Task4/beq.png)
### Instruction 5:or r9,r2,r5
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/184f770b31201eee0599171d614c1a23fdb62835/Task4/or.png)
### Instruction 6:slt r11,r2,r4
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/184f770b31201eee0599171d614c1a23fdb62835/Task4/slt.png)
### Instruction 7:sub r7,r1,r2
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/184f770b31201eee0599171d614c1a23fdb62835/Task4/sub1.png)
### Instruction 8:xor r10,r1,r4
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/184f770b31201eee0599171d614c1a23fdb62835/Task4/xor.png)
### Waveforms
![img alt](https://github.com/Suhani-Sahyadri-ECE/Samsung-riscv/blob/218abe45cc6926d0329954755b5181b96cf24122/Task4/waveforms.png)








