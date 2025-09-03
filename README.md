⚙️ Parallel Extruder Head for Fiber-Reinforced 3D Printing
This repository contains the firmware and design files for a specialized, custom-built extruder head developed for the 3D printing of fiber-reinforced objects. This project is inspired by the Markforged concept and uses a parallel component arrangement to create a unique and compact extrusion solution. The ultimate goal was to print objects strengthened with coated carbon fibers to achieve higher material strength.

✨ The Basic Concept
This image illustrates the core concept behind the work: the integration of a separate unit for the extrusion of coated carbon fibers alongside a standard filament extruder.

<br>
<img src="https://www.google.com/search?q=https://github.com/Pyrius2k/Additive-Manufacturing/raw/main/concept.png" alt="Basic concept of the project" width="650">

<br>

🔬 Goal and Project Overview
The main objective of this project was to significantly increase the tensile strength of 3D-printed objects by using coated carbon fibers. The developed extruder head is specifically designed to process this material.

Fiber Reinforcement: The design is optimized to precisely process coated carbon fibers.

Stepper & Servo: The stepper motors ensure accurate fiber extrusion, while the servo motor has a sharp object attached to it to cut the fiber at the end of a print section, a core feature inspired by the Markforged concept.

Lightweight Construction: The configuration aims to reduce mass to improve print speed and accuracy.

🛠️ Design and Slicing Integration
The extruder head was designed to allow for the dual extrusion of both plastic (PLA) and carbon fibers. The slicer software is configured to strategically place the fibers in specific paths to achieve maximum strength.

<br>
<img src="https://github.com/Pyrius2k/Additive-Manufacturing/raw/main/Druckkopf.png" alt="Render of the extruder head" width="500">
<img src="https://www.google.com/search?q=https://github.com/Pyrius2k/Additive-Manufacturing/raw/main/curapic.png" alt="Slicer view in Cura" width="500">

<br>

The second image shows a slicer view of a tensile test specimen with the embedded carbon fiber paths, which were designed to be printed for strength testing.

📁 Repository Contents
concept.png: A schematic representation of the basic concept.

Druckkopf.png: A render of the specially designed extruder head.

curapic.png: A slicer view of the fiber paths in a test object.

Servo.ino: A standalone Arduino sketch for basic servo testing.

StepperMotor-Basic.ino: A standalone Arduino sketch for basic stepper motor testing.

/Marlin-Firmware/: A folder containing the modified Marlin firmware files. (Note: You will need to upload this folder and its files to the repository)

💻 Firmware Integration (Marlin)
The core functionality of this extruder is achieved by modifying the open-source Marlin firmware. The provided Servo.ino and StepperMotor-Basic.ino sketches represent the key control logic that has been adapted and integrated into the main Marlin codebase to operate the parallel extruder.

Key firmware modifications include:

Custom pin definitions for the servo and stepper drivers.

Logic for controlling the servo's position to cut the fiber during specific G-code commands.

Pulse generation for the stepper motors for precise fiber feeding.

🛠️ How to Use
To replicate this project, you will need to:

Assemble the Hardware: Mount the stepper motors, servos, and fans.

Flash the Firmware: Upload the customized Marlin firmware to your 3D printer's mainboard.

Calibrate: Perform the necessary calibration steps for the extruder.

This video explains the basics of reinforcing 3D prints with carbon fiber.
<br>
How to reinforce your 3D prints with carbon fiber.
