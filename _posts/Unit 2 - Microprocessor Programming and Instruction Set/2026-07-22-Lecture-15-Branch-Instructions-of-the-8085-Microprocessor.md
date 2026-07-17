---
layout: base
title: "Lecture 15: Branch Instructions of the 8085 Microprocessor"
date: 2026-06-29 09:50:00 +0530
categories: jekyll update
permalink: "/lecture-15-branch-instructions-of-the-8085-microprocessor/"
---

# {{ page.title | escape }}

## 1. What are Branch Instructions?

A microprocessor executes instructions one after another in memory. This is called sequential execution. Many real-world problems require decisions, loops, or repeated actions. In such cases, the program must change its normal sequence of execution. Instructions that change the normal execution sequence are called Branch Instructions.

## 2. Types of Branch Instructions

8085 microprocessor branch instructions can be classified into three groups:

![Types of Branch Instructions]({{ '/assets/images/Types-of-Branch-Instructions.png' | relative_url }})

## # Jump Instructions

A Jump instruction transfers program control to another memory location.

There are two types:

<ol type="A">
<li>Unconditional Jump</li>
<li>Conditional Jump</li>
</ol>

## A. Unconditional Jump (JMP)

The `JMP` instruction always transfers control to the specified address. No condition is checked.

Syntax: `JMP Address`

Example:

```asm
MVI A,10H
JMP NEXT
MVI A,20H
NEXT:
HLT
```

## B. Conditional Jump Instructions

Conditional jumps execute only if a specific flag condition is satisfied. The processor first checks the Flag Register. If the condition is true then Jump occurs, otherwise execution continues normally.

### I. JZ (Jump if Zero)

Jumps when the Zero Flag = 1.

Syntax: `JZ Address`

Example:

```
MVI A,20H
MVI B,20H
CMP B
JZ EQUAL
MVI C,01H

EQUAL:
HLT
```

### II. JNZ (Jump if Not Zero)

Jump if Zero Flag = 0.

Syntax: `JNZ Address`

Example:

```
MVI A,20H
MVI B,15H
CMP B
JNZ NOTEQUAL
HLT

NOTEQUAL:
MVI C,01H
HLT
```

### III. JC (Jump if Carry)

Jumps when carry = 1

Syntax: `JC Address`

Example:

```
MVI A,20H
MVI B,30H
CMP B
JC SMALL
HLT

SMALL:
MVI C,01H
HLT
```

### IV. JNC (Jump if No Carry)

Jumps when carry = 0

Syntax: `JNC Address`

Example:

```
MVI A,40H
MVI B,20H
CMP B
JNC GREATER
HLT

GREATER:
MVI D,01H
HLT
```

### V. JP (Jump if Positive)

The `JP` instruction transfers control if the Sign Flag (S) = 0, indicating a positive result.

Syntax: `JP Address`

Example:

```
MVI A,20H
SUI 10H
JP POSITIVE
HLT

POSITIVE:
MVI B,01H
HLT
```

### VI. JM (Jump if Minus)

The `JM` instruction transfers control if the Sign Flag (S) = 1, indicating a negative result (MSB = 1 in two's complement representation).

Syntax: `JM Address`

Example:

```
MVI A,10H
SUI 20H
JM NEGATIVE
HLT

NEGATIVE:
MVI B,FFH
HLT
```

### VII. JPE (Jump if Parity Even)

The `JPE` instruction transfers control if the Parity Flag (P) = 1, meaning the result contains an even number of 1s.

Syntax: `JPE Address`

### VIII. JPO (Jump if Parity Odd)

The `JPO` instruction transfers control if the Parity Flag (P) = 0, meaning the result contains an odd number of 1s.

Syntax: `JPO Address`

## 3. What is a Subroutine?

A subroutine is a reusable block of instructions designed to perform a specific task.

### # Advantages of Subroutines

- Reduces program size
- Avoids duplicate code
- Makes debugging easier
- Improves readability
- Simplifies maintenance

### # CALL Instruction

The `CALL` instruction transfers control to a subroutine.

Syntax: `CALL Address`

### # RET (Return)

The `RET` instruction returns execution from the subroutine to the main program.

Syntax: `RET`

Example:

```
START:
MVI A,10H
CALL SUB1
HLT

SUB1:
ADI 20H
RET
```

### # Conditional CALL Instructions

The 8085 microprocessor also supports conditional calls. A conditional `CALL` executes only if its specified condition is true.

| Instruction | Condition           |
| ----------- | ------------------- |
| CZ          | Call if Zero        |
| CNZ         | Call if Not Zero    |
| CC          | Call if Carry       |
| CNC         | Call if No Carry    |
| CP          | Call if Positive    |
| CM          | Call if Minus       |
| CPE         | Call if Parity Even |
| CPO         | Call if Parity Odd  |

### # Conditional Return Instructions

Conditional return instructions return from a subroutine only when a specified condition is satisfied.

| Instruction | Condition             |
| ----------- | --------------------- |
| RZ          | Return if Zero        |
| RNZ         | Return if Not Zero    |
| RC          | Return if Carry       |
| RNC         | Return if No Carry    |
| RP          | Return if Positive    |
| RM          | Return if Minus       |
| RPE         | Return if Parity Even |
| RPO         | Return if Parity Odd  |

### # RST (Restart) Instructions

`RST` (Restart) is a one-byte instruction that transfers control to one of eight fixed memory locations.

| Instruction | Address |
| ----------- | ------- |
| RST 0       | 0000H   |
| RST 1       | 0008H   |
| RST 2       | 0010H   |
| RST 3       | 0018H   |
| RST 4       | 0020H   |
| RST 5       | 0028H   |
| RST 6       | 0030H   |
| RST 7       | 0038H   |
