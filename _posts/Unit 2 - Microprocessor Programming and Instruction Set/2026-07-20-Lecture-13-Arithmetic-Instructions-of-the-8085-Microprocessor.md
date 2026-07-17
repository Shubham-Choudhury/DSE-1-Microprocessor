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

### V. SUB

The SUB instruction subtracts the contents of a register or memory location from the Accumulator.

Syntax: `SUB Register`

or

Syntax: `SUB M`

Example: `SUB B`

### VI. SBB (Subtract with Borrow)

Subtracts the operand and the Carry Flag (borrow) from the Accumulator.

Syntax: `SBB Register`

or

Syntax: `SBB M`

Example: `SBB B`

### VII. SUI (Subtract Immediate)

Subtracts immediate data from the Accumulator.

Syntax: `SUI Data`

Example: `SUI 20H`

### VIII. SBI (Subtract Immediate with Borrow)

Subtracts immediate data and the Carry Flag from the Accumulator.

Syntax: `SBI Data`

Example: `SBI 10H`

### IX. INR (Increment)

Increases the value of a register or memory location by 1.

Syntax: `INR Register`

or 

Syntax: `INR M`

Example: `INR B`

### X. DCR (Decrement)

Decreases the value of a register or memory location by 1.

Syntax: `DCR Register`

or 

Syntax: `DCR M`

Example: `DCR B`

### XI. INX (Increment Register Pair)

Increments a 16-bit register pair by 1.

Syntax: `INX B`

or

Syntax: `INX D`

or

Syntax: `INX H`

or

Syntax: `INX SP`

Example: `INX H`

### XII. DCX (Decrement Register Pair)

Decrements a 16-bit register pair by 1.

### XIII. DAD (Double Add)

Adds a 16-bit register pair to the HL register pair.

Syntax `DAD RegisterPair`

Possible register pairs: BC, DE, HL, SP