# ⚡ PCB_DC_Driver
**Single DC Motor Driver with H-Bridge Architecture**

---

<p align="center">
  <a href="https://github.com/Kolicks/PCB_DC_Driver" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-Visit%20Repo-blue?logo=github&style=for-the-badge" alt="GitHub Repo">
  </a>
</p>

---

## 📘 Overview
**PCB_DC_Driver** is a theoretical yet practical design for a **DC motor driver** built around an **H-Bridge architecture** using dedicated gate drivers.  
The project focuses on achieving an efficient, compact, and manufacturable design while following **Design for Assembly (DFA)** and **Design for Manufacturing (DFM)** principles.

<p align="center">
  <img src="images/3D.png" alt="3D Render" width="500"/>
  <br>
  <em>3D render of the finished PCB_DC_Driver board</em>
</p>

---

## ⚙️ General Information
- Theoretical **simple DC driver** implementing an **H-Bridge** with gate drivers.  
- Designed with **DFA** considerations to optimize ease of assembly and production workflow.  
- Built on **2 layers**, using **standard FR4 (TG135)** core and prepreg stackup, **1.6 mm thickness**.  

<p align="center">
  <img src="images/SCH.png" alt="Schematic" width="600"/>
  <br>
  <em>Full schematic diagram of the PCB_DC_Driver (KiCad 9)</em>
</p>

---

## 🔧 Characteristics
- Controls **one DC motor** with full H-Bridge operation.  
- Supports up to **10 A continuous current**, limited by the gate drivers and onboard fuse.  
- Operates at **24 VDC** nominal input voltage.  
- **All high-current power lanes routed on the top layer** to simplify current flow and reduce noise.  
- **All components placed on the top side**, enabling a **two-step DFA process**:  
  - Reflow soldering for SMD components.  
  - Wave soldering for through-hole parts.  
- **DFM-compliant design**:  
  - Includes multiple **mounting holes**.  
  - **Maximum PCB size:** 100 × 100 mm (optimized for **JLCPCB**).  
  - **Surface finish:** HASL (with lead).  
  - **Tented vias** for protection and manufacturing consistency.  
- **Optimized gate loop design:**  
  - Gate drivers positioned close to MOSFETs to minimize loop inductance.  
  - Bottom ground layer cleared in high-current paths to ensure controlled current direction and reduce EMI/EMC issues.
- **Space between MOSFET**: For a 20x15 Mounted radiators space. 
- **Microcontroller:** Reused **STM32F030K6T6** from previous projects for convenience, reusability, and familiarity with existing firmware.

<p align="center">
  <img src="images/" alt="PCB Layout" width="600"/>
  <br>
  <em>Top layer routing and overall PCB layout (KiCad 9)</em>
</p>

---

## ⚠️ Design Notes
- Power paths designed with proper copper width for 10 A continuous load capability.  
- Ground and power planes isolated to improve switching behavior and minimize noise coupling.  
- Routing and layout optimized for **EMI/EMC performance**.  
- Designed for **expandability**, allowing integration of PWM control, fault sensing, or current feedback in future iterations.  

---

## 🧩 Repository Structure
