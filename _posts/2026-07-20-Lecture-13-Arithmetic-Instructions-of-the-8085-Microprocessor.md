---
layout: base
title: "Lecture 13: Arithmetic Instructions of the 8085 Microprocessor"
date: 2026-06-29 09:50:00 +0530
categories: jekyll update
permalink: "/lecture-13-arithmetic-instructions-of-the-8085-microprocessor/"
---

# {{ page.title | escape }}

## 1. What are Arithmetic Instructions?

Arithmetic Instructions perform mathematical operations on data. They are used for:

- Addition
- Subtraction
- Increment
- Decrement
- 16-bit addition

## 2. Classification of Arithmetic Instructions

| Instruction | Operation                          |
| ----------- | ---------------------------------- |
| ADD         | Add register/memory to Accumulator |
| ADC         | Add with Carry                     |
| ADI         | Add immediate data                 |
| ACI         | Add immediate data with Carry      |
| SUB         | Subtract register/memory           |
| SBB         | Subtract with Borrow               |
| SUI         | Subtract immediate                 |
| SBI         | Subtract immediate with Borrow     |
| INR         | Increment by 1                     |
| DCR         | Decrement by 1                     |
| INX         | Increment register pair            |
| DCX         | Decrement register pair            |
| DAD         | 16-bit addition                    |

### I. ADD Instruction

The `ADD` instruction adds the contents of a register or memory location to the Accumulator. The result is stored in the Accumulator.

Syntax: `ADD Register`

or 

Syntax: `ADD M`

Example: `ADD B`

### II. ADC (Add with Carry)

The ADC instruction adds Accumulator, Operand, Existing Carry Flag.

Syntax: `ADC Register`

or 

Syntax: `ADC M`

Example: `ADC B`

#### # Why is ADC Needed?

It is used for multi-byte addition. When adding large numbers (16-bit, 32-bit, etc.), the carry generated from the lower byte must be added to the higher byte.

### III. ADI (Add Immediate)

The `ADI` instruction adds 8-bit immediate data to the Accumulator.

Synttax: `ADI Data`

Example: `ADI 30H`

### IV. ACI (Add Immediate with Carry)

Adds immediate data and the Carry Flag to the Accumulator.

Syntax: `ACI Data`

Example: `ACI 15H`

