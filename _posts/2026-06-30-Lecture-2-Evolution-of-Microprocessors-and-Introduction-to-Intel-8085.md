---
layout: base
title: "Lecture 2: Evolution of Microprocessors and Introduction to Intel 8085"
date: 2026-06-29 09:50:00 +0530
categories: jekyll update
permalink: "/lecture-2-evolution-of-microprocessors-and-introduction-to-intel-8085/"
---

# {{ page.title | escape }}

## 1. Why Did Microprocessors Evolve?

The first microprocessors were designed for simple tasks such as basic calculations. As technology advanced, users demanded computers that were:

- Faster
- More powerful
- Able to process larger amounts of data
- Capable of multitasking
- More energy-efficient
- Smaller and less expensive

To meet these demands, manufacturers continually improved microprocessor designs.

## 2. Timeline of Microprocessor Evolution

![Timeline of Microprocessor Evolution]({{ '/assets/images/Timeline-of-Microprocessor-Evolution.png' | relative_url }})

## Word Length

The word length of a processor indicates the number of bits it can process in a single operation.

Examples:

- 4-bit processor → Processes 4 bits at a time
- 8-bit processor → Processes 8 bits at a time
- 16-bit processor → Processes 16 bits at a time
- 32-bit processor → Processes 32 bits at a time
- 64-bit processor → Processes 64 bits at a time

## 3. First Generation of Microprocessors – Intel 4004 (1971)

The Intel 4004 was the world's first commercially available microprocessor.

### Features

- 4-bit processor
- Approximately 2,300 transistors
- Clock speed around 740 kHz
- Could execute about 92,000 instructions per second
- Originally developed for calculators

### Advantages

- Small size
- Lower cost than previous CPU designs
- Reduced power consumption

### Limitations

- Very limited processing power
- Could not support complex applications
- Small memory capacity

## 4. Intel 8008 (1972)

Intel introduced the 8008 as an improvement over the 4004.

### Features

- 8-bit processor
- Larger instruction set
- Higher speed
- More memory support

## 5. Intel 8080 (1974)

The Intel 8080 became one of the first successful general-purpose microprocessors.

### Features

- 8-bit data bus
- 16-bit address bus
- Can access 64 KB of memory
- Faster clock speed
- Richer instruction set

### Applications

- Early personal computers
- Industrial control systems
- Embedded devices

## 6. Major Features of Intel 8085

| Feature         | Description         |
| --------------- | ------------------- |
| Word Length     | 8-bit               |
| Address Bus     | 16-bit              |
| Data Bus        | 8-bit               |
| Maximum Memory  | 64 KB               |
| Clock Frequency | Approximately 3 MHz |
| Number of Pins  | 40                  |
| Technology      | NMOS                |
| Power Supply    | +5 V                |

### # Why Is It Called an 8-Bit Processor?

The Intel 8085 processes 8 bits of data at a time.

#### **Example:**

Suppose:

```
A = 11001010
```

The entire 8-bit value is processed in one operation. A 4-bit processor would require two operations to process the same amount of data.

## 7. Memory Addressing in Intel 8085

The Intel 8085 has a 16-bit address bus. A 16-bit address bus can generate: $ 2^{16} =65,536 $ addresses.

Since:

$$
1 KB = 1024 bytes
$$

$$
65,536 bytes=64 KB
$$

Therefore, the Intel 8085 can access 64 KB of memory.

### Data Bus vs Address Bus

| Data Bus             | Address Bus                |
| -------------------- | -------------------------- |
| Transfers data       | Transfers memory addresses |
| 8 bits               | 16 bits                    |
| Bidirectional        | Unidirectional             |
| Determines data size | Determines memory capacity |
