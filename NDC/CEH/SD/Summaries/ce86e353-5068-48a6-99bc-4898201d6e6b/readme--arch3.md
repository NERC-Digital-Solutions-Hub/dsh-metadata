# Sorption simulation data of veterinary antibiotic interactions with kaolinite surfaces

## Overview
- Dataset of input and output files from first principles molecular dynamics (MD) calculations on kaolinite, detailing interactions with four veterinary antibiotics: enrofloxacin, florfenicol, ciprofloxacin (metabolite of enrofloxacin), and florfenicol amine (metabolite of florfenicol).
- Aimed at understanding sorption dynamics of veterinary medicines with soil mineral structures and implications for antimicrobial resistance (AMR).
- Collected under the NERC Exploring the Frontiers grant NE/X009572/1 during 2023 on Leeds ARC4 and ARCHER2 high-performance computing facilities.
- Work conducted by PDRA Yunqing Wang; data are complete apart from calculations that failed.
- Data quality and reproducibility are supported by including all input (.cell, .param) files and by providing explicit file naming and descriptors; CASTEP is used for both geometry optimization and MD.

## Experimental design
- Geometry optimization performed on kaolinite surfaces and antibiotics using first principles DFT with CASTEP (version 22.11).
- Surfaces examined: Al-terminated and Si-terminated kaolinite.
- Antibiotics tested: single molecules and pairs (including metabolites Ciprofloxacin and Florfenicol amine as appropriate).
- MD simulations run after optimization, trajectories of about 10 picoseconds.
- Quality controls: convergence-tested cut-off energies for optimization; MD stability via Hamiltonian drift kept below 0.01 eV s^-1 per atom.
- All relevant CASTEP inputs are included to enable replication of the simulations.

## Data included
- The dataset includes optimized molecular structures and MD trajectories for all successful simulations, organized by file handles (Table 1) and described in Table 2.
- Four antibiotics and their metabolites are represented, with separate entries for Al-terminated and Si-terminated kaolinite surfaces.
- Example file handles and what they contain:
  - enrofloxacin_cat: Optimized enrofloxacin structure (out.cell, out.cif, .castep)
  - kaoAl_enro: Al-terminated kaolinite surface with enrofloxacin (.cell, .param, .castep, .md)
  - kaoSi_enro: Si-terminated kaolinite surface with enrofloxacin (.cell, .param, .castep, .md)
  - enrofloxacin_m1_cat: Optimized metabolite of enrofloxacin (out.cell, out.cif, .castep)
  - kaoAl_menro / kaoSi_menro: Surfaces with enrofloxacin metabolite
  - florfenicol_cat, florfenicol_m1_ca, and corresponding surfaces with florfenicol and its metabolite
  - Combinations such as kaoAl_enroflor, kaoAl_metmet, kaoSi_enroflor, kaoSi_metmet, and related entries for mixtures of antibiotics and metabolites
- File types included:
  - .param: CASTEP parameter input for each calculation
  - .cell: CASTEP structural input for each calculation
  - .castep: main CASTEP output file (calculation details and version)
  - .md: MD trajectory files (structure sequences, energies, temperatures, atomic coordinates, cell data, forces, etc.)
  - .out.cell and .out.cif: final optimized structure representations
- File format notes:
  - Text files (.param, .cell, .out.cif, .out.cell, .castep) can be read with standard editors.
  - MD trajectory files (.md) require suitable visualization tools, e.g., OVITO.

## Data accessibility and reuse
- The dataset provides comprehensive material to reproduce or extend the work using CASTEP and standard MD analysis.
- Trajectories and optimized structures are available alongside the input files to support transparency and verification.
- MD trajectory content includes key codes and data categories (E, T, R, h, hv, F, V, S, P) to interpret simulation results.
- The data emphasize AMR-relevant environmental chemistry within soil minerals and could inform monitoring frameworks addressing environmental contaminants and governance of data sharing and reproducibility.