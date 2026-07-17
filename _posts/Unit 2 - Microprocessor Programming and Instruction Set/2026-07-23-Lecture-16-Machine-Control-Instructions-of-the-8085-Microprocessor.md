---
layout: base
title: "Lecture 16: Machine Control Instructions of the 8085 Microprocessor"
date: 2026-06-29 09:50:00 +0530
categories: jekyll update
permalink: "/lecture-16-machine-control-instructions-of-the-8085-microprocessor/"
---

# {{ page.title | escape }}

## 1. What are Machine Control Instructions?

Machine Control Instructions control the overall operation of the microprocessor rather than performing arithmetic or logical operations.

They are used to:

- Stop program execution.
- Introduce delays.
- Enable or disable interrupts.
- Read or set interrupt masks.
- Control processor state.

## 2. Classification of Machine Control Instructions

![Classification of Machine Control Instructions]({{ '/assets/images/Classification-of-Machine-Control-Instructions.png' | relative_url }})

### I. NOP (No Operation)

`NOP` stands for No Operation. The processor fetches and decodes the instruction but does not perform any operation. It generate small time delays.

Syntax: `NOP`

Example: 

```
MVI A,20H
NOP
NOP
ADI 10H
```

### II. HLT (Halt)

Stops program execution. The processor enters the HALT state until Reset signal, or Interrupt occurs.

Syntax: `HLT`

Example:
```
MVI A,25H
HLT
ADI 10H
```

## 3. What is an Interrupt?

An interrupt is a signal that temporarily stops the current program so the processor can respond to an urgent event.

### # Types of Interrupts

8085 microprocessor has hardware interrupts such as:

- TRAP
- RST 7.5
- RST 6.5
- RST 5.5
- INTR

