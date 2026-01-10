# Half & Full Adder/Subtractor in Verilog (Vivado Verified)

This repository features **robust, simulation-validated implementations of Half/Full Adders and Subtractors** in Verilog. The designs are modular, testbench-driven, and suitable as foundational arithmetic blocks in digital logic design.  
All modules are synthesized and visualized using industry-standard tools like **Xilinx Vivado** and simulated with open-source tools (Icarus Verilog, GTKWave).

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

- **Full Adder**  
  [YouTube Demo](https://youtube.com/shorts/YUpM37PON2s?feature=shared)

- **Full Subtractor**  
  [YouTube Demo](https://youtube.com/shorts/F-r96FAdp4E?si=rx6YhmUOveSDVush)

- **Half Adder**  
  [YouTube Demo](https://youtube.com/shorts/DaoT0IykHmo?si=SLKe4n4rGXW07Vkw)

- **Half Subtractor**  
  [YouTube Demo](https://youtube.com/shorts/OssNW_W3E6k?si=Qf98I_jwUKjFF4Ek)

  ---

## Project Overview

This project implements and verifies:
- **Half Adder / Full Adder**
- **Half Subtractor / Full Subtractor**

All designs are written in concise, industry-style Verilog. Each block comes with a dedicated testbench, RTL and technology-level schematics, and sample simulation waveforms.

- **Tech Stack:**  
  - *Design:* Verilog HDL  
  - *Simulation:* Icarus Verilog, GTKWave  
  - *Synthesis, Schematics:* Xilinx Vivado

<br/>

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
> **Note:** All waveform and schematic images are contained locally within each module’s folder for clarity and reproducibility.

---

## Module Descriptions

Each folder contains:
- `*.v`: Verilog source for the corresponding arithmetic unit.
- **Waveform (`OP_WAVEFORM.png`)**: Screenshot of simulation output, demonstrating correct operation.
- **RTL Schematic (`RTL_Schematic.png`)**: Post-synthesis register-transfer-level schematic from Vivado.
- **Technology Schematic (`Technology Schematic.png`)**: Physical gate-level view after technology mapping.
- **Testbench**: Automated stimulus generator and self-checking unit.

| Module              | Operations    | Folder           |
|---------------------|--------------|------------------|
| Half Adder          | a+b (sum,carry)       | `HALF_Adder/`  |
| Full Adder          | a+b+cin (sum,carry)   | `FULL_Adder/`  |
| Half Subtractor     | a-b (diff,borrow)     | `HALF_Subtractor/` |
| Full Subtractor     | a-b-bin (diff,borrow) | `Full_Subtractor/` |

---

## Testbenches & Verification

- Each module is comprehensively tested with its relevant testbench (located in its directory).
- Tests include **all input combinations** for 1-bit adder and subtractor circuits.
- Simulation output is saved as PNG waveform images.
- For reproducibility, you can re-run simulations using Icarus Verilog or Vivado’s simulator.

**Sample simulation output (from OP_WAVEFORM.png):**
```
Input: a=1, b=0, cin=1   |   Full Adder Output: sum=0, carry=1
Input: a=1, b=1, bin=0   |   Full Subtractor Output: diff=0, borrow=0
```

---

## RTL & Technology Schematics

- All synthesized using Vivado:  
  - RTL schematics precisely illustrate the functional hierarchy.
  - Technology schematics display the mapped logic gates and interconnections.
- **Refer to the included schematic images in each module directory.** These are crucial for demonstrating your competence in using professional FPGA and ASIC toolchains.

---

## How to Run (Simulation & Schematic Extraction)

#### Prerequisites

- **Simulation:** Icarus Verilog, GTKWave *(open-source, cross-platform)*
- **Synthesis & Schematics:** Xilinx Vivado *(for RTL/technology diagrams)*

#### Simulation Example (Icarus Verilog)
```sh
cd HALF_Adder
iverilog -o ha_sim Half_Adder.v Testbench_ha
vvp ha_sim
gtkwave dump.vcd &
```

#### Generate Schematics (Vivado)

- Create a new Vivado project.
- Add `*.v` sources from desired module.
- Run synthesis.
- Open "RTL Analysis" for RTL schematic.
- Open "Technology Schematic" for gate-level mapping.
- Export/capture screenshots as shown in `/FULL_Adder/`, etc.

---

## Best Practices & Extensibility

- Modular structure ensures easy integration in larger ALU/datapath projects.
- All code follows best practices for digital logic design and testbench structure.
- You are encouraged to extend with multi-bit versions or parameterized designs as interview/assignment ready skill demonstrations.

---

## License

This repository is released under MIT License.  
*See [LICENSE](./LICENSE) for details.*

---

## Contact

Author: [230140111021tej](https://github.com/230140111021tej)  
**For questions, suggestions, or contributions – open an issue or pull request!**

---

*This README is designed for professional readability and technical screening. All images referenced are contained in this repository – please ensure you do not reference images by broken links or external names.*

<!--
Screenshots are available locally (do NOT use image1/image2/image3, use only repo files). Remove image links if not included in repo.
-->
---

## License

This project is for academic and educational use.
