---
layout: base
title: "Lecture 3: Internal Architecture of Intel 8085 Microprocessor"
date: 2026-06-29 09:50:00 +0530
categories: jekyll update
permalink: "/lecture-3-internal-architecture-of-intel-8085-microprocessor/"
---

# {{ page.title | escape }}

## 1. Internal Block Diagram of Intel 8085

![Internal Block Diagram of Intel 8085]({{ '/assets/images/Internal-Block-Diagram-of-Intel-8085.png' | relative_url }})

## 2. Major Functional Blocks

The Intel 8085 consists of the following major blocks:

<ol type="I">
<li>Arithmetic Logic Unit (ALU)</li>
<li>Accumulator</li>
<li>General Purpose Registers</li>
<li>Flag Register</li>
<li>Program Counter</li>
<li>Stack Pointer</li>
<li>Instruction Register</li>
<li>Instruction Decoder</li>
<li>Timing and Control Unit</li>
<li>Address Buffer</li>
<li>Data Buffer</li>
<li>Interrupt Control</li>
<li>Serial I/O Control</li>
</ol>

## I. Arithmetic Logic Unit (ALU)

The ALU performs the actual numerical and logical operations such as Addition (ADD), Subtraction (SUB), AND, OR etc. It uses data from memory and from Accumulator to perform operations. The results of the arithmetic and logical operations are stored in the accumulator.

## II. Accumulator

The accumulator is an 8-bit register that is a part of ALU. This register is used to store 8-bit data and to perform arithmetic and logical operations. The result of an operation is stored in the accumulator. The accumulator is also identified as register A.

## III. General Purpose Registers

The 8085 includes six registers, one accumulator and one flag register. In addition, it has two 16-bit registers: stack pointer and program counter.

The 8085 has six general-purpose registers to store 8-bit data; these are identified as B, C, D, E, H and L. they can be combined as register pairs - BC, DE and HL to perform some 16- bit operations. The programmer can use these registers to store or copy data into the register by using data copy instructions.

## IV. Flag register

The ALU includes five flip-flops, which are set or reset after an operation according to data condition of the result in the accumulator and other registers. They are called Zero (Z), Carry (CY), Sign (S), Parity (P) and Auxiliary Carry (AC) flags. Their bit positions in the flag register are shown in Fig. 4. The microprocessor uses these flags to test data conditions.

![Flag register]({{ '/assets/images/Flag-Register.png' | relative_url }})

For example, after an addition of two numbers, if the result in the accumulator is larger than 8-bit, the flip-flop uses to indicate a carry by setting CY flag to 1. When an arithmetic operation results in zero, Z flag is set to 1. The S flag is just a copy of the bit D7 of the accumulator. A negative number has a 1 in bit D7 and a positive number has a 0 in 2’s complement representation. The AC flag is set to 1, when a carry result from bit D3 and passes to bit D4. The P flag is set to 1, when the result in accumulator contains even number of 1s.

## V. Program Counter (PC)

This 16-bit register deals with sequencing the execution of instructions. This register is a memory pointer. The microprocessor uses this register to sequence the execution of the instructions. The function of the program counter is to point to the memory address from which the next byte is to be fetched. When a byte is being fetched, the program counter is automatically incremented by one to point to the next memory location.

## VII. Stack Pointer (SP)

The stack pointer is also a 16-bit register, used as a memory pointer. It points to a memory location in R/W memory, called stack. The beginning of the stack is defined by loading 16-bit address in the stack pointer.

## VIII. Instruction Register/Decoder

It is an 8-bit register that temporarily stores the current instruction of a program. Latest instruction sent here from memory prior to execution. Decoder then takes instruction and decodes or interprets the instruction. Decoded instruction then passed to next stage.

## IX. Timing and Control Unit

The Timing and Control Unit coordinates all processor activities. It generates timing signals to ensure each operation occurs in the correct sequence. Functions include:

- Reading memory
- Writing memory
- Reading I/O ports
- Writing I/O ports
- Synchronizing internal operations

## X. Address Buffer

The Address Buffer sends memory addresses to external memory.

The Intel 8085 has a 16-bit Address Bus, allowing it to access: $2^{16} = \text{65,536 bytes} = \text{64 KB}$

## XI. Data Buffer

The Data Buffer transfers data between the processor and memory or I/O devices.

Characteristics:

- 8-bit wide
- Bidirectional
- Carries data and instructions

## XII. Interrupt Control

An Interrupt is a signal that temporarily stops the current program so the processor can respond to an urgent event.

Examples:

- Keyboard key press
- Printer request
- Timer overflow

The Interrupt Control Unit manages these requests.

## XIII. Serial Input/Output Control

The Intel 8085 supports serial communication through two pins:

| Pin | Function           |
| --- | ------------------ |
| SID | Serial Input Data  |
| SOD | Serial Output Data |

These pins are used to communicate with serial devices one bit at a time.
