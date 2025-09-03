# ⚙️ Parallel Extruder Head for 3D Printers

This repository contains the firmware and design files for a custom-built parallel extruder head, specifically developed for a 3D printer. This project integrates both servo and stepper motor control to achieve a unique, compact extrusion system.

![Custom Parallel Extruder Head](https://github.com/Pyrius2k/Additive-Manufacturing/raw/main/Druckkopf.png)

## ✨ Project Overview

The goal of this project was to design and build a lightweight, custom extruder head that utilizes a parallel arrangement of components. The design includes:

* **Stepper Motors:** For precise control of filament extrusion.
* **Servos:** Integrated to control specific movements or functions.
* **Custom-Printed Parts:** All components are designed to be 3D printed for easy replication.

This project is a great resource for anyone interested in advanced 3D printer modifications, custom firmware, or mechatronics.

---

## 📁 Repository Contents

* **`Druckkopf.png`**: A render of the custom-designed extruder head.
* **`Servo.ino`**: Standalone Arduino sketch for basic servo testing.
* **`StepperMotor-Basic.ino`**: Standalone Arduino sketch for basic stepper motor testing.
* **`/Marlin-Firmware/`**: A folder containing the modified Marlin firmware files. The core logic for the servo and stepper motor control is integrated here. *(Note: You would need to add this folder and its files to your repository)*
* **`/CAD-Files/`**: A folder containing the 3D design files for the extruder parts in `.stl`, `.dwg`, or other formats. *(Note: You would need to add this folder and its files to your repository)*

---

## 💻 Firmware Integration (Marlin)

The core functionality of this extruder is managed by modifying the open-source **Marlin firmware**. The provided `Servo.ino` and `StepperMotor-Basic.ino` sketches represent the key control logic that has been adapted and integrated into the main Marlin code base to operate the parallel extruder.

**Key firmware modifications include:**

* Custom pin definitions for the servo and stepper drivers.
* Logic for controlling the servo's position during specific G-code commands.
* Step/direction pulse generation for the stepper motors.

---

## 🛠️ How to Use

To replicate this project, you will need to:

1.  **Print the Parts:** 3D print all the components from the CAD files.
2.  **Assemble the Hardware:** Mount the stepper motors, servos, and fans to the printed parts.
3.  **Flash the Firmware:** Upload the custom Marlin firmware to your 3D printer's mainboard.
4.  **Calibrate:** Perform the necessary calibration steps for the extruder.

---

**You can replace the placeholder text and URLs with your actual information.** For instance, change `YourUsername` and `YourRepoName` to your own details, and remember to add the referenced files and folders to your repository.
