---
layout: base
title: "Lecture 5: Registers of the Intel 8085 Microprocessor"
date: 2026-06-29 09:50:00 +0530
categories: jekyll update
permalink: "/lecture-5-registers-of-the-intel-8085-microprocessor/"
---

# {{ page.title | escape }}

## 1. What is a Register?

A register is a small, high-speed storage location inside the microprocessor. Registers temporarily store Data, Instructions, Memory addresses, Intermediate results.

### # Characteristics of Registers

- Located inside the microprocessor
- Very high speed
- Limited storage capacity
- Used for temporary storage
- Essential for instruction execution

### # Register Organization of Intel 8085

The Intel 8085 contains the following registers:

![Register Organization of Intel 8085]({{ '/assets/images/Register-Organization-of-Intel-8085.png' | relative_url }})

### # Classification of Registers

| Type                      | Registers                                |
| ------------------------- | ---------------------------------------- |
| General-Purpose Registers | B, C, D, E, H, L                         |
| Special-Purpose Registers | A, PC, SP, Flag Register                 |
| Internal Registers        | Instruction Register, Temporary Register |

## I. Accumulator (A Register)

Accumulator directly connected to the Arithmetic Logic Unit (ALU), making it the primary register for performing arithmetic and logical operations. The accumulator stores data (operands) before processing, holds intermediate results during calculations, and keeps the final result after an operation is completed. Because almost all arithmetic and logical instructions use the accumulator, it plays a central role in the execution of programs in the 8085 microprocessor.

## II. General-Purpose Registers

The Intel 8085 microprocessor has six general-purpose registers: B, C, D, E, H, and L. Each register is 8 bits wide and is used to store temporary data during program execution. These registers help the processor perform calculations and data manipulation efficiently without accessing memory repeatedly. Having six general-purpose registers allows the processor to store multiple values simultaneously, reducing memory access and improving execution speed.

### # Register Pairs

In the Intel 8085 microprocessor, two adjacent 8-bit registers can be combined to form a 16-bit register pair. The three register pairs are BC (B + C), DE (D + E), and HL (H + L). These register pairs are used to store 16-bit data or memory addresses, enabling the processor to handle larger values efficiently. Among them, the HL register pair is the most important because it is commonly used as a memory pointer. It stores the address of a memory location, allowing the processor to access data directly from memory. During many operations, the data stored at the memory location pointed to by the HL pair is transferred to the Accumulator for processing, making the HL pair essential for memory-related operations.

## III. Program Counter (PC)

The Program Counter (PC) is a 16-bit register that stores the address of the next instruction to be executed. After an instruction is fetched, the Program Counter is automatically updated to the address of the next instruction unless a branch, jump, or call instruction changes its value. This ensures that the processor executes instructions in the correct order.

## IV. Stack Pointer (SP)

The Stack Pointer (SP) is a 16-bit register that stores the address of the top of the stack in memory. The stack is a special area of memory used to temporarily store data, return addresses, and register contents during program execution. The Stack Pointer automatically updates whenever data is pushed onto or popped from the stack, ensuring that stack operations are performed correctly. It is especially important during subroutine calls, interrupts, and temporary data storage, making it an essential register for efficient program execution.

## V. Flag Register

The Flag Register stores the status of the most recent arithmetic or logical operation performed by the Arithmetic Logic Unit (ALU). It is an 8-bit register, but only five flags are active: Sign (S), Zero (Z), Auxiliary Carry (AC), Parity (P), and Carry (CY). The Sign Flag indicates whether the result is negative, the Zero Flag is set when the result is zero, the Auxiliary Carry Flag is used during Binary Coded Decimal (BCD) operations, the Parity Flag shows whether the result has even or odd parity, and the Carry Flag indicates a carry or borrow generated during arithmetic operations. These flags help the processor make decisions during program execution, especially in conditional branching and arithmetic operations.

## VI. Instruction Register

The Instruction Register temporarily stores the instruction fetched from memory.

## VII. Instruction Decoder

Instruction Decoder decodes the fetched instruction and generates the necessary control signals, allowing the processor to execute the instruction correctly.

## VIII. Temporary Register

The Temporary Register is used during arithmetic and logical operations. It is not accessible to the programmer, stores intermediate data, and assists the Arithmetic Logic Unit (ALU) in performing calculations efficiently.

## IX. Processor Status Word (PSW)

The Processor Status Word (PSW) is a combination of the Accumulator and the Flag Register. It stores both the result of an operation and the processor's status flags. The PSW can be saved to or restored from the stack using specific instructions, making it useful during subroutine calls and interrupt handling.

### # Register Sizes

| Register             | Size   |
| -------------------- | ------ |
| A                    | 8-bit  |
| B                    | 8-bit  |
| C                    | 8-bit  |
| D                    | 8-bit  |
| E                    | 8-bit  |
| H                    | 8-bit  |
| L                    | 8-bit  |
| Flag Register        | 8-bit  |
| Program Counter      | 16-bit |
| Stack Pointer        | 16-bit |
| Instruction Register | 8-bit  |
| Temporary Register   | 8-bit  |
