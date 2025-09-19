# ASIC/SoC Design Flow Summary

This document summarizes the design flow of an ASIC/SoC as explained in the video.  

## O1 – Chip Modelling
- **Input:** Specifications written in C model.  
- **Activity:** Functional behavior of the chip is modeled.  
- **Verification:** Testbench is written in **C language** to validate the functionality.  
- **Output:** High-level model for early validation.  

## O2 – RTL Design (RTL Architect Stage)
- **Input:** Specs from O1.  
- **Activity:** Create a **soft copy of the hardware** using RTL (Verilog).  
- **Components Designed:**
  - Processor  
  - Peripherals/IPs  
- **Verification:** Validated with the same C testbench to ensure correctness.  
- **Output:** RTL description of the system.  

## Synthesis & IP Integration
- **RTL → Gate Level Netlist (Synthesized).**  
- Peripherals/IPs are handled in two categories:
  - **Macros** (synthesized RTL blocks).  
  - **Analog IPs** (functional RTL models or hardened IPs).  

## O3 – SoC Integration
- **Input:** Processor, peripherals, gate-level netlist, macros, and analog IPs.  
- **Activity:** Integrate everything into a complete SoC.  
- **Includes:** GPIOs, connectivity, and verification.  
- **Output:** Integrated SoC ready for physical design flow (RTL2GDS).  

## O4 – Final Chip with Peripherals
- **Activity:** Integration of processor core and peripherals into the physical chip.  
- **Verification:** Testbench in C language ensures that  
  **O1 = O2 = O3 = O4** (functional equivalence maintained at all levels).  
