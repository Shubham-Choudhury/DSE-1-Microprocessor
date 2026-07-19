---
layout: base
title: "Lecture 17: Memory Organization and Memory Interfacing (Part 1)"
date: 2026-06-29 09:50:00 +0530
categories: jekyll update
permalink: "/lecture-17-memory-organization-and-memory-interfacing-part-1/"
---

# {{ page.title | escape }}

## 1. Memory Organization in a Computer

![Memory Organization in a Computer]({{ '/assets/images/Memory-Organization-in-a-Computer.png' | relative_url }})

## 2. Random Access Memory (RAM)

### # Characteristics of RAM

- Read and write memory
- Fast access
- Temporary storage
- Volatile

### # Applications

- Operating System
- Application software
- Program execution
- Data processing

### I. Static RAM (SRAM)

#### # Features

- Very fast
- No refresh required
- Expensive
- Lower storage capacity

#### # Uses

- Cache memory
- High-speed buffers

### II. Dynamic RAM (DRAM)

#### # Features

- Slower than SRAM
- Requires periodic refreshing
- Less expensive
- Higher storage capacity

#### # Uses

- Main memory (system RAM)

## 3. Read Only Memory (ROM)

### # Characteristics

- Read-only during normal operation
- Permanent storage
- Non-volatile
- Stores system software

### # Applications

- BIOS
- Embedded systems
- Bootloader
- Microcontroller firmware

### I. Mask ROM

Programmed during manufacturing, cannot be modified.

### II. PROM (Programmable ROM)

Programmed once by the user, cannot be erased.

### III. EPROM (Erasable Programmable ROM)

Can be erased using ultraviolet (UV) light, can be reprogrammed.

### IV. EEPROM (Electrically Erasable Programmable ROM)

Can be erased and programmed electrically. Widely used in modern embedded systems.
