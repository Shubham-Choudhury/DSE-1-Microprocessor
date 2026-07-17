---
layout: base
title: "Lecture 1: Introduction to Microprocessors"
date: 2026-06-25 00:00:00 +0530
categories: jekyll update
permalink: "/lecture-1-introduction-to-microprocessors/"
---

# {{ page.title | escape }}

## 1. What is a Microprocessor?

**Definition:** A Microprocessor is a programmable electronic integrated circuit (IC) that accepts binary data as input, processes it according to instructions stored in memory, and produces output.

## 2. Block Diagram of a Microprocessor System

![Block Diagram of a Microprocessor System]({{ '/assets/images/Block-Diagram-of-a-Microprocessor-System.png' | relative_url }})

### Explanation

**Input:** `Provides data and instructions.`

Examples:

```
Keyboard
Mouse
Scanner
```

**Memory:**

Stores:

- Data
- Programs
- Intermediate results

**Microprocessor:** Processes data according to instructions.

**Output:** Displays results.

Examples:

```
Monitor
Printer
Speakers
```

## 3. Functions of a Microprocessor

A microprocessor performs four major functions:

1. **Fetch:** Obtains instructions from memory.

   Example:

   ```
   ADD A, B
   ```

   The processor fetches this instruction from memory.

2. **Decode:** Determines what the instruction means.

   Example:

   ```
   ADD A, B
   ```

   The processor understands that it must add B to A.

3. **Execute:** Performs the operation.

   Example:

   ```
   A = A + B
   ```

4. **Store Result:** Stores the result back into memory or a register.

### Fetch-Decode-Execute Cycle

![Fetch-Decode-Execute Cycle]({{ '/assets/images/Fetch-Decode-Execute-Cycle.png' | relative_url }})

## 4. Characteristics of a Microprocessor

A microprocessor has the following features:

- **Programmable:** Can execute different programs.

- **High Speed:** Processes millions of instructions per second.

- **Compact Size:** Available on a small IC chip.

- **Reliable:** Works continuously without fatigue.

- **Versatile:** Can be used in many applications.

## 5. Evolution of Microprocessors

| Processor         | Year    | Word Length |
| ----------------- | ------- | ----------- |
| Intel 4004        | 1971    | 4-bit       |
| Intel 8008        | 1972    | 8-bit       |
| Intel 8080        | 1974    | 8-bit       |
| Intel 8085        | 1976    | 8-bit       |
| Intel 8086        | 1978    | 16-bit      |
| Intel Pentium     | 1993    | 32-bit      |
| Modern Processors | Present | 64-bit      |

## 6. CPU vs Microprocessor

- CPU:

  CPU stands for: Central Processing Unit

  It is the logical processing unit of a computer.

- Microprocessor

  A microprocessor is an implementation of the CPU on a single chip.

| CPU                 | Microprocessor           |
| ------------------- | ------------------------ |
| Functional unit     | Physical chip            |
| Performs processing | Implements CPU functions |
| Concept             | Hardware device          |

In modern systems, CPU and Microprocessor are often used interchangeably.

## 7. Advantages of Microprocessors

- **High Speed:** Millions or billions of operations per second.

- **Accuracy:** Produces precise results.

- **Automation:** Can perform tasks without human intervention.

- **Reliability:** Works continuously.

- **Cost Effective:** Mass production lowers cost.

## 8. Limitations of Microprocessors

- **Requires Programming:** Cannot work without instructions.

- **Depends on Memory:** Needs external memory for storage.

- **Power Requirement:** Requires electrical power.
