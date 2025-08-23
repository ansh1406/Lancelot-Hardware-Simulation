# Lancelot-m1: 16-bit CPU in Logisim Evolution

## Overview
Lancelot-m1 is a fully custom 16-bit CPU designed and implemented in Logisim Evolution. All components are built from scratch using only basic logic gates (AND, OR, NOT, XOR), demonstrating a deep understanding of digital design principles.

## Features
- **16-bit Architecture:** All data paths, registers, and operations are 16 bits wide.
- **Custom Components:** Every part of the CPU, including the ALU, registers, and control unit, is constructed from basic gates—no pre-built Logisim components are used.
- **Registers:**
  - 4 General Purpose Registers (GPRs)
  - 1 Flags Register (for status flags like zero, carry, etc.)
  - 1 Memory Address Register (MAR)
  - 1 Instruction Register (IR)
  - 1 Keyboard Register (for input)
- **Input/Output:**
  - Input is received from a keyboard component.
  - Output is displayed on a TTY display, supporting ASCII characters up to 127.
- **Microcode-Based Control Unit:**
  - The control unit uses microcode to manage instruction execution, allowing for flexible and extensible instruction sets.
- **Single Bus Architecture:**
  - A single bus is used for both address and data, simplifying the design and demonstrating bus multiplexing.

## Components
- **ALU (Arithmetic Logic Unit):** Performs arithmetic and logical operations using only basic gates.
- **Registers:** All registers are custom-built using flip-flops and gates.
- **Control Unit:** Implements instruction decoding and sequencing via microcode ROM.
- **Memory:** RAM and ROM modules for program and data storage.
- **Keyboard Interface:** Accepts input from a simulated keyboard.
- **TTY Display:** Outputs ASCII characters to a terminal display.

## How It Works
1. **Instruction Fetch:** The CPU fetches instructions from memory using the MAR and IR.
2. **Decode & Execute:** The control unit decodes instructions and generates control signals via microcode.
3. **Data Movement:** All data and addresses are transferred over a single shared bus.
4. **I/O Operations:** Keyboard input is read into the keyboard register; output is sent to the TTY display.

## Usage
- Open `Lancelot_m1.circ` in Logisim Evolution.
- Use the keyboard component to input characters.
- Observe output on the TTY display.
- Explore the circuit to understand the custom implementation of each component.

## Design Philosophy
- **Educational:** Designed to teach and demonstrate CPU architecture and digital logic fundamentals.
- **Minimalism:** Uses only basic gates for all logic, avoiding built-in Logisim components.
- **Expandability:** Microcode-based control allows for easy addition of new instructions.

## File Structure
- `Lancelot_m1.circ`: Main Logisim Evolution circuit file containing the entire CPU design.

Created by [Ansh Swaroop](https://github.com/ansh1406).

## License
[Specify your license here, e.g., MIT, GPL, etc.]
