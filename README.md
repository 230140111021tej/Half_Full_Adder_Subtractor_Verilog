# Half & Full Adder/Subtractor in Verilog

This repository contains Verilog implementations, testbenches, waveforms, and schematics for basic arithmetic circuits:
- Half Adder
- Full Adder
- Half Subtractor
- Full Subtractor

Each module has its own dedicated directory with the Verilog source code, testbenches, simulation results, and design schematics.

## Folder Structure

```
.
├── FULL_Adder
│   ├── Full_Adder.v
│   ├── OP_WAVEFORM.png
│   ├── RTL_SCHEMATIC.png
│   ├── Technology schematic.png
│   └── Testbench
├── Full_Subtractor
│   ├── Full_Subtractor.v
│   ├── OP_Waveform.png
│   ├── RTL_Schematic.png
│   ├── Technology Schematic.png
│   └── FS_testbench
├── HALF_Adder
│   ├── Half_Adder.v
│   ├── OP_waveform.png
│   ├── RTL_Schematic.png
│   ├── Technology Schematic.png
│   └── Testbench_ha
├── HALF_Subtractor
│   ├── Half_subtractor.v
│   ├── Op_waveform.png
│   ├── RTL_Schematic.png
│   ├── Technology_schematic.png
│   └── HS_testbench
└── testbench
```

## Description

### 1. Half Adder
- **File**: `HALF_Adder/Half_Adder.v`
- **Testbench**: `Testbench_ha`
- **Outputs**:
  - `OP_waveform.png`: Simulated output waveform
  - `RTL_Schematic.png`: RTL Schematic view
  - `Technology Schematic.png`: Technology mapped schematic

### 2. Full Adder
- **File**: `FULL_Adder/Full_Adder.v`
- **Testbench**: `Testbench`
- **Outputs**:
  - `OP_WAVEFORM.png`: Simulated output waveform
  - `RTL_SCHEMATIC.png`: RTL Schematic view
  - `Technology schematic.png`: Technology mapped schematic

### 3. Half Subtractor
- **File**: `HALF_Subtractor/Half_subtractor.v`
- **Testbench**: `HS_testbench`
- **Outputs**:
  - `Op_waveform.png`: Simulated output waveform
  - `RTL_Schematic.png`: RTL Schematic view
  - `Technology_schematic.png`: Technology mapped schematic

### 4. Full Subtractor
- **File**: `Full_Subtractor/Full_Subtractor.v`
- **Testbench**: `FS_testbench`
- **Outputs**:
  - `OP_Waveform.png`: Simulated output waveform
  - `RTL_Schematic.png`: RTL Schematic view
  - `Technology Schematic.png`: Technology mapped schematic

## How to Use

1. **View the Source Code**: Each arithmetic circuit's Verilog code can be found in its respective folder.
2. **Run Simulations**: Use the provided testbenches to simulate the designs in a Verilog simulator (e.g., ModelSim, Icarus Verilog).
3. **Check Results**: Review the waveform images for simulation results and the schematic images for RTL and technology-level views.

## Visual Overview

Repository file & folder structure:
![Project Structure](image3)

Sample files in HALF_Adder:
![Sample Directory](image1)

Repository on GitHub:
![GitHub Repo View](image2)

---

## License

This project is for academic and educational use.
