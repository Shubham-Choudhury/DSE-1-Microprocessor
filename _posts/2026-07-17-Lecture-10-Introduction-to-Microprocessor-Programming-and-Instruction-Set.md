---
layout: base
title: "Lecture 10: Introduction to Microprocessor Programming and Instruction Set"
date: 2026-06-29 09:50:00 +0530
categories: jekyll update
permalink: "/lecture-10-introduction-to-microprocessor-programming-and-instruction-set/"
---

# {{ page.title | escape }}

## 1. Why Do We Need Programming?

A microprocessor is an electronic device. It cannot think or make decisions on its own. It only executes the instructions provided by the programmer.

Without a program:

- The processor cannot perform calculations.
- It cannot communicate with memory or I/O devices.
- It cannot solve problems.

## 2. Program Execution Cycle

![Program Execution Cycle]({{ '/assets/images/Program-Execution-Cycle.png' | relative_url }})

## 3. Programming Languages

Programming languages can be classified into three categories:

![Programming Languages]({{ '/assets/images/Programming-Languages.png' | relative_url }})

## I. Machine Language

Machine Language is the lowest-level programming language understood directly by the microprocessor. It consists of binary numbers (0s and 1s).

### # Advantages

- Fast execution
- No translation required
- Directly understood by the processor

### # Disadvantages

- Very difficult to write
- Difficult to debug
- Difficult to remember binary codes
- Processor-dependent

## II. Assembly Language

Assembly Language uses mnemonic codes instead of binary numbers. A mnemonic is a short, meaningful abbreviation representing an instruction.

### # Examples of Mnemonics

| Mnemonic | Meaning             |
| -------- | ------------------- |
| MOV      | Move data           |
| MVI      | Move immediate data |
| ADD      | Add                 |
| SUB      | Subtract            |
| INR      | Increment           |
| DCR      | Decrement           |
| JMP      | Jump                |
| HLT      | Halt the processor  |

### # Advantages

- Easy to understand
- Easier debugging
- Shorter development time
- Suitable for hardware-level programming

### # Disadvantages

- Must be translated before execution
- Processor-dependent
- Not as portable as high-level languages

## III. High-Level Languages (HLL)

High-Level Languages are designed to resemble human language.

Examples: C, C++, Java, Python

### # Advantages

- Easy to learn
- Portable across different processors
- Faster software development
- Easier maintenance

### # Disadvantages

- Requires a compiler or interpreter
- Generally produces less hardware-specific code than assembly language
- Offers less direct control over hardware

## 4. Assembler

An Assembler converts an Assembly Language program into Machine Language.

## 5. Compiler

A Compiler converts an entire High-Level Language program into Machine Language before execution. The compiler translates the complete program into executable machine code.

### # Characteristics

- Translates the entire program at once.
- Reports errors after compilation.
- Produces an executable program.

## 6. Interpreter

An Interpreter translates and executes a High-Level Language program one statement at a time.

### # Characteristics

- Executes line by line.
- Stops immediately if an error is found.
- Does not usually generate a separate executable file.

### # Compiler vs Interpreter

| Compiler                           | Interpreter                        |
| ---------------------------------- | ---------------------------------- |
| Translates the whole program       | Translates one statement at a time |
| Faster execution after compilation | Slower execution                   |
| Produces executable code           | Usually no separate executable     |
| Errors shown after compilation     | Errors shown immediately           |

## 7. Structure of an Assembly Language Program

A simple assembly language program generally consists of:

<ol type="I">
<li>Comments</li>
<li>Labels (optional)</li>
<li>Mnemonics</li>
<li>Operands</li>
</ol>

### # Example:

```asm
START:   MVI A,25H    ; Load 25H into Accumulator
         MVI B,15H    ; Load 15H into Register B
         ADD B        ; Add B to A
         HLT          ; Stop execution
```

## 8. What is an Instruction?

An Instruction is a command that tells the microprocessor to perform a specific operation.

Examples: Move data, Add numbers, Compare values, Jump to another instruction, Stop execution

### # Components of an Instruction

An instruction generally consists of:

$$\text{Mnemonic} + \text{Operand(s)}$$

## 9. Classification of the 8085 Microprocessor Instruction Set

| Category                     | Purpose                       |
| ---------------------------- | ----------------------------- |
| Data Transfer Instructions   | Move data                     |
| Arithmetic Instructions      | Perform arithmetic operations |
| Logical Instructions         | Perform logical operations    |
| Branch Instructions          | Change program flow           |
| Machine Control Instructions | Control processor operation   |

### # Examples

#### Data Transfer

```asm
MOV A,B
MVI C,25H
LDA 2050H
```

#### Arithmetic

```asm
ADD B
SUB C
INR A
DCR B
```

#### Logical

```asm
ANA B
ORA C
XRA D
CMP E
```

#### Branch

```asm
JMP LOOP
JC NEXT
JZ END
CALL SUB1
RET
```

#### Machine Control

```asm
NOP
HLT
EI
DI
```
