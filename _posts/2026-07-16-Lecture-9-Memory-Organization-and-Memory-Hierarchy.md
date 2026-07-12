---
layout: base
title: "Lecture 9: Memory Organization and Memory Hierarchy"
date: 2026-06-29 09:50:00 +0530
categories: jekyll update
permalink: "/lecture-9-memory-organization-and-memory-hierarchy/"
---

# {{ page.title | escape }}

## 1. What is Memory?

Memory is a storage unit that holds data and instructions required by the microprocessor for processing.

## 2. Basic Memory Organization

![Basic Memory Organization]({{ '/assets/images/Basic-Memory-Organization.png' | relative_url }})

## 3. Memory Terminology

### # Bit

Smallest unit of information.

Possible values: 0 or 1

### # Byte

One Byte = 8 bits

### # Word

A word is the amount of data processed by the processor in one operation.

| Processor         | Word Size |
| ----------------- | --------- |
| 8085              | 8 bits    |
| 8086              | 16 bits   |
| Modern 64-bit CPU | 64 bits   |

## 4. Types of Memory

![Types of Memory]({{ '/assets/images/Types-of-Memory.png' | relative_url }})

### # Primary Memory

Primary memory is directly accessible by the processor. It is also called Main Memory.

Examples: RAM, ROM, Cache Memory

Characteristics:

- Fast access
- Smaller capacity
- More expensive than secondary storage

### # Secondary Memory

Secondary memory stores data permanently.

Examples: Hard Disk, SSD, CD/DVD, Pen Drive, Memory Card

Characteristics:

- Large capacity
- Slower than RAM
- Non-volatile

## 5. Memory Hierarchy

Different memories have different speeds and costs. To achieve high performance at a reasonable cost, computers use a memory hierarchy.

![Memory Hierarchy]({{ '/assets/images/Memory-Hierarchy.png' | relative_url }})

| Memory    | Speed     | Capacity | Cost     |
| --------- | --------- | -------- | -------- |
| Registers | Highest   | Lowest   | Highest  |
| Cache     | Very High | Small    | High     |
| RAM       | High      | Medium   | Moderate |
| SSD/HDD   | Low       | Large    | Low      |

## Registers

Registers are located inside the processor.

Examples: Accumulator, B Register, Program Counter, Stack Pointer

Characteristics:

- Fastest memory
- Very small capacity
- Directly accessed by the CPU

## Cache Memory

Cache Memory is a high-speed memory placed between the CPU and RAM.

**Purpose:** Reduce the time required to access frequently used data.

Advantages:

- Very fast
- Reduces CPU waiting time
- Improves overall system performance

## Random Access Memory (RAM)

RAM is a temporary storage memory used while the computer is running.

It stores: Operating system, Running programs, Temporary data, Characteristics, Read and write memory, Volatile, High speed

## Read Only Memory (ROM)

ROM stores permanent programs.

Examples: BIOS, Firmware, Boot program

Characteristics

- Non-volatile
- Read-only during normal operation
- Stores permanent instructions

| RAM                     | ROM               |
| ----------------------- | ----------------- |
| Volatile                | Non-volatile      |
| Read and Write          | Mostly Read Only  |
| Temporary Storage       | Permanent Storage |
| Faster                  | Slightly slower   |
| Stores running programs | Stores firmware   |

## Secondary Storage

Examples: Hard Disk, SSD, USB Flash Drive

Characteristics:

- Permanent storage
- Very large capacity
- Slower than RAM
