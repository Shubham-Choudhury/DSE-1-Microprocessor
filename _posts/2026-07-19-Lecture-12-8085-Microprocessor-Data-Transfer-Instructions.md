---
layout: base
title: "Lecture 12: 8085 Microprocessor Data Transfer Instructions"
date: 2026-06-29 09:50:00 +0530
categories: jekyll update
permalink: "/lecture-12-8085-microprocessor-data-transfer-instructions/"
---

# {{ page.title | escape }}

## 1. What are Data Transfer Instructions?

Data Transfer Instructions are used to copy data from one location to another.

The data may be transferred:

- Register → Register
- Register → Memory
- Memory → Register
- Immediate Data → Register
- Memory → Accumulator
- Accumulator → Memory

## 2. Classification of Data Transfer Instructions

| Instruction | Purpose                            |
| ----------- | ---------------------------------- |
| MOV         | Register/Memory to Register/Memory |
| MVI         | Load immediate data                |
| LXI         | Load register pair immediately     |
| LDA         | Load accumulator directly          |
| STA         | Store accumulator directly         |
| LDAX        | Load accumulator indirectly        |
| STAX        | Store accumulator indirectly       |
| LHLD        | Load HL pair directly              |
| SHLD        | Store HL pair directly             |
| XCHG        | Exchange HL and DE register pairs  |

### I. MOV Instruction (Move)

`MOV` copies data from the source register (or memory) to the destination register (or memory).

Syntax: `MOV destination, source`

Example: `MOV A,B`

### II. MVI (Move Immediate)

`MVI` loads 8-bit immediate data into a register or memory location.

Syntax: `MVI Register, Data`

or

Syntax: `MVI M, Data`

Example: `MVI A,25H`

### III. LXI (Load Register Pair Immediate)

`LXI` loads a 16-bit immediate value into a register pair.

Syntax: `LXI RegisterPair,16-bit Data`

Example: `LXI SP,4000H`

### IV. LDA (Load Accumulator Direct)

Loads the contents of a specified memory location into the Accumulator.

Syntax: `LDA Address`

Example: `LDA 2500H`

### V. STA (Store Accumulator Direct)

Stores the contents of the Accumulator into a specified memory location.

Syntax: `STA Address`

Example: `STA 3000H`

### VI. LDAX (Load Accumulator Indirect)

Loads the Accumulator using the memory address contained in a register pair. Only BC and DE register pairs are allowed.

Syntax: `LDAX Register Pair`

Example: `LDAX BC`

### VII. STAX (Store Accumulator Indirect)

Stores the Accumulator into the memory location pointed to by BC or DE.

Syntax: `STAX Register Pair`

Example: `STAX BC`

### VIII. LHLD (Load H and L Direct)

Loads the HL register pair directly from two consecutive memory locations.

Syntax: `LHLD Address`

Example: `LHLD 2500H`

### IX. SHLD (Store H and L Direct)

Stores the HL register pair into two consecutive memory locations.

Syntax: `SHLD Address`

Example: `SHLD 2500H`

### X. XCHG (Exchange Register Pairs)

Exchanges the contents of the HL and DE register pairs.

Syntax: `XCHG`

