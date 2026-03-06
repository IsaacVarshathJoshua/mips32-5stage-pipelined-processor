# Simulation Results

This section shows the simulation results of the 5-stage pipelined MIPS32 processor.

## Test Program

The processor executes the following instructions:

1. ADDI R1, R0, 10
2. ADDI R2, R0, 20
3. ADDI R3, R0, 25
4. ADD R4, R1, R2
5. ADD R5, R4, R3
6. HLT

## Expected Register Values

| Register | Value |
|--------|--------|
| R1 | 10 |
| R2 | 20 |
| R3 | 25 |
| R4 | 30 |
| R5 | 55 |

## Pipeline Execution

The instructions move through the following pipeline stages:

IF → ID → EX → MEM → WB

Multiple instructions execute simultaneously across pipeline stages.

## Simulation Output

Example output from the simulator:

R0 - 0
R1 - 10
R2 - 20
R3 - 25
R4 - 30
R5 - 55


## Waveform

Simulation waveform showing pipeline operation:

![Waveform](simulation_waveform.png)
