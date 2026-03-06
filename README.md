# 5-Stage Pipelined MIPS32 Processor (Verilog)

This project implements a **5-stage pipelined RISC processor** inspired by the **MIPS32 architecture** using **Verilog HDL**.  
The processor demonstrates **instruction pipelining, ALU operations, and branch execution** through RTL design and simulation.

The design follows the classical **MIPS pipeline architecture** and is simulated using **ModelSim / Vivado**.

---

# Architecture Overview

The processor uses a **5-stage pipeline** to improve instruction throughput.

1. **IF – Instruction Fetch**
2. **ID – Instruction Decode**
3. **EX – Execute**
4. **MEM – Memory Access**
5. **WB – Write Back**

Each stage communicates through **pipeline registers**:

- IF/ID
- ID/EX
- EX/MEM
- MEM/WB

This allows **multiple instructions to execute simultaneously** in different pipeline stages.

---

# Pipeline Stages

## Instruction Fetch (IF)
- Fetch instruction from memory
- Update the Program Counter (PC)
- Store instruction in the IF/ID pipeline register

## Instruction Decode (ID)
- Decode instruction opcode
- Read operands from the register file
- Perform **sign extension** for immediate values

## Execute (EX)
- Perform ALU operations
- Execute arithmetic and logical instructions
- Evaluate branch conditions

## Memory Access (MEM)
- Perform **load/store operations**
- Access data memory

## Write Back (WB)
- Write computed results back to the register file

---

# Supported Instructions

### Arithmetic Instructions
- ADD
- SUB
- MUL

### Logical Instructions
- AND
- OR
- SLT

### Immediate Instructions
- ADDI
- SUBI
- SLTI

### Memory Instructions
- LW
- SW

### Branch Instructions
- BEQZ
- BNEQZ

### Control Instruction
- HLT

---

# Project Structure

mips32-pipelined-processor
│
├── pipe_MIPS32.v # Main processor RTL implementation
├── test_mips32.sv # Testbench for simulation
├── README.md
└── LICENSE


---

# Simulation

The processor can be simulated using **ModelSim or Vivado**.

### Compile

vlog pipe_MIPS32.v
vlog test_mips32.sv


### Run Simulation

vsim test_mips32
run -all


Waveforms can be viewed using **VCD dump files**.

---

# Key Concepts Demonstrated

- RTL Processor Design
- 5-Stage Instruction Pipeline
- Pipeline Registers
- Branch Handling
- ALU Design
- Verilog Hardware Modeling
- Simulation and Verification

---

# Future Improvements

- Hazard detection unit
- Data forwarding
- Pipeline stall control
- Expanded instruction set
- Improved verification coverage

---

# Author

**J Isaac Varshath Joshua**  
Electronics and Communication Engineering  
VIT Vellore
