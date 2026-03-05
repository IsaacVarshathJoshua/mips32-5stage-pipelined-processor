# 5-Stage Pipelined MIPS32 Processor (Verilog)

This project implements a **5-stage pipelined RISC processor** similar to the MIPS32 architecture using **Verilog HDL**.  
The processor is designed using **RTL design principles** and simulated to demonstrate instruction execution through pipeline stages.

---

## Architecture Overview

The processor follows a classic **5-stage pipeline architecture**:

1. **IF – Instruction Fetch**
2. **ID – Instruction Decode**
3. **EX – Execute**
4. **MEM – Memory Access**
5. **WB – Write Back**

Each stage is separated by **pipeline registers**:

- IF/ID
- ID/EX
- EX/MEM
- MEM/WB

This allows multiple instructions to be processed simultaneously in different pipeline stages.

---

## Pipeline Stages

### 1. Instruction Fetch (IF)
- Fetch instruction from instruction memory
- Update Program Counter (PC)
- Store instruction in IF/ID register

### 2. Instruction Decode (ID)
- Decode instruction fields
- Read operands from register file
- Perform sign extension for immediate values

### 3. Execute (EX)
- Perform ALU operations
- Compute arithmetic and logical results
- Evaluate branch conditions

### 4. Memory Access (MEM)
- Perform load/store operations
- Access data memory

### 5. Write Back (WB)
- Write results back to register file

---

## Supported Instructions

The processor currently supports the following operations:

- ADD
- SUB
- AND
- OR
- SLT
- MUL
- BEQZ
- BNEQZ

These instructions demonstrate arithmetic, logical, and branch operations.

---

## Project Structure

mips32-5stage-pipelined-processor
│
├── rtl
│   ├── mips32_top.v
│   ├── if_stage.v
│   ├── id_stage.v
│   ├── ex_stage.v
│   ├── mem_stage.v
│   └── wb_stage.v
│
├── testbench
│   └── mips32_tb.v
│
├── docs
│   └── pipeline_diagram.png
│
└── README.md


---

## Tools Used

- **Verilog HDL**
- **ModelSim / Vivado Simulator**
- **RTL Simulation**

---

## Key Concepts Demonstrated

- RTL Design
- Processor Architecture
- Pipeline Registers
- Branch Handling
- ALU Design
- Verilog Hardware Modeling

---

## Future Improvements

- Implement hazard detection
- Add data forwarding
- Expand instruction set
- Improve testbench coverage

---

## Author

J Isaac Varshath Joshua  
VIT Vellore
Electronics and Communication Engineering

