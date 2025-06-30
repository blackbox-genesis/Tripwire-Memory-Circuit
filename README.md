# Tripwire Memory Logic Circuit

This is one of the most advanced genetic logic circuits I’ve built so far.  
It combines memory, logic gating, and reset into a single design — kind of like a finite state machine (FSM), but built from genes, not silicon.

The system works like a **tripwire**: one input flips memory ON, another triggers output *only if* memory is active. Then after some time, memory fades — making the circuit respond only once unless retriggered.

---

## What This Project Shows

- **Genetic memory** using AraC (triggered by IPTG)
- **AND logic gate** with memory + real-time signal (AraC + AHL → GFP)
- **Self-latching feedback loop**
- **Output that depends on both sequence and timing**
- A timed **reset** as AraC decays

---

## 📁 Circuit Modules

### **Module A - Memory Switch (IPTG -> AraC)**
Simulates how IPTG turns on memory (AraC), which stays ON after induction.

### **Module B - AND Gate Logic (AraC + AHL -> GFP)**
Basic logic gate. GFP only appears if memory is latched **and** AHL is present.

### **Module C - Self-Latching Memory (AraC -> AraC)**
AraC activates itself after a trigger. This module helps understand persistent memory.

### **Integrated System - Tripwire Logic**
- IPTG flips memory ON  
- AHL triggers output only if memory is present  
- After a while, memory decays → circuit resets itself

---

## 📊 Graphs

Each module and the final circuit include plotted outputs (time vs concentration) to show exactly when and why each part activates. They're easy to follow and meant to feel visual and logical.

---

## 🛠 Tools Used

- **Python + Tellurium**  
- Antimony modeling syntax  
- roadrunner simulations  
- matplotlib for plotting

Everything’s clean, modular, and meant to be understandable if you're into synthetic biology or just curious about how logic can be done with genes.

---

## Author Notes

This circuit was designed as a capstone to my self-taught synthetic biology modeling sprint before formally starting my undergraduate program. It represents a transition from basic logic gates to complex, state-dependent genetic memory systems and is part of a broader effort to build publishable, simulation-driven synthetic circuits from scratch.
