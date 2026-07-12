---
layout: base
title: "Lecture 6: Flag Register and Processor Status Word"
date: 2026-06-29 09:50:00 +0530
categories: jekyll update
permalink: "/lecture-6-flag-register-and-processor-status-word/"
---

# {{ page.title | escape }}

## 1. What is a Flag Register?

The Flag Register is an 8-bit special-purpose register that stores the status (condition) of the result produced by the Arithmetic Logic Unit (ALU). Whenever the ALU performs an arithmetic or logical operation, the Flag Register is automatically updated. The programmer can then use these flags to make decisions in a program.

### # Bit Structure of the Flag Register

The Intel 8085 Flag Register contains 8 bits, but only 5 bits are active.

![Bit Structure of the Flag Register]({{ '/assets/images/Bit-Structure-of-the-Flag-Register.png' | relative_url }})

### # Explanation

| Bit | Name                 | Purpose                              |
| --- | -------------------- | ------------------------------------ |
| D7  | Sign Flag (S)        | Indicates sign of the result         |
| D6  | Zero Flag (Z)        | Indicates whether the result is zero |
| D5  | Reserved             | Always 0                             |
| D4  | Auxiliary Carry (AC) | Indicates carry from bit 3 to bit 4  |
| D3  | Reserved             | Always 0                             |
| D2  | Parity Flag (P)      | Indicates parity of the result       |
| D1  | Reserved             | Always 1                             |
| D0  | Carry Flag (CY)      | Indicates carry or borrow            |

### # Sign Flag (S)

The Sign Flag (SF) indicates whether the result of an arithmetic or logical operation is positive or negative. It reflects the value of the Most Significant Bit (MSB) of the result. In an 8-bit binary number, the MSB is Bit 7. If Bit 7 is 1, the result is interpreted as negative in signed (two's complement) representation, and the Sign Flag is set to 1. If Bit 7 is 0, the result is considered positive or zero, and the Sign Flag is cleared to 0. The Sign Flag is commonly used by processors to determine the sign of a result and to support conditional branching and comparison operations in assembly language programs.

### # Zero Flag (Z)

The Zero Flag (ZF) indicates whether the result of an arithmetic or logical operation is zero. The Zero Flag is set to 1 when the result of an operation is 00H (zero), and it is cleared to 0 when the result is any non-zero value. This flag is widely used in processors for comparison and decision-making operations, allowing programs to determine whether two values are equal or whether an operation has produced a zero result. It plays an important role in conditional branching and loop control in assembly language programming.

### # Carry Flag (CY)

The Carry Flag (CY) indicates whether an arithmetic operation generates a carry or a borrow. It is set to 1 when an addition operation produces a carry out of the Most Significant Bit (MSB), indicating that the result exceeds the maximum value that can be stored in the register. During subtraction, the Carry Flag is also used to indicate a borrow, meaning the subtraction required borrowing from a higher-order bit. If no carry or borrow occurs, the Carry Flag is cleared to 0. This flag is essential for performing multi-byte arithmetic operations and is widely used in conditional branching and arithmetic instructions in assembly language programming.

### # Auxiliary Carry Flag (AC)

The Auxiliary Carry Flag (AC) indicates whether a carry is generated from bit 3 to bit 4 during an arithmetic operation. The Auxiliary Carry Flag is set to 1 when this carry occurs and cleared to 0 when it does not. Unlike the Carry Flag, which detects a carry out of the Most Significant Bit (MSB), the Auxiliary Carry Flag is specifically used for operations involving the lower four bits of a byte. It plays an important role in Binary-Coded Decimal (BCD) arithmetic, particularly with instructions such as decimal adjustment, ensuring accurate decimal calculations in assembly language programming.

### # Parity Flag (P)

The Parity Flag (P) is a status flag in the microprocessor's flag register that indicates the parity of the result produced by an arithmetic or logical operation. It examines the number of 1 bits in the least significant byte (8 bits) of the result. If the result contains an even number of 1s, the Parity Flag is set (P = 1), indicating even parity. If the result contains an odd number of 1s, the Parity Flag is cleared (P = 0), indicating odd parity. The Parity Flag is commonly used for error detection in data communication and memory operations, as even parity helps identify single-bit transmission errors.

## 2. Processor Status Word (PSW)

The Processor Status Word (PSW) is a special 16-bit register pair in the 8085 microprocessor that represents the current status of the processor. It consists of two 8-bit registers:

Accumulator (A) – Stores the result of arithmetic and logical operations.
Flag Register (F) – Stores the status of the processor after an operation.

Thus,

PSW = Accumulator (A) + Flag Register (F)

### # Saving and Restoring the PSW

During the execution of a program, it is often necessary to save the current processor state before calling a subroutine or servicing an interrupt. The Intel 8085 provides two special instructions for this purpose.

1. PUSH PSW

   The PUSH PSW instruction saves the contents of the Accumulator and the Flag Register onto the stack. This preserves the processor's current status so that it can be restored later.

   Syntax:

   ```
   PUSH PSW
   ```

   Operation:
   - Pushes the Accumulator (A) and Flag Register (F) onto the stack.
   - Decrements the Stack Pointer (SP) by two bytes.

2. POP PSW

   The POP PSW instruction restores the previously saved Accumulator and Flag Register from the stack.

   Syntax:

   ```
   POP PSW
   ```

   Operation:
   - Retrieves the Flag Register and Accumulator from the stack.
   - Increments the Stack Pointer (SP) by two bytes.

| Flag | Full Name       | Function                           | Typical Use           |
| ---- | --------------- | ---------------------------------- | --------------------- |
| S    | Sign            | Indicates positive/negative result | Signed arithmetic     |
| Z    | Zero            | Indicates zero result              | Equality testing      |
| AC   | Auxiliary Carry | Carry from bit 3 to bit 4          | BCD arithmetic        |
| P    | Parity          | Indicates even/odd parity          | Error detection       |
| CY   | Carry           | Indicates carry or borrow          | Multi-byte arithmetic |
