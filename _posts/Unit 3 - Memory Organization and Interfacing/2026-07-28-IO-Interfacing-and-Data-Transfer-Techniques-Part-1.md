---
layout: base
title: "Lecture 21: I/O Interfacing and Data Transfer Techniques (Part 1)"
date: 2026-06-29 09:50:00 +0530
categories: jekyll update
permalink: "/lecture-21-io-interfacing-and-data-transfer-techniques-part-1/"
---

# {{ page.title | escape }}

## 1. Why is I/O Interfacing Required?

The Intel 8085 cannot directly operate devices like keyboards or printers because different devices have different operating speeds, devices use different voltage levels and communication protocols, multiple devices may be connected to the same processor. Therefore, an I/O interface acts as a bridge between the processor and external devices.

### # Functions of an I/O Interface

- Transfers data between CPU and devices.
- Matches speed differences.
- Generates control signals.
- Selects the correct device.
- Buffers data when necessary.

### # Communication Between CPU and I/O Devices

![Communication Between CPU and I/O Devices]({{ '/assets/images/Communication-Between-CPU-and-IO-Devices.png' | relative_url }})

## 2. Memory-Mapped I/O

In Memory-Mapped I/O, I/O devices are treated as memory locations. The same instructions used for memory can also access I/O devices.

### # Characteristics

- Uses the 16-bit address bus.
- Supports up to 64 KB address space.
- Any memory instruction can access an I/O device.

### # Advantages

- Large address space.
- All memory instructions can be used.
- Flexible programming.

### # Disadvantages

- Reduces available memory space.
- More complex address decoding.

## 3. I/O-Mapped (Isolated) I/O

In I/O-Mapped I/O, memory and I/O devices have separate address spaces. Special instructions (IN and OUT) are used to communicate with I/O devices.

### # Characteristics

- Uses an 8-bit port address.
- Supports 256 I/O ports.
- Memory address space remains completely available.

### # Advantages

- Memory space is preserved.
- Simple hardware.
- Easy to implement.

### # Disadvantages

- Limited to 256 ports.
- Only IN and OUT instructions can access I/O devices.
