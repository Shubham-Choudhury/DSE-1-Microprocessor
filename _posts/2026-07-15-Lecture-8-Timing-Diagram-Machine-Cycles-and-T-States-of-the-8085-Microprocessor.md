---
layout: base
title: "Lecture 8: Timing Diagram, Machine Cycles, and T-States of the 8085 Microprocessor"
date: 2026-06-29 09:50:00 +0530
categories: jekyll update
permalink: "/lecture-8-timing-diagram-machine-cycles-and-t-states-of-the-8085-microprocessor/"
---

# {{ page.title | escape }}

## 1. Clock Signal

A clock signal is a continuous sequence of electrical pulses that synchronizes all operations inside the microprocessor.

### # Clock Waveform

![Clock Waveform]({{ '/assets/images/Clock-Waveform.png' | relative_url }})

## 2. Clock Frequency

Clock frequency is the number of clock pulses generated in one second.

Unit:`Hertz (Hz)`

#### **Examples:**

| Frequency | Meaning                         |
| --------- | ------------------------------- |
| 1 Hz      | 1 pulse per second              |
| 1 kHz     | 1,000 pulses per second         |
| 1 MHz     | 1,000,000 pulses per second     |
| 1 GHz     | 1,000,000,000 pulses per second |

In 8085 microprocessor typical clock frequency is 3 MHz. This means approximately 3,000,000 clock pulses every second.

## 3. What is a T-State?

A T-State (Timing State) is the smallest unit of time in the operation of a microprocessor. One T-state corresponds to one clock pulse.

### # Duration of One T-State

The duration of one T-state depends on the clock frequency.

Formula:

$$\text{Time for one T-State} = \frac{1}{\text{Clock Frequency}}$$

#### Example:

Clock Frequency = $\text{3 MHz}$

$$\text{T} = \frac{1}{\text{3000000}}$$

$$\text{T} = 0.333 \mu\text{s}$$

## 4. What is a Machine Cycle?

A Machine Cycle is the time required to complete one basic operation such as Fetching an instruction, Reading from memory, Writing to memory, Reading from an I/O device, Writing to an I/O device. A machine cycle consists of one or more T-states.

### # Types of Machine Cycles in 8085 Microprocessor

The 8085 Microprocessor uses five major machine cycles:

| Machine Cycle | Purpose                   |
| ------------- | ------------------------- |
| Opcode Fetch  | Fetch instruction         |
| Memory Read   | Read data from memory     |
| Memory Write  | Write data to memory      |
| I/O Read      | Read from an input device |
| I/O Write     | Write to an output device |

## I. Opcode Fetch Cycle

The Opcode Fetch Cycle is the first machine cycle of every instruction.

The processor:
1. Places the instruction address on the Address Bus.
2. Activates the RD signal.
3. Reads the opcode from memory.
4. Decodes the instruction.

Opcode Fetch usually requires 4 to 6 T-States. Most simple instructions use 4 T-states for the opcode fetch.

![Opcode Fetch Sequence]({{ '/assets/images/Opcode-Fetch-Sequence.png' | relative_url }})

### # Timing Diagram of Opcode Fetch

![Timing Diagram of Opcode Fetch]({{ '/assets/images/Timing-Diagram-of-Opcode-Fetch.png' | relative_url }})

## II. Memory Read Cycle

Used when the processor reads data (not an instruction) from memory. Memory Read Cycle Usually requires 3 T-States.

### # Memory Read Timing Diagram

![Memory Read Timing Diagram]({{ '/assets/images/Memory-Read-Timing-Diagram.png' | relative_url }})

Steps:
1. Address 3000H placed on Address Bus.
2. RD becomes LOW.
3. Memory places data on Data Bus.
4. Processor stores the data.

## III. Memory Write Cycle

Used when data is stored into memory. Memory Write Cycle Usually requires 3 T-States.

Sequence
1. Address placed on Address Bus.
2. Data placed on Data Bus.
3. WR becomes LOW.
4. Memory stores the data.

### # Memory Write Timing Diagram

![Memory Write Timing Diagram]({{ '/assets/images/Memory-Write-Timing-Diagram.png' | relative_url }})

## IV. I/O Read Cycle

Used when reading data from an input device.

## V. I/O Write Cycle

Used when sending data to an output device.

## 5. What is an Instruction Cycle?

An Instruction Cycle is the total time required to complete an instruction. An instruction cycle may consist of One machine cycle or Two machine cycles or Three machine cycles or more machine cycles, depending on the instruction.

### # Relationship Between T-State, Machine Cycle, and Instruction Cycle

![Relationship Between T-State, Machine Cycle, and Instruction Cycle]({{ '/assets/images/Relationship-Between-T-State-Machine-Cycle-and-Instruction-Cycle.png' | relative_url }})

| Unit              | Description                               |
| ----------------- | ----------------------------------------- |
| Clock Pulse       | One electrical pulse                      |
| T-State           | One clock period                          |
| Machine Cycle     | Group of T-states for one basic operation |
| Instruction Cycle | Complete execution of one instruction     |
