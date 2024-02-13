# Digital Hockey Game - CS-303 Logic and Digital System Design Final Project

## Overview
This repository contains the Verilog code for a digital hockey game, developed as the final project for the CS-303 Logic and Digital System Design course. The project simulates a hockey game using buttons for player inputs, LEDs to represent the puck's position, and seven-segment displays (SSDs) to show the scores and game states. This game demonstrates the application of digital logic and state machine concepts in creating interactive digital systems.

## Team Members
- Doğukan
- Ayça 

## Project Structure
- `hockey.v`: Core game logic, including player interactions, puck movement, scoring, and game state management.
- `top_module.v`: Interfaces the physical inputs/outputs with the game logic. Includes clock division, button debouncing, and module instantiation.
- `ssd.v`: Controls the seven-segment displays, showing game-related information such as scores.
- `debouncer.v`: Filters mechanical noise from button presses to ensure clean input signals.
- `[Project Name].xdc`: Xilinx Design Constraints file for mapping FPGA pins to the Verilog design inputs and outputs.

## Features
- Button debouncing for reliable player input.
- Dynamic LED display to represent the puck's position on the field.
- SSD-based score and game state display.
- Modular design for easy understanding and modification.

## Dependencies
- A Verilog-compatible simulation or synthesis tool (e.g., Xilinx Vivado, ModelSim).
- FPGA board or simulation environment for deployment and testing.

## Setup and Running
1. **Clone the repository:**
2. **Open the project in your Verilog development environment.**
3. **Compile and synthesize the Verilog files.**
4. **Deploy the synthesized design to your FPGA board or run the simulation in your development environment.**
5. **Ensure the XDC file is correctly configured for your specific FPGA board model and pin layout.**
6. **Integrate the `debouncer` module for button inputs in the `top_module` to utilize clean signals for game logic.**

## Controls
- **BTN_A**: Player A's button for hitting the puck.
- **BTN_B**: Player B's button for hitting the puck.
- **DIR_A** and **DIR_B**: Direction inputs for controlling the puck's movement.
- **YA** and **YB**: Y-coordinate inputs for Player A and B's positions.

## Xilinx Design Constraints (XDC) File
The XDC file specifies the package pin, I/O standard, and port name for each input/output used in the project. It is crucial for the correct interfacing with the FPGA board.

## Debouncer Module
The `debouncer` module ensures that each button press is registered as a single, clean input signal, preventing multiple triggers for a single press.

## Acknowledgements
This project was developed as part of the coursework for CS-303 Logic and Digital System Design at Sabanci University. We express our gratitude to our instructor Atıl Utku Ay for their guidance and support throughout the course.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
