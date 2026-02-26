# README for 'Sorption simulation data of veterinary antibiotic interactions with kaolinite surfaces' dataset

## Overview
- Dataset of input and output files from first-principles molecular dynamics on kaolinite, detailing interactions with four veterinary antibiotics: enrofloxacin, florfenicol, ciprofloxacin, and florfenicol amine (metabolite of florfenicol).
- Includes final, complete MD trajectories of sorption for each antibiotic on Al-terminated or Si-terminated kaolinite surfaces.
- Aims to shed light on sorption dynamics of risky veterinary medicines in soil minerals, contributing to understanding drivers of antimicrobial resistance (AMR) in the environment.
- Part of the NERC Exploring the Frontiers grant NE/X009572/1; data collection occurred in 2023 on HPCs at Leeds ARC4 and ARCHER2; led by Dr Yunqing Wang.

## Data provenance and grant
- Grant: NE/X009572/1, "Antibiotic chemistry in agricultural soils: modelling mineral-antibiotic interactions from first principles".
- Field: Emerging contaminants in the environment and AMR.
- Data collection: High-performance computing resources at Leeds University (ARC4) and ARCHER2; year 2023; completed except for calculations that failed.

## Experimental design
- Geometry optimization of kaolinite surfaces and antibiotic molecules using first-principles density functional theory (DFT) with CASTEP (v22.11).
- Antibiotics placed above kaolinite surfaces (Al-terminated or Si-terminated), either as single molecules or in pairs.
- Molecular dynamics simulations performed with CASTEP; trajectories run for ~10 picoseconds.
- Data quality ensured by convergence-tested cut-off energies for optimization and maintaining Hamiltonian drift below 0.01 eV s^-1 atom^-1 during MD.
- All input files (.cell, .param) are included for the MD simulations; CASTEP output shows the version in the initial banner.

## Data included
- CASTEP-optimized antibiotic structures and optimized metabolites.
- MD trajectories for all successful simulations.
- File naming follows a structured convention described in Table 1; Table 2 explains file types.
- Files are designed to be readable with standard tools: text editors for .cell/.param/.castep/.out.cell/.out.cif, and MD trajectories (.md) with visualization software such as OVITO.

## File types and structure (Table descriptions)
- File handles and examples (summarized):
  - enrofloxacin_cat: Optimized enrofloxacin structure. File types: out.cell, out.cif, .castep.
  - kaoAl_enro: Al-terminated kaolinite surface with enrofloxacin. File types: .cell, .param, .castep, .md.
  - kaoSi_enro: Si-terminated kaolinite surface with enrofloxacin. File types: .cell, .param, .castep, .md.
  - enrofloxacin_m1_cat: Optimized enrofloxacin metabolite. File types: out.cell, out.cif, .castep.
  - kaoAl_menro: Al-terminated kaolinite surface with enrofloxacin metabolite. File types: .cell, .param, .castep, .md.
  - kaoSi_menro: Si-terminated kaolinite surface with enrofloxacin metabolite. File types: .cell, .param, .castep, .md.
  - florfenicol_cat: Optimized florfenicol structure. File types: out.cell, out.cif, .castep.
  - kaoAl_flor: Al-terminated kaolinite surface with florfenicol. File types: .cell, .param, .castep, .md.
  - kaoSi_flor: Si-terminated kaolinite surface with florfenicol. File types: .cell, .param, .castep, .md.
  - florfenicol_m1_ca: Optimized florfenicol metabolite. File types: out.cell, out.cif, .castep.
  - kaoAl_mflor: Al-terminated kaolinite surface with florfenicol metabolite. File types: .cell, .param, .castep, .md.
  - kaoSi_mflor: Si-terminated kaolinite surface with florfenicol metabolite. File types: .cell, .param, .castep, .md.
  - kaoAl_enroflor, kaoAl_fl_me, kaoAl_metmet, kaoAl_mf_en: Al-terminated kaolinite surfaces with various combinations of antibiotics and metabolites.
  - kaoSi_enroflor, kaoSi_fl_me, kaoSi_metmet, kaoSi_mf_en: Si-terminated kaolinite surfaces with various combinations of antibiotics and metabolites.
- Note: Ciprofloxacin is the metabolite of enrofloxacin; florfenicol amine is the metabolite of florfenicol. Multiple combinations include single molecules, metabolites, and mixtures on both Al- and Si-terminated kaolinite surfaces.

- Table 2 (file types):
  - .param: Text input parameters for CASTEP (task describes simulation type; additional details at provided links).
  - .cell: Structural input file; defines lattice and atomic coordinates.
  - .out.cif: Final structure after geometry optimization (cell parameters and coordinates).
  - .out.cell: Final optimized structure in CASTEP .cell format.
  - .castep: Main CASTEP output file; includes calculation parameters and CASTEP version.
  - .md: Molecular dynamics trajectory file; includes codes for data blocks (E, T, R, h, hv, F, V, S, P) and associated values.

## Data formats and access
- All input text files (.param, .cell) can be read with a text editor.
- MD trajectory files (.md) require visualization software; OVITO is recommended.
- The .param/.cell inputs enable reproducibility by allowing identical CASTEP simulations to be run.
- CASTEP version information is contained in the initial banner of .castep files.
- Additional information and formal file format details are provided via linked resources in the dataset documentation.

## Data quality and completeness
- Data quality ensured with convergence-tested cut-off energies for geometry optimizations and MD simulations with low Hamiltonian drift.
- The dataset is complete for successful simulations; some calculations failed and are not included.
- Measurements and trajectories collected in 2023 on established HPC facilities.

## How to use the data (Analysts’ perspective)
- Replicate or extend simulations for sorption dynamics on mineral surfaces with similar systems.
- Analyze MD trajectories to study adsorption/desorption events, surface binding configurations, and time-evolution of structural properties.
- Combine with other datasets to assess AMR-related environmental risk factors or to model transport and fate of veterinary antibiotics in soil.

## Citation and access
- Associated grant: NERC Exploring the Frontiers, NE/X009572/1.
- Data provenance includes explicit links to CASTEP input/output formats and recommended visualization tool OVITO.
- Data intended to support researchers investigating mineral-antibiotic interactions and environmental AMR dynamics.