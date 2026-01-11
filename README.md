# Half & Full Adder/Subtractor in Verilog (Vivado Verified)

This repository features **robust, simulation-validated implementations of Half/Full Adders and Subtractors** in Verilog. All designs are modular, fully testbench-driven, and synthesized/visualized in **Xilinx Vivado**. Simulations are also provided using open-source tools (Icarus Verilog, GTKWave).

---

## Table of Contents

- [Project Overview](#project-overview)
- [Directory Structure](#directory-structure)
- [Module Descriptions](#module-descriptions)
- [Testbenches & Verification](#testbenches--verification)
- [RTL & Technology Schematics](#rtl--technology-schematics)
- [How to Run (Simulation & Schematic Extraction)](#how-to-run-simulation--schematic-extraction)
- [Best Practices & Extensibility](#best-practices--extensibility)
- [License](#license)
- [Contact](#contact)

---

### Related Demo Videos

- **Full Adder**: [YouTube](https://youtube.com/shorts/YUpM37PON2s?feature=shared)
- **Full Subtractor**: [YouTube](https://youtube.com/shorts/F-r96FAdp4E?si=rx6YhmUOveSDVush)
- **Half Adder**: [YouTube](https://youtube.com/shorts/DaoT0IykHmo?si=SLKe4n4rGXW07Vkw)
- **Half Subtractor**: [YouTube](https://youtube.com/shorts/OssNW_W3E6k?si=Qf98I_jwUKjFF4Ek)

---

## Project Overview

Implements and verifies the following:
- **Half Adder / Full Adder**
- **Half Subtractor / Full Subtractor**

Each design follows modular, industry-style Verilog practices and comes with:
- A dedicated testbench
- RTL and technology-level schematics
- Example simulation waveforms

**Tech Stack:**  
- *Design*: Verilog HDL  
- *Simulation*: Icarus Verilog, GTKWave  
- *Synthesis & Schematics*: Xilinx Vivado

---

## Directory Structure

```
.
├── FULL_Adder/
│   ├── Full_Adder.v
│   ├── OP_WAVEFORM.png
│   ├── RTL_SCHEMATIC.png
│   ├── Technology schematic.png
│   └── Testbench
├── Full_Subtractor/
│   ├── Full_Subtractor.v
│   ├── OP_Waveform.png
│   ├── RTL_Schematic.png
│   ├── Technology Schematic.png
│   └── FS_testbench
├── HALF_Adder/
│   ├── Half_Adder.v
│   ├── OP_waveform.png
│   ├── RTL_Schematic.png
│   ├── Technology Schematic.png
│   └── Testbench_ha
├── HALF_Subtractor/
│   ├── Half_subtractor.v
│   ├── Op_waveform.png
│   ├── RTL_Schematic.png
│   ├── Technology_schematic.png
│   └── HS_testbench
└── testbench/
```
> **Note:** Each module's folder contains its source (`*.v`), simulation waveform, RTL schematic, technology schematic, and local testbench.

---

## Module Descriptions

- `*.v` — Verilog source for the arithmetic unit
- `OP_WAVEFORM.png` (or similar) — Simulation output as waveform image
- `RTL_Schematic.png` — RTL schematic (Vivado)
- `Technology Schematic.png` — Technology-mapped schematic (Vivado)
- `Testbench` — Automated testbench for all input combinations

| Module           | Main Operation     | Folder           |
|------------------|-------------------|------------------|
| Half Adder       | a + b (sum, carry)| HALF_Adder/      |
| Full Adder       | a + b + cin       | FULL_Adder/      |
| Half Subtractor  | a - b (diff, borrow) | HALF_Subtractor/ |
| Full Subtractor  | a - b - bin       | Full_Subtractor/ |

---

## Testbenches & Verification

- Each module is tested with a dedicated testbench (within its module folder).
- **All input combinations** for single-bit adder/subtractor circuits.
- Simulation results are saved as PNG images.
- Re-run simulations using either Icarus Verilog or Vivado for reproducibility.

**Sample output (from `OP_WAVEFORM.png`):**
```
Input: a=1, b=0, cin=1   |   Full Adder Output: sum=0, carry=1
Input: a=1, b=1, bin=0   |   Full Subtractor Output: diff=0, borrow=0
```

---

## RTL & Technology Schematics

- Generated using Vivado:
  - RTL schematics illustrate the functional hierarchy.
  - Technology schematics show actual gate/resource mapping.
- See `RTL_Schematic.png` and `Technology Schematic.png` in each module directory.

---

## How to Run (Simulation & Schematic Extraction)

### Prerequisites

- **Simulation:** [Icarus Verilog](https://iverilog.fandom.com/wiki/Installation_Guide), [GTKWave](http://gtkwave.sourceforge.net/) (optional)
- **Synthesis/Schematics:** Xilinx Vivado

### Example: Simulate Half Adder with Icarus

```sh
cd HALF_Adder
iverilog -o testbench_name.vvp testbench_name.v
vvp testbench_name.vvp
gtkwave half_add.vcd 
```

### Example: Generate Schematics with Vivado
- Create new Vivado project, add relevant `.v` files
- Run synthesis
- View RTL & Technology Schematic, export screenshots

---

## Best Practices & Extensibility

- Modular, standalone code enables easy reuse in ALUs or datapaths
- Follows industry and academic conventions for HDL structure and simulation
- Consider extending with parameterized/multi-bit adders or subtractors!

---

## License

This project is licensed under the MIT License.  
See [LICENSE](LICENSE) for details.

---

## Contact

Author: [Tejas R Mallah (230140111021tej)](https://github.com/230140111021tej)  
- **LinkedIn:** [Profile](https://www.linkedin.com/posts/tejas-r-mallah-28052b283_verilog-fpga-digitaldesign-activity-7364343834392113152-s981?utm_source=share&utm_medium=member_desktop&rcm=ACoAAET0mcABoSmVvowkUz7qcSZkG2bhRVZnDQ4)
- **Email:** tejasmallah@gmail.com

---

_Questions, feedback, or collaboration proposals welcome!_

```
#Verilog #DigitalDesign #Adder #Subtractor #Vivado #Testbench #FPGA #RTL #EDA
```
