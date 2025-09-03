# ⚙️ Parallel Extruder Head for Fiber-Reinforced 3D Printing

This repository contains the firmware and design files for a specialized, custom-built extruder head developed for the 3D printing of **fiber-reinforced objects**. This project is inspired by the **Markforged concept** and uses a parallel component arrangement to create a unique and compact extrusion solution. The ultimate goal was to print objects strengthened with coated carbon fibers to achieve higher material strength.

![Custom Parallel Extruder Head](https://github.com/Pyrius2k/Additive-Manufacturing/raw/main/Druckkopf.png)

## ✨ Project Overview

The aim of this project was to design a lightweight, custom extruder head for 3D printing that allows the use of fiber-reinforced materials.

* **Fiber Reinforcement:** The design is specifically optimized to process **coated carbon fibers**.
* **Stepper & Servo:** The integration of stepper and servo motors enables precise control over the extrusion and fiber feeding process. The **servo motor has a sharp object attached to it to cut the fiber** at the end of a print section, a core feature inspired by the Markforged concept.
* **Lightweight Construction:** The configuration aims to reduce mass to improve print speed and accuracy.

---

## 📁 Repository Contents

* **`Druckkopf.png`**: A render of the specially designed extruder head.
* **`Servo.ino`**: A standalone Arduino sketch for basic servo testing.
* **`StepperMotor-Basic.ino`**: A standalone Arduino sketch for basic stepper motor testing.
* **`/Marlin-Firmware/`**: A folder containing the modified Marlin firmware files. The core logic for controlling the motors is integrated here. *(Note: You will need to upload this folder and its files to the repository)*

---

## 💻 Firmware Integration (Marlin)

The core functionality of this extruder is achieved by modifying the open-source **Marlin firmware**. The provided `Servo.ino` and `StepperMotor-Basic.ino` sketches represent the key control logic that has been adapted and integrated into the main Marlin codebase to operate the parallel extruder.

**Key firmware modifications include:**

* Custom pin definitions for the servo and stepper drivers.
* Logic for controlling the servo's position to cut the fiber during specific G-code commands.
* Pulse generation for the stepper motors for precise fiber feeding.

---

## 🛠️ How to Use

To replicate this project, you will need to:

1.  **Assemble the Hardware:** Mount the stepper motors, servos, and fans to the printed parts.
2.  **Flash the Firmware:** Upload the customized Marlin firmware to your 3D printer's mainboard.
3.  **Calibrate:** Perform the necessary calibration steps for the extruder.

---

This video explains the basics of reinforcing 3D prints with carbon fiber.
<br>
[How to reinforce your 3D prints with carbon fiber.](https://www.youtube.com/watch?v=BATPn2OY-4I)
