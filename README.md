Design and Implementation of a Pipelined RISC-V Processor in Verilog
Overview

This project implements a modular 5-stage pipelined RISC-V processor using Verilog HDL. The processor supports arithmetic, logical, memory, and control-flow instructions. It integrates instruction fetch, decode, execute, memory, and write-back stages with pipeline registers and provides debugging support by displaying register values at each clock cycle.

Features

Based on the RISC-V instruction set architecture

5-stage pipeline (IF, ID, EX, MEM, WB)

Modular design with the following units:

IFU: Instruction Fetch Unit

IMU: Instruction Memory Unit

CU: Control Unit

ALU: Arithmetic Logic Unit

RFU: Register File Unit

Support for jump, branch, load, and store instructions

Debugging support through register state display at runtime

File Structure

TOP.v – Top-level module integrating all processor units

ALU.v – Arithmetic and logical operations

CU.v – Control unit for instruction decoding

IFU.v – Instruction fetch and program counter management

IMU.v – Instruction memory and instruction fetch logic

RFU.v – Register file handling read, write, load, and store

How It Works

Instruction Fetch (IFU + IMU)
Fetches instruction from flash memory using the program counter.

Decode (CU)
Decodes the instruction, extracts opcode, function fields, and immediate values.

Execute (ALU)
Performs arithmetic, logic, or branch operations.

Memory Access (RFU)
Handles register read/write and memory load/store operations.

Write Back (RFU)
Updates the destination register with results from ALU or memory.

Simulation

The processor is simulated using Verilog testbenches.

Instructions are loaded from flash_data.txt into flash memory.

At every clock cycle, register values are displayed for debugging.

Skills Demonstrated

Verilog HDL

Digital Logic Design

RISC-V ISA

Pipelined Processor Design

Computer Architecture Concepts
