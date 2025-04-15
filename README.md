# Approximate-1-bit-Full-Adder-LCAFA8-Design-and-Analysis
## Abstract
This project presents a custom transistor-level design, hierarchical symbol creation, and system-level simulation of an 8-bit adder using Cadence Virtuoso. A 1-bit full adder was implemented using CMOS logic and encapsulated into a symbol, which was instantiated eight times to form an 8-bit adder. This was further integrated into an 8×8-bit multiplier using Verilog testbench stimuli. Simulations using Analog Simulation Manager (ASM) validated functionality, showcasing efficient logic for high-bit-width operations.

## Introduction
Arithmetic units are core components of digital systems. This project aims to:

Design a CMOS-based 1-bit full adder.

Replicate it into an 8-bit adder.

Integrate it in an 8×8 multiplier system using Verilog inputs.

Simulate the structure using Cadence Virtuoso & Spectre.

## Tools & Technologies
Cadence Virtuoso (Schematic Editor, Symbol Creation)

Spectre Simulator (Functional & Power Simulation)

Analog Simulation Manager (ASM) – NewConfig Flow

## Design Methodology
### 1. CMOS 1-Bit Full Adder
Custom-designed with transistor-level logic.

Inputs: A, B, Cin

Outputs: Sum, Cout

Simulated using .meas commands and pulse inputs.

### 2. Hierarchical Symbol Creation
Schematic encapsulated as a symbol.

Instantiated 8× for 8-bit cascading adder.

Final block also symbolized for top-level hierarchy.

### 3. 8×8-Bit Multiplier System Integration
Two 8-bit inputs: A[7:0], B[7:0].

Used repeated addition logic via the 8-bit adder.

Verified 16-bit multiplication correctness via Verilog.

### 4. Simulation with ASM (NewConfig)
ASM setup used for waveform-based simulation.

Functional verification using .meas and waveform analysis.

## Output & Analysis
Input transitions simulated for A, B, Cin.

/sum output shows correct logic with some glitches due to transition states.

/cout remains stable with correct carry propagation.

### Voltage swing reaches ~1.8V, though sum doesn’t achieve ideal rail-to-rail swing.

### Propagation Delay observed between input toggles and output response.

## Multi-bit Waveform Validation
/sum<0:7> toggled correctly for all 8 bits.

/net1 and /net2 reflect valid input patterns.

Clean transitions with minimal glitching in carry save architecture.

## Simulation Results
Average Power Consumption: ~3.163 μW

Fully functional and scalable 8-bit arithmetic design using CMOS logic

Symbolic abstraction enabled modular construction

## Extension: 8-Bit Carry Save Adder (CSA)
LCAFA8 cells used to build an 8-bit CSA.

Avoided carry propagation for faster multi-operand addition.

Functional simulation verified cascading and intermediate carry correctness.

## Conclusion
This project demonstrates a complete VLSI design flow, from:

Custom transistor-level full adder ➝

Hierarchical symbol abstraction ➝

System-level simulation and power analysis ➝

Approximate error metric evaluation

It confirms the design’s correctness, low-power operation, and approximation behavior. A solid foundation for future scalable digital arithmetic blocks in VLSI, DSP, or AI hardware systems.

📬 Contact
Shirin Maria Priya W
📍 Chennai, India
📧 wshirin.4681@gmail.com
