# MSP430 Assembly Programming Lab 3

This repository contains the solution to **Lab 3**, focusing on GPIO (General Purpose Input/Output) programming for the MSP430 microcontroller. This lab involves configuring and controlling GPIO ports, handling input states, and driving outputs based on specified conditions.

---

## 📋 Description of the Assignment

### Part A: Theoretical Section
1. **Registers for GPIO Configuration**:
   - Explanation of `PxDIR`, `PxSEL`, `PxIN`, and `PxOUT` registers.
2. **Default Port States**:
   - Analysis of the default state of GPIO ports after a system reset.
3. **Port Configuration Example**:
   - Steps to configure `PORT9` with even-indexed pins as output and odd-indexed pins as input.
4. **Clock Cycle Calculations**:
   - Calculation of clock cycles required to generate a square wave with a period of 1 ms on an output pin using `MCLK`.

### Part B: Practical Section
#### Task: Personal Evaluation Kit
1. **Input Configuration**:
   - Four switches (`SW0`, `SW1`, `SW2`, `SW3`) are connected to `P1.0` through `P1.3`, providing a binary value (`SWstate`).
2. **Output Configuration**:
   - LEDs connected to `PORT2`.
3. **Functionality**:
   - Based on `SWstate`, the program performs one of the following actions:
     - **`SWstate = 0x01`**: Display an 8-bit binary count up on the LEDs with a 1-second delay.
     - **`SWstate = 0x02`**: Display an 8-bit binary count down on the LEDs with a 1-second delay.
     - **`SWstate = 0x04`**: Illuminate LEDs sequentially based on the digits of two student IDs, with a 1-second delay.
     - **Other Values**: Turn off all LEDs and do nothing.

#### Task: Lab Evaluation Kit
1. **Input Configuration**:
   - Four switches (`SW0`, `SW1`, `SW2`, `SW3`) connected to `P1.0` through `P1.3`.
2. **Output Configuration**:
   - Two LED ports: `PORT9` (`LEDs_A`) and `PORT10` (`LEDs_B`).
3. **Functionality**:
   - Similar to the Personal Evaluation Kit but with the following changes:
     - **`SWstate = 0x01`**: 16-bit binary count up on the LEDs.
     - **`SWstate = 0x02`**: 16-bit binary count down on the LEDs.
     - **`SWstate = 0x04`**: Illuminate LEDs in sequence according to the digits of two concatenated student IDs.

---

