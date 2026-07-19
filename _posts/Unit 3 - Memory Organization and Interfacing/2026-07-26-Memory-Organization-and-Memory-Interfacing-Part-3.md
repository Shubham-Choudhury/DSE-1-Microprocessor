---
layout: base
title: "Lecture 19: Memory Organization and Memory Interfacing (Part 3)"
date: 2026-06-29 09:50:00 +0530
categories: jekyll update
permalink: "/lecture-19-memory-organization-and-memory-interfacing-part-3/"
---

# {{ page.title | escape }}

## 1. Communication Between the Microprocessor and Memory

The 8085 microprocessor communicates with memory using three buses:

![Communication Between the Microprocessor and Memory]({{ '/assets/images/Communication-Between-the-Microprocessor-and-Memory.png' | relative_url }})

## 2. Memory Read Cycle

A Memory Read Cycle is the sequence of operations performed when the processor reads data from memory.

### **Step 1:**

Processor places the address on the address bus.

### **Step 2:**

ALE becomes HIGH. Lower address is latched.

### **Step 3:**

Processor activates RD̅ = 0 and memory understands READ requested.

### **Step 4:**

Memory places data on the data bus.

### **Step 5:**

Processor receives data.

### **Step 6:**

RD̅ returns HIGH and memory releases the data bus.

## 3. Memory Write Cycle

A Memory Write Cycle stores data into memory.

### **Step 1:**

Processor places address on address bus.

### **Step 2:**

ALE stores lower address.

### **Step 3:**

Processor places data.

### **Step 4:**

Processor activates WR̅ = 0 and memory stores data.

### **Step 5:**

WR̅ becomes HIGH. Write operation ends.

## 4. READY Signal

The READY signal indicates whether the memory device is ready for data transfer. If READY = 1 then processor continues normally.
If READY = 0, memory is slow, processor waits.

## 5. Wait State

A Wait State is an extra clock cycle inserted when memory is too slow to respond.
