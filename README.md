# Smart-Adaptive-Traffic-Light-Controller
## 📌 Overview
This project implements a **Smart Traffic Light Controller** using **Verilog HDL** and a **Moore FSM**.  
The controller adapts its **green light duration** based on real-time **traffic density inputs**, while ensuring **safe state transitions** with **all-red intervals** to avoid collisions.  

It is verified through simulation in **Vivado** (Xilinx) and **Icarus Verilog + GTKWave**.

---

## ✨ Features
- ✅ **Adaptive timing**: Green duration increases or decreases based on 2-bit traffic density input.  
- ✅ **Moore FSM**: Stable, glitch-free outputs derived only from the current state.  
- ✅ **Safety states**: All-red intervals between transitions to prevent accidents.  
- ✅ **Verification**: Self-checking testbench with assertions (no both-green or both-yellow at the same time).  
- ✅ **Synthesizable**: Works on FPGA boards like **Basys3/Nexys A7**.  

---
## 🖥️ State Diagram
![State Diagram](docs/state_diagram.png)  

FSM cycle:  
`NS_GREEN → NS_YELLOW → ALL_RED_1 → EW_GREEN → EW_YELLOW → ALL_RED_2 → (back to NS_GREEN)`

---
