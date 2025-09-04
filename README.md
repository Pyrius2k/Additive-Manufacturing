# ⚙️ Parallel Extruder Head for Fiber-Reinforced 3D Printing

This repository contains the firmware and design files for a custom-built extruder head designed for the 3D printing of fiber-reinforced objects. Inspired by the **Markforged concept**, this project features a **parallel extruder system** capable of handling both standard filament and **coated carbon fibers**, enabling the creation of high-strength composite prints.

---

## ✨ Project Concept

The image below illustrates the core concept: an integrated dual-extrusion head—one for standard filament and another for coated carbon fibers.

<div align="center">
  <img src="https://github.com/Pyrius2k/Additive-Manufacturing/raw/main/concept.png" width="500">
</div>

---

## 🎯 Project Goals

The primary objective of this project is to significantly improve the **tensile strength** of 3D-printed parts by embedding continuous or segmented carbon fibers into the print path.

### ✅ Key Features:

- **Fiber Reinforcement**: Optimized for extruding coated carbon fibers alongside PLA.
- **Precision Mechanics**:  
  - **Stepper Motor** for accurate fiber feeding  
  - **Servo Motor** with a sharp blade to cut fiber segments after each print section
- **Lightweight Design**: Carefully engineered to reduce head weight for faster, more accurate prints.

---

## 🛠️ Design Overview & Slicer Integration

The extruder is fully integrated with slicing software (e.g., Cura) to allow for **strategic fiber placement** in designated toolpaths—particularly useful for structural parts like **tensile test specimens**.

<div align="center">
  <img src="https://github.com/Pyrius2k/Additive-Manufacturing/raw/main/Druckkopf.png" width="450">
  <br><em>3D Render of the Custom Extruder Head</em>
</div>

<br>

<div align="center">
  <img src="https://github.com/Pyrius2k/Additive-Manufacturing/raw/main/curapic.png" width="500">
  <br><em>Slicer View Showing Embedded Carbon Fiber Paths</em>
</div>

---

## 📁 Repository Contents

| File | Description |
|------|-------------|
| `concept.png` | Diagram showing the basic extruder layout |
| `Druckkopf.png` | Render of the extruder head CAD design |
| `curapic.png` | Screenshot from Cura showing fiber paths |
| `Servo.Code.ino` | Arduino sketch for servo cutting control |
| `Stepper_Code.ino` | Arduino sketch for stepper motor control |
| `Marlin.confi.ino/` | Folder containing modified Marlin firmware for parallel extrusion setup |

---

## 💻 Firmware Integration (Marlin)

The extruder head's functionality is achieved by **modifying Marlin firmware** to handle an additional fiber-feeding stepper and servo-controlled cutter.

### 🔧 Firmware Modifications:

- Custom **pin assignments** for stepper and servo control
- G-code logic to trigger servo cutting at specific layers or regions
- Pulse generation and timing control for stepper fiber extrusion
- Optionally triggered by `M` or `G` commands for precise control

---

## 🚀 Getting Started

To replicate or build upon this project:

1. **Assemble the Hardware**  
   Mount stepper motors, servo, and any cooling elements according to your frame design.

2. **Flash the Firmware**  
   Upload the provided modified Marlin firmware to your 3D printer’s control board.

3. **Calibration & Testing**  
   - Run the `Stepper_Code.ino` and `Servo.Code.ino` sketches for initial tests  
   - Adjust motor direction, cutting angles, and fiber feed rates

---

## 📌 Notes

- Fiber placement currently requires manual G-code or custom post-processing
- The servo cutter blade can be replaced or upgraded depending on fiber type
- Print cooling should be adjusted to accommodate carbon fiber heat retention

---

## 🤝 Contributions

Ideas, suggestions, and PRs are welcome—whether it’s for improving slicing strategies, mechanical enhancements, or smarter firmware logic.

---

## 📜 License

This project is open-source under the MIT License. Feel free to adapt, remix, and build upon the work.

