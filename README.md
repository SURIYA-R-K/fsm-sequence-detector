# FSM Sequence Detector (110) using Cadence Virtuoso

This project implements a 3-bit sequence detector (detecting `110`) using a **Mealy Finite State Machine (FSM)** in **Cadence Virtuoso**.  
The FSM is built using **True Single Phase Clock (TSPC) D Flip-Flops** for high-speed performance.

---

## 🔧 Project Description

- Detects binary sequence: **110**
- FSM Type: **Mealy**
- Implemented using logic derived from truth tables and K-maps
- Constructed using **TSPC D flip-flops**
- Simulated using **Spectre** in **Cadence Virtuoso**
- Verified with **transient and DC analysis**

---

## 🧠 FSM Design Summary

- **States**: S0 → S1 → S2 → S3 (using 2 flip-flops)
- **Output Y** becomes `1` when sequence `110` is detected
- **DA, DB, and Y** expressions derived using Boolean minimization

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
| V2 (High)      | 1V            |
| Period         | 2ns           |
| Rise/Fall Time | 50ps          |
| Pulse Width    | 1ns           |

### 🔁 Input Pulse (VPULSE)
| Parameter      | Value         |
|----------------|---------------|
| V1 (Low)       | 0V            |
| V2 (High)      | 1V            |
| Period         | 6ns           |
| Rise/Fall Time | 50ps          |
| Pulse Width    | 1ns           |
| Delay          | 500ps         |

### 🔋 VDC Supply
| Parameter      | Value         |
|----------------|---------------|
| DC Voltage     | 1V            |

---

## ✅ Output Verification

- The output **Y** goes HIGH as soon as the sequence `110` is detected.
- Simulation waveform confirms correct FSM behavior.

---

## 📸 Screenshots

| FSM Schematic | Waveform Output |
|---------------|-----------------|
| (![image](https://github.com/user-attachments/assets/c34ae955-dfd3-4eef-b359-3451f7a666b9) | (![image](https://github.com/user-attachments/assets/9a794a1b-83e0-4455-8fba-b435a4ad085f) |

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




