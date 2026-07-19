---
layout: base
title: "Lecture 20: Memory Organization and Memory Interfacing (Part 4)"
date: 2026-06-29 09:50:00 +0530
categories: jekyll update
permalink: "/lecture-20-memory-organization-and-memory-interfacing-part-4/"
---

# {{ page.title | escape }}

## 1. Memory Chip Organization

A memory chip consists of Memory cells, Address decoder, Control logic, Input/Output circuitry

### # Components

- **Memory Cell Array:** Stores binary data (0 or 1).

- **Address Decoder:** Selects one memory location based on the input address.

- **Control Logic:** Performs read and write operations.

- **Data Bus:** Transfers data between the processor and memory.

## 2. Memory Capacity

Memory capacity is the total amount of data that a memory chip can store.

### # Formula

$$ \text{Memory Capacity} = 2^n * m $$

where:

- n = Number of address lines
- m = Number of bits per memory location

## 3. Memory Organization

Memory chips are described using the notation:

$$ \text{Number of Locations } \text{ x } \text{Bits per Location} $$

| Memory Organization | Meaning                      |
| ------------------- | ---------------------------- |
| 1K × 8              | 1024 locations, 8 bits each  |
| 2K × 8              | 2048 locations, 8 bits each  |
| 4K × 8              | 4096 locations, 8 bits each  |
| 8K × 8              | 8192 locations, 8 bits each  |
| 16K × 8             | 16384 locations, 8 bits each |
| 32K × 8             | 32768 locations, 8 bits each |

## 4. Address Lines Required

To determine the number of address lines:

$$ \text{Address Lines} = \log_{2}(\text{Number of Memory Locations}) $$

## 5. Data Lines

The 8085 microprocessor has an 8-bit data bus, so a single memory access transfers 8 bits (1 byte).
