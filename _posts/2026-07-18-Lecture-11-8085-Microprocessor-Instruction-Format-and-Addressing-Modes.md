---
layout: base
title: "Lecture 11: 8085 Microprocessor Instruction Format and Addressing Modes"
date: 2026-06-29 09:50:00 +0530
categories: jekyll update
permalink: "/lecture-11-8085-microprocessor-instruction-format-and-addressing-modes/"
---

# {{ page.title | escape }}

## 1. What is an Instruction?

An instruction is a command given to the microprocessor to perform a specific operation.

Examples: Move data, Add two numbers, Compare values, Jump to another instruction, Stop execution

### # Components of an Instruction

![Components of an Instruction]({{ '/assets/images/Components-of-an-Instruction.png' | relative_url }})

### # Opcode

The Opcode (Operation Code) specifies what operation the processor should perform.

### # Operand

The Operand specifies on which data the operation is performed.

## 2. General Instruction Format

![General Instruction Format]({{ '/assets/images/General-Instruction-Format.png' | relative_url }})

## 3. Instruction Length

The 8085 Microprocessor supports three instruction lengths:

<ol type="I">
<li>One-byte instructions</li>
<li>Two-byte instructions</li>
<li>Three-byte instructions</li>
</ol>

The length depends on the number of bytes required to store the instruction and its operands.

### I. One-Byte Instructions

A one-byte instruction occupies only one byte (8 bits) in memory. The opcode and operand information are encoded within the same byte.

#### Example:

```asm
MOV A,B
```

Stored at address: `2000H`

Memory:

| Address | Instruction |
| ------- | ----------- |
| 2000H   | MOV A,B     |

Only one memory location is occupied.

### II. Two-Byte Instructions

A two-byte instruction occupies two consecutive memory locations. The first byte contains the opcode. The second byte contains the data or port address.

#### Example:

```asm
MVI A,25H
```

Memory:

| Address | Contents |
| ------- | -------- |
| 2000H   | Opcode   |
| 2001H   | 25H      |

### III. Three-Byte Instructions

A three-byte instruction occupies three consecutive memory locations. The second and third bytes together form a 16-bit memory address.

#### Example:

```asm
LDA 2050H
```

Memory:

| Address | Contents          |
| ------- | ----------------- |
| 3000H   | Opcode            |
| 3001H   | 50H (Lower byte)  |
| 3002H   | 20H (Higher byte) |

## 4. What is an Addressing Mode?

The addressing mode specifies how the processor obtains the operand (data) required for an instruction.

### # Types of Addressing Modes in 8085 Microprocessor

| Addressing Mode   | Description                           |
| ----------------- | ------------------------------------- |
| Immediate         | Data is part of the instruction       |
| Register          | Data is in a register                 |
| Direct            | Address of data is given directly     |
| Register Indirect | Address is stored in a register pair  |
| Implied           | Operand is implied by the instruction |
