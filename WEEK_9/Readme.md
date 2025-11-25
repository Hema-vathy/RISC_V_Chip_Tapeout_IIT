Week-wise Documentation
//Week 1 – Introduction & Architecture

Understanding SoC basics
VSDBabySoC block diagram
RISC-V core + custom blocks
Tool installation steps
Verification of OpenLane and PDK setup
Screenshots: Terminal startup, directory structure, PDK check

//Week 2 – RTL Simulation

Running testbench for VSDBabySoC
Icarus Verilog simulation
Checking waveforms on GTKWave
Debugging RTL warnings
Screenshots: Sim command logs, GTKWave output

//Week 3 – Logic Synthesis

Running synthesis (run_synthesis)
Inspection of synthesis reports:
Cell count
Area report
Timing slack
Constraints applied (CLOCK_PERIOD etc.)
Screenshots: Synthesis log, OpenLane results folder

//Week 4 – Floorplanning

Die and core area setup
Tap cells and end-cap insertion
PDN generation
Floorplan configuration changes
Screenshots: Floorplan DEF, GUI view, PDN logs

//Week 5 – Placement
Global placement
Detailed placement
Checking density, overlaps, DRC
Screenshots: OpenROAD placement window, reports

//Week 6 – Clock Tree Synthesis (CTS)

Clock buffer insertion
CTS-based timing report
Skew analysis
Screenshots: CTS tree view, CTS logs

//Week 7 – Routing

Global + Detailed routing
Antenna checks
DRC-clean layout
Generating final routed DEF and GDS
Screenshots: Final routed layout, DRC summary

//Week 8 – SPEF & Post-Layout STA

SPEF extraction using OpenROAD
Timing extraction with parasitics
Setup & Hold analysis
Timing comparison with pre-route results
Screenshots: STA reports, SPEF logs

//Week 9 – Final Documentation & Summary

This week consolidates all the information into this GitHub repository.
All screenshots show my Unix terminal username clearly, following IITGN rules.
