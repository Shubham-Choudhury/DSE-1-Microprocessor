---
layout: base
title: "Lecture 14: Logical Instructions of the 8085 Microprocessor"
date: 2026-06-29 09:50:00 +0530
categories: jekyll update
permalink: "/lecture-14-logical-instructions-of-the-8085-microprocessor/"
---

# {{ page.title | escape }}

## 1. What are Logical Instructions?

Logical instructions perform bit-by-bit operations on binary data instead of mathematical calculations.

They are mainly used for:

- Comparing bits
- Setting bits
- Clearing bits
- Toggling bits
- Masking
- Data encryption (basic concept)
- Hardware interfacing
- Digital circuit operations

## 2. What is a Bitwise Operation?

A bitwise operation compares corresponding bits of two binary numbers.

## 3. Types of Logical Operations

| Operation  | Meaning                         |
| ---------- | ------------------------------- |
| AND        | Common bits                     |
| OR         | Either bit                      |
| XOR        | Different bits                  |
| Compare    | Compare values                  |
| Complement | Invert bits                     |
| Rotate     | Shift bits in a circular manner |

### I. ANA (Logical AND)

The `ANA` instruction performs a logical AND between the Accumulator and a register or memory location.

Syntax: `ANA Register`

or

Syntax: `ANA M`

Example: `ANA B`

### II. ANI (AND Immediate)

The `ANI` instruction performs a logical AND between the Accumulator and immediate 8-bit data.

Syntax: `ANI Data`

Example: `ANI 0FH`

### III. ORA (Logical OR)

Performs logical OR between the Accumulator and a register or memory location.

Syntax: `ORA Register`

or

Syntax: `ORA M`

Example: `ORA B`

### IV. ORI (OR Immediate)

Syntax: `ORI Data`

Example: `ORI 05H`

### V. XRA (Exclusive OR)

Performs XOR between the Accumulator and a register or memory location.

Syntax: `XRA Register`

or

Syntax: `XRA M`

Example: `XRA B`

### VI. XRI (Exclusive OR Immediate)

Performs XOR with immediate data.

Syntax: `XRI Data`

Example: `XRI FFH`

### VII. CMP (Compare Register/Memory)

The `CMP` instruction compares the contents of a register (or memory location) with the Accumulator. However the result is not stored, the Accumulator remains unchanged, only the Flag Register is updated.

Syntax: `CMP Register`

or

Syntax: `CMP M`

### VIII. CPI (Compare Immediate)

Compares immediate 8-bit data with the Accumulator.

Syntax: `CPI Data`

### IX. CMA (Complement Accumulator)

Complements every bit of the Accumulator.

Syntax: `CMA`

### X. CMC (Complement Carry)

Reverses the Carry Flag.

0 -> 1

1 -> 0

Syntax: `CMC`

### XI. STC (Set Carry)

Sets Carry Flag to 1.

Syntax: `STC`

### XII. RLC (Rotate Left)

Rotates all bits of the Accumulator one position to the left. Bit D7 (MSB) moves to D0 (LSB). Bit D7 is also copied into the Carry Flag.

Syntax: `RLC`

### XIII. RRC (Rotate Right)

Rotates all bits of the Accumulator one position to the right. Bit D0 moves to D7. Bit D0 is copied into the Carry Flag.

Syntax: `RRC`

### XIV. RAL (Rotate Left through Carry)

Rotates bits left through the Carry Flag. D7 goes to Carry. Previous Carry enters D0.

Syntax: `RAL`

### XV. RAR (Rotate Right through Carry)

Rotates bits right through the Carry Flag. D0 moves to Carry. Previous Carry enters D7.