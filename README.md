# FSM Sequence Detector (1010) using Cadence Virtuoso

This project implements a **4-bit sequence detector** designed to detect the binary sequence **1010** using a **Mealy Finite State Machine (FSM)** in **Cadence Virtuoso**. The FSM is designed with overlapping sequence detection, which allows it to detect consecutive occurrences of the sequence without missing any bits.

The FSM is realized using **True Single Phase Clock (TSPC) D Flip-Flops**, chosen for their **high-speed operation and low-power consumption**, making them ideal for fast digital circuits. The Mealy machine model is employed, so the output Y responds immediately to the input sequence, providing faster detection compared to a Moore FSM.

The design process involved deriving the **next-state logic and output equations** using truth tables and K-map simplification. The schematic was implemented in Cadence Virtuoso, and simulation was performed using Spectre to verify correct functionality. **Transient analysis** confirmed that the FSM correctly detects the 1010 sequence and produces overlapping outputs where applicable.

This project demonstrates not only the principles of FSM design and sequential logic but also the practical application of TSPC D Flip-Flops for high-performance digital circuits, giving hands-on experience in VLSI design and verification.

---

## 🔧 Project Description

- Detects binary sequence: **1010**
- FSM Type: **Mealy**
- Implemented using logic derived from truth tables and K-maps
- Constructed using **TSPC D flip-flops**
- Simulated using **Spectre** in **Cadence Virtuoso**
- Verified with **transient and DC analysis**

---

## 🧠 FSM Design Summary

- **States**: S0 → S1 → S2 → S3 → S4 (using 2 flip-flops)
- **Output Y** becomes `1` when sequence `1010` is detected
- **D1, D0, and Y** expressions derived using Boolean minimization

---

# BLOCK DIAGRAM
![image](https://github.com/user-attachments/assets/709173a8-7407-414f-b190-0115385916b6) 

## 🛠️ Project Contents

| Image Preview | Description |
|---------------|-------------|
| [📷 FSM Schematic](images/schematic.jpg) | FSM logic schematic |
| [📷 TSPC D Flip-Flops](images/TSPC_D_flip-flops_Schematic.png) | TSPC D flip-flops schematic |
| [📷 Symbol View](images/symbol_view.jpg) | Custom symbol created for FSM |
| [📷 Testbench](images/testbench.jpg) | Testbench schematic with clock and input |
| [📷 Waveform Output](images/waveform_output.jpg) | Simulation waveform showing detection |
| [📷 State Diagram](images/state_diagram.jpg) | FSM state diagram |
| [📷 Truth Table + K-Map](images/truth_table_kmap.jpg) | Truth table and K-map simplification |
| [📷 Boolean Equations](images/Boolean_equations_truth_table.jpg) | Boolean logic equations |


---

## 🧪 Simulation Setup

### 🔁 Clock Source (VPULSE)
| Parameter      | Value         |
|----------------|---------------|
| V1 (Low)       | 0V            |
| V2 (High)      | 1.8V          |
| Period         | 50s           |
| Pulse Width    | 25s           |

### 🔁 Input Pulse (VPULSE)
| Parameter      | Value         |
|----------------|---------------|
| V1 (Low)       | 0V            |
| V2 (High)      | 1.8V          |
| Period         | 50s           |
| Pulse Width    | 25s           |

### 🔋 VDC Supply
| Parameter      | Value         |
|----------------|---------------|
| DC Voltage     | 1.8V          |

---

## ✅ Output Verification

- The output **Y** goes HIGH as soon as the sequence `1010` is detected.
- Simulation waveform confirms correct FSM behavior.


---

## ⚙️ Tools Used

- **Cadence Virtuoso 6.1.8**
- **Spectre** (for transient & DC analysis)
- **Linux** environment

---

## 🧠 Insights Gained

- FSM Design (Mealy machine)
- K-map simplification for logic expressions
- Schematic and Symbol creation in Cadence
- Transient simulation and waveform analysis
- Working with **TSPC D flip-flops** for low-power, high-speed design

---
## 🔮 Future Work

- Add layout view with DRC/LVS verification  
- Include power and delay analysis using Spectre  
- RTL version in Verilog for FPGA comparison  
- Implement using FinFET PDK for scaled power analysis

## ✍️ Author

**SURIYA R K - BE EEE**   

---




