# CMOS Inverter and NAND2 Gate — Transistor-Level Layout using Magic VLSI & SKY130

A transistor-level CMOS layout project implementing an **inverter** and **2-input NAND gate** from scratch using **Magic VLSI** with the **SKY130 open-source PDK**.

The project focuses on understanding CMOS device construction, layout rules, transistor topology, and physical verification through DRC and GDSII generation.

---

## Project Overview

This project demonstrates manual layout design at the transistor level using the SKY130 process technology.

Implemented circuits:

* CMOS Inverter
* CMOS NAND2 Gate

Design activities included:

* Drawing diffusion and poly layers
* Creating PMOS and NMOS transistor structures
* Metal routing and contacts
* DRC verification
* GDSII export
* Layout visualization in KLayout

---

## Tools and Technology

| Stage                | Tool             |
| -------------------- | ---------------- |
| Layout Design        | Magic VLSI       |
| Layout Visualization | KLayout          |
| Process Design Kit   | SKY130A Open PDK |
| Scripting            | Tcl              |

---

## Repository Structure

```text
project_root/
│
├── inverter/
│   ├── inverter.mag
│   ├── inverter.gds
│
├── nand2/
│   ├── nand2.mag
│   ├── nand2.gds
│
├── docs/
│   ├── inverter_layout.png
│   ├── nand2_layout.png
│   ├── drc_result.png
│
└── README.md
```

---

## CMOS Inverter Layout

The CMOS inverter was implemented using:

* PMOS transistor in n-well
* NMOS transistor in p-substrate
* Poly gate crossing diffusion regions
* Metal routing for VDD, GND, input and output

### Layout

![Inverter Layout](docs/inverter_layout.png)

---

## CMOS NAND2 Layout

The CMOS NAND gate was implemented using:

* Two PMOS transistors connected in parallel
* Two NMOS transistors connected in series
* Shared diffusion regions for area optimization

### Layout

![NAND2 Layout](docs/nand2_layout.png)

---

## Verification

The layouts were checked using Magic DRC.

Verification included:

✅ Design Rule Check (DRC)

✅ GDSII generation

✅ KLayout visualization

---

## Key Learnings

* CMOS transistor construction using diffusion and poly layers
* PMOS and NMOS physical implementation
* CMOS logic topology at transistor level
* Layout area optimization using shared diffusion
* DRC constraints in SKY130 technology
* GDSII generation flow

---

## Future Improvements

* Perform LVS verification
* Extract parasitics for timing analysis
* Design larger standard cells
* Build a complete standard-cell library
