# DEUARC (Electronic Universal Automatic Reduced Computer)

This project is a custom-designed basic computer architecture called **DEUARC**, developed and synthesized using **Altera Quartus II**. The design implements a complete processing unit with a dedicated instruction set, control logic, and a common bus system.

## 🚀 Architecture Overview

DEUARC is built with a modular approach, integrating several core components to execute complex machine-level instructions:

* **Processing Power:** 9 dedicated registers (including AR, PC, SP, IR, INPR, OUTPR, and R0-R2) and a custom Arithmetic Logic Unit (ALU).
* **Memory Units:** * **Instruction Memory:** 32x11 bits for storing program machine code.
  * **Data Memory:** 16x4 bits for operand storage.
  * **Stack Memory:** 16x5 bits for subroutine management (PUSH/POP operations).
* **Control Unit:** A hardwired control logic that decodes instructions using a 4x16 decoder and a sequence counter (SC) to manage the data path.

## 🛠 Arithmetic Logic Unit (ALU) Operations

The ALU is the heart of DEUARC, supporting 4-bit operations selected via input controls:
* **Arithmetic:** ADD (Addition), INC (Increment), DBL (Double), DBT (Divide by 2).
* **Logic:** AND, XOR, NOT (Complement).
* **Flags:** Supports an **Overflow (V)** flag for arithmetic monitoring.

## 📜 Instruction Set Architecture (ISA)

The computer supports a diverse set of instructions categorized as:
1. **Data Transfer:** `LD` (Load from memory), `ST` (Store to memory), `IO` (Input/Output transfer), `TSF` (Transfer between registers).
2. **Program Control:** `JMP` (Unconditional/Conditional Jump), `CAL` (Subroutine Call - Push PC), `RET` (Return from Subroutine - Pop PC), and `HLT` (Halt).
3. **Arithmetic/Logic:** Operations directly mapped to the ALU functions.

## ⚙️ How to Open and Simulate

1. **Software:** Open the project in **Altera Quartus II**.
2. **Design Files:** Review the `.bdf` (Block Diagram Files) for the top-level DEUARC integration.
3. **Compilation:** Run the synthesis to check the logic element usage on the target FPGA.
4. **Verification:** Use the **Vector Waveform File (VWF)** to simulate execution and verify signal transitions across the common bus.

---

**Project Team:** Atakan Kahraman, Olcay Karahasan, Alp Kaya, Emre Altundal 
**Course:** CME 2206 Computer Architecture Lab  
**Institution:** Dokuz Eylül University, Department of Computer Engineering
