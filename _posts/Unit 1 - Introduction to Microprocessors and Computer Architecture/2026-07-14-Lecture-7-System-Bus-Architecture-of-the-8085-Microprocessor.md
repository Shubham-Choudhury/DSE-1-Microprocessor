---
layout: base
title: "Lecture 7: System Bus Architecture of the 8085 Microprocessor"
date: 2026-06-29 09:50:00 +0530
categories: jekyll update
permalink: "/lecture-7-system-bus-architecture-of-the-8085-microprocessor/"
---

# {{ page.title | escape }}

## 1. What is a Bus?

A Bus is a collection of parallel electrical lines used to transfer data, addresses, and control signals between different components of a computer.

### # Why Are Buses Required?

Without buses the processor cannot access memory, data cannot move between components, input and output devices cannot communicate. Therefore, buses are essential for every computer system.

### # System Bus Architecture

![System Bus Architecture]({{ '/assets/images/System-Bus-Architecture.png' | relative_url }})

### # Types of Buses

There are three fundamental buses:

| Bus         | Function                |
| ----------- | ----------------------- |
| Address Bus | Carries addresses       |
| Data Bus    | Carries data            |
| Control Bus | Carries control signals |

## I. Address Bus

The Address Bus carries the address of the memory location or I/O device that the processor wants to access.

Characteristics:

- Unidirectional
- Carries only addresses
- Width determines maximum memory capacity

### # Why is it Unidirectional?

The processor generates the address. Memory only receives it. The address never travels from memory back to the processor.

### # Address Bus in 8085 Microprocessor

The Intel 8085 has a 16-bit Address Bus. It consists of A15–A8 (Higher-order address lines) and AD7–AD0 (Lower-order address lines during the first part of the machine cycle)

## II. Data Bus

The Data Bus transfers actual data between the processor and memory or I/O devices.

Characteristics

- Bidirectional
- Transfers data and instructions
- Width determines how much data is transferred at a time

### # Data Bus in 8085 Microprocessor

The Intel 8085 has an 8-bit Data Bus. Therefore, it can transfer 8 bits = 1 byte in one operation.

## III. Control Bus

The Control Bus carries control and timing signals that coordinate communication between the processor and external devices.

Examples of Control Signals

- RD (Read)
- WR (Write)
- ALE (Address Latch Enable)
- IO/M
- RESET
- HOLD
- HLDA
- INTA

## Advantages of the System Bus

- Enables communication between all hardware components.
- Simplifies processor design.
- Allows memory expansion.
- Supports connection of various I/O devices.
- Makes computer systems modular and scalable.
