# DFT Calculations Supporting A Mechanistic Understanding of How Weak Links Enhance Polymer Recyclability Towards Uncovering Idealized Doping Strategy

## Overview
This repository contains input and output files for the density functional theory (DFT) calculations reported in the manuscript:

**“A Mechanistic Understanding of How Weak Links Enhance Polymer Recyclability Towards Uncovering Idealized Doping Strategy”**  
*2025*

The calculations were performed to compute thermodynamic properties for the polymer and copolymer systems discussed in the paper. 

---

## Repository Structure
```
pmma-dft-calcs/
├── README.md
├── bde_calc_grid.csv
├── ts_calc_grid.csv
│
├── bond_dissociation/
│   ├── bond_dissociation_energies.csv
│   ├── co_AABB_cleav_case_A/
│   │   ├── neutral/
│   │   ├── radical1/
│   │   └── radical2/
│   ├── co_AABB_cleav_case_B/
│   │   ├── neutral/
│   │   ├── radical1/
│   │   └── radical2/
│   ├── co_ABAB_cleav_case_A/
│   │   ├── neutral/
│   │   ├── radical1/
│   │   └── radical2/
│   ├── co_ABAB_cleav_case_B/
│   │   ├── neutral/
│   │   ├── radical1/
│   │   └── radical2/
│   ├── homo_PMDL_cleav/
│   │   ├── neutral/
│   │   ├── radical1/
│   │   └── radical2/
│   ├── homo_PMMA_cleav/
│   │   ├── neutral/
│   │   ├── radical1/
│   │   └── radical2/
│   ├── internal_alkene_end_cleav/
│   │   ├── neutral/
│   │   ├── radical1/
│   │   └── radical2/
│   └── unsat_end_cleav/
│       ├── neutral/
│       ├── radical1/
│       └── radical2/
│
├── depoly_reactions/
│   ├── hetero/
│   │   ├── co_p_dl_to_ma/
│   │   ├── co_p_ma_to_dl/
│   │   ├── co_t_dl_to_ma/
│   │   └── co_t_ma_to_dl/
│   ├── PMDL/
│   │   ├── PMDL_elim/
│   │   ├── PMDL_p_rad_bs/
│   │   └── PMDL_t_rad_bs/
│   └── PMMA/
│       ├── PMMA_elim/
│       ├── PMMA_p_rad_bs/
│       └── PMMA_t_rad_bs/
│
└── input_xyzs/
    ├── AABB_case_A_p_rad.xyz
    ├── AABB_case_A_t_rad.xyz
    ├── AABB_case_B_p_rad.xyz
    ├── AABB_case_B_t_rad.xyz
    ├── AABB_tetramer.xyz
    ├── ABAB_case_A_p_rad.xyz
    ├── ABAB_case_A_t_rad.xyz
    ├── ABAB_case_B_p_rad.xyz
    ├── ABAB_case_B_t_rad.xyz
    ├── ABAB_tetramer.xyz
    ├── PMDL_p_rad_tetramer.xyz
    ├── PMDL_rad_1.xyz
    ├── PMDL_rad_2.xyz
    ├── PMDL_t_rad_tetramer.xyz
    ├── PMDL_tetramer.xyz
    ├── PMMA_p_rad_tetramer.xyz
    ├── PMMA_rad_1.xyz
    ├── PMMA_rad_2.xyz
    ├── PMMA_t_rad_tetramer.xyz
    ├── PMMA_tetramer_internal_alkene.xyz
    ├── PMMA_tetramer_unsat.xyz
    ├── PMMA_tetramer.xyz
    ├── unsat_rad_1.xyz
    ├── internal_alkene_rad_1.xyz
    ├── internal_alkene_rad_2.xyz
    └── unsat_rad_2.xyz
```

---

## Directory Contents

### bond_dissociation/
Contains DFT calculation data for bond dissociation energy (BDE) calculations across various polymer structures:
- `bond_dissociation_energies.csv` — Summary of computed BDE values
- Each subdirectory corresponds to a specific bond cleavage scenario:
  - `co_AABB_cleav_case_A/` and `co_AABB_cleav_case_B/` — AABB copolymer cleaving cases
  - `co_ABAB_cleav_case_A/` and `co_ABAB_cleav_case_B/` — ABAB copolymer cleaving cases
  - `homo_PMMA_cleav/` and `homo_PMDL_cleav/` — Homopolymer cleavage
  - `internal_alkene_end_cleav/` and `unsat_end_cleav/` — End-group cleavage scenarios
- Each cleaving scenario contains subdirectories:
  - `neutral/` — Calculations for neutral species
  - `radical1/` — Calculations for the first radical fragment
  - `radical2/` — Calculations for the second radical fragment

### depoly_reactions/
Contains DFT calculation data for depolymerization reaction pathway studies, organized by polymer type:
- `hetero/` — Heterolytic depolymerization reactions
  - `co_p_dl_to_ma/`, `co_p_ma_to_dl/`, `co_t_dl_to_ma/`, `co_t_ma_to_dl/` — Copolymer conversions
- `PMMA/` — PMMA homopolymer depolymerization
  - `PMMA_elim/` — Elimination reactions
  - `PMMA_p_rad_bs/` — Primary radical β-scission pathways
  - `PMMA_t_rad_bs/` — Tertiary radical β-scission pathways
- `PMDL/` — PMDL homopolymer depolymerization
  - `PMDL_elim/`, `PMDL_p_rad_bs/`, `PMDL_t_rad_bs/` — Similar reaction pathways

### input_xyzs/
Contains initial molecular geometry files (XYZ format) for all calculated systems, used as input for DFT optimizations.

## File Structure Within Each Calculation Directory

Within each `neutral/`, `radical1/`, or `radical2/` subdirectory, you will typically find:
- `orca.inp` — ORCA input file for the DFT calculation
- `orca.xyz` — ORCA optimized geometry
- `orca_trj.xyz` — Full optimization trajectory
- `structure.xyz` — Optimized structure in standard XYZ format
- `shermo_298.txt` — Thermochemistry output at 298 K
- `shermo_563.txt` — Thermochemistry output at 563 K
- (Additional files may include `orca.001.xyz`, `orca.002.xyz`, `orca.allxyz` from multi-step calculations)

## Calculation Data Files

- `bde_calc_grid.csv` — Summary of bond dissociation energy calculation inputs
- `ts_calc_grid.csv` — Summary of transition state calculation inputs

## Citation
If you use or reference these calculations, please cite:

```
{TBD}}
```