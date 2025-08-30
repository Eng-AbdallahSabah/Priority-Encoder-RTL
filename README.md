# Priority-Encoder-RTL

This repository offers a **Verilog RTL implementation** of an **8-to-3 Priority Encoder** along with a complete **testbench** and simulation setup for functional verification.

---

##  Design Overview
A **Priority Encoder** is a combinational circuit that encodes the index of the highest-priority active input (if multiple inputs are asserted) into a binary output. Here, the input with the highest index (e.g., bit 7 over bit 0) takes precedence. :contentReference[oaicite:3]{index=3}

Typical applications include **interrupt controllers**, **signal arbitration**, and conversion from high-resolution to binary indices. :contentReference[oaicite:4]{index=4}

---

##  Repository Structure
```
Priority-Encoder-RTL/
├── rtl/
│ └── priority_enc.v # Verilog RTL source for encoder
├── tb/
│ └── priority_enc_tb.sv # Verification testbench
├── scripts/
│ ├── run.do # Simulation script (ModelSim/Questa)
│ └── coverage_rpt.txt # Coverage report (if applicable)
├── results/
│ ├── transcript # Simulation log
│ └── Screenshot.png # Waveform or result visualization
├── docs/
│ └── README.md # You are reading
├── LICENSE # MIT License
└── README.md # Project overview
```

---

##  Getting Started

1. Open your simulator (e.g., **ModelSim** or **QuestaSim**).
2. Navigate to the `scripts/` folder:
   ```tcl
   cd scripts
   do run.do
3.Review the simulation output:
In results/transcript—for logs and behavioral data.
In results/Screenshot.png—for visual waveforms or signals.
In scripts/coverage_rpt.txt (if coverage was measured).
What’s Inside

RTL (priority_enc.v)
Implements the 8-to-3 encoder by prioritizing the highest active bit among multiple assertions.

Testbench (priority_enc_tb.sv)
Validates functionality across all scenarios, including edge cases and multiple inputs.

Simulation Setup

run.do: Automates compilation and execution scripts.

transcript: Logs simulation results.

coverage_rpt.txt: Functional coverage output (if coverage was enabled).

Visualization
A screenshot (waveform) illustrates signal transitions or output behavior.

Tools & Requirements

Hardware Description: Verilog / SystemVerilog

Verification Environment: ModelSim, QuestaSim, or compatible simulators

License

Distributed under the MIT License. Check the LICENSE file for more details.

Learning Points

Understanding how priority encoding resolves multiple active inputs.

Structuring testbenches for digital circuit verification.

Organizing project files for clarity and modularity.
