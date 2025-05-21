# 🔩 QFN Solder Joint Reliability Simulation (ANSYS)

This repository contains the simulation workflow, models, and analysis results for evaluating the **fatigue reliability of solder joints** in a **Quad Flat No-Leads (QFN)** package under thermal cycling using **ANSYS Mechanical**.

## 📌 Project Overview

The goal of this project is to analyze the thermo-mechanical reliability of QFN solder joints by:

- Simulating thermal cycling from **−40°C to 100°C** at a ramp rate of 10°C/min.
- Evaluating three lead-free solder alloys: **SAC105**, **SAC305**, and **SAC405**.
- Comparing fatigue life and plastic deformation using **Garofalo creep** and **Syed fatigue life** models.

---

## 🛠 Tools & Technologies

- **ANSYS Mechanical (Workbench + SpaceClaim)**
- Finite Element Analysis (FEA)
- Garofalo Creep Model
- Syed Fatigue Life Prediction Model
- Thermal Cycling & Solder Joint Reliability Simulation

---

## 🧱 Package Details

| Parameter                | Value         |
|--------------------------|---------------|
| Package Type             | QFN (VQFN-48) |
| Manufacturer             | Texas Instruments |
| Part Number              | ADS1158IRTCR |
| Lead Count               | 48            |
| Solder Thickness         | 0.075 mm      |
| Die Size                 | 3.5 mm × 3.5 mm |
| Flag Size                | 5.1 mm × 5.1 mm |
| PCB Size                 | 17 mm × 17 mm |
| Materials Used           | FR-4, Copper, Overmold QFN, Silicon |

---

## 🔬 Simulation Workflow

1. **Modeling**: Created geometry in SpaceClaim as per datasheet specs.
2. **Material Assignment**: Applied appropriate thermal and mechanical properties to each component.
3. **Meshing**: Used MultiZone and sweep methods for mesh control in solder and PCB regions.
4. **Boundary Conditions**:
   - Fixed support at one vertex
   - Displacement allowed along x-z plane
5. **Thermal Cycling Setup**:
   - Two cycles: −40°C to 100°C with ramp/dwell
   - Stepwise loading and thermal profiles
6. **Fatigue Analysis**:
   - Applied **Syed model** for life prediction
   - Analyzed plastic strain, strain energy, deformation

---

## 📊 Results Summary

| Solder Alloy | Plastic Work | Cycles to Failure | Reliability |
|--------------|--------------|-------------------|-------------|
| **SAC105**   | 0.0355       | ~1726             | ★★★★☆       |
| **SAC305**   | 0.0032       | ~78               | ★★☆☆☆       |
| **SAC405**   | 0.0100       | ~3150             | ★★★★★       |

- **SAC105** showed the best balance between ductility and fatigue resistance.
- **SAC405**, while stronger due to higher Ag content, exhibited higher brittleness and strain localization.
- **SAC305** had the shortest fatigue life, making it less suitable for high-reliability environments.

---

## 🧠 Key Learnings

- Higher silver content increases strength but reduces ductility, affecting solder reliability.
- Accurate material modeling and fatigue prediction is critical in electronics packaging.
- FEA-based fatigue simulation can guide material selection for robust IC design.

---

## 📘 References

- ANSYS Training: Thermo-Mechanical Reliability of IC Packages
- Texas Instruments Datasheet: ADS1158IRTCR
- Creep and Fatigue Models: Syed, Garofalo

---

## 📧 Contact

**Aditya Saraf**  
B.Tech. | Material Science and Engineering  
IIT Kanpur  
Email: *[adityasaraf.adi15@gmail.com]*

---
