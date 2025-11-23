Week 8 – Post-Layout STA & PVT Timing Analysis
VSDBabySoC – Complete ASIC Flow (RTL → GDS)

This repository contains the Week 8 work for the VSDBabySoC project.
In this week, post-layout Static Timing Analysis (STA) is performed using the SPEF file generated after routing.
Timing is analyzed across all PVT corners and compared with Week 3 post-synthesis results.

1. Objective of Week 8
The goal is to:
Run Post-Layout STA using the final routed netlist and SPEF.
Analyze timing across multiple PVT corners (TT, SS, FF).
Visualize timing paths using timing graphs.
Compare Week 3 post-synthesis vs Week 8 post-route timing.
Understand how RC parasitics affect setup/hold timing.

3. Step-by-Step Procedure
Step 1 — Load Post-Route Design in OpenSTA

Open OpenSTA:
sta
Run the TCL script:
source sta_scripts/post_route_sta.tcl
This script performs:
Loading Liberty libraries
Loading post-route netlist
Loading SDC constraints
Annotating SPEF parasitics
Running STA for TT, SS, FF

Generating timing reports
📜 3. OpenSTA Script (post_route_sta.tcl)
4. Metrics Extracted

For each PVT corner, the following metrics are collected:

Metric	Meaning
WNS	Worst Negative Slack (Setup)
TNS	Total Negative Slack (Setup)
WHS	Worst Hold Slack
THS	Total Hold Slack

These determine whether the design meets timing.

5. Timing Graphs

Timing graphs were generated using:

report_timing -path_delay max
report_timing -path_delay min


Sample graph images (stored in /graphs/):

graphs/
├── TT_graph.png
├── SS_graph.png
└── FF_graph.png
Typical Observations:

Setup slack usually degrades after routing due to extra RC delay.

Hold slack often becomes worse in FF corner.

SPEF adds:

wire resistance

capacitance

coupling effects

These make post-route timing more realistic.
7. Interpretation of Results
✔ Why Post-Route Timing is Different

Physical routing adds real delays.

Wires have resistance and capacitance.

Coupling between adjacent nets introduces crosstalk delay.

✔ Effect of SPEF Annotation

Replaces ideal wire loads with:

actual parasitic capacitance

resistance segments

coupling capacitances

Results become silicon-accurate.

✔ PVT Impact

SS → slow transistors → worst setup

FF → fast transistors → worst hold

TT → typical behavior

📦 8. Deliverables
✔ Timing Reports
✔ Timing Graphs
✔ STA TCL Script
✔ Comparison Table
✔ Documentation
All steps, commands, and results included in this README.

Final Outcome (End of Week 8)
By completing this week, you have:
Performed Post-Layout STA using SPEF.
Run STA across TT, SS, FF corners.
Generated full timing reports and graphs.
Compared synthesis vs layout timing.
Understood how RC parasitics affect silicon behavior.
Completed the entire RTL → GDS ASIC design flow.
