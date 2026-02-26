# README for 'Sorption simulation data of veterinary antibiotic interactions with kaolinite surfaces' dataset

## Overview
- A dataset of input and output files from first-principles molecular dynamics (MD) calculations.
- Focuses on interactions between kaolinite (soil mineral) surfaces and four veterinary antibiotics (and their metabolites): enrofloxacin, florfenicol, ciprofloxacin (enrofloxacin metabolite), and florfenicol amine (florfenicol metabolite).
- Includes both Al-terminated and Si-terminated kaolinite surfaces to illuminate sorption dynamics relevant to environmental AMR.
- Collected in 2023 on HPC resources (Leeds ARC4 and ARCHER2) as part of the NERC Exploring the Frontiers grant NE/X009572/1.

## What the data contain
- Complete MD trajectories for the sorption processes of each antibiotic (and metabolites) on kaolinite surfaces.
- Optimized molecular structures for parent antibiotics and metabolites.
- Data cover various surface configurations: Al-terminated and Si-terminated kaolinite, with single molecules, pairs, and combinations (e.g., multiple antibiotics/metabolites on surfaces).
- File naming follows a described convention (Table 1) and file type descriptions (Table 2).

## Experimental design and methods
- Geometry optimization performed with CASTEP (first-principles DFT).
- MD simulations run after optimization, using CASTEP, with trajectories approximately 10 picoseconds long.
- Data quality controls:
  - Convergence-tested cut-off energies for optimizations and MD.
  - Hamiltonian drift kept below 0.01 eV per second per atom.
- All input files used for simulations are included:
  - .cell and .param: CASTEP input parameters and structure.
  - .castep: main CASTEP output (with version and calculation details).
  - .out.cell and .out.cif: optimized final structures.
  - .md: MD trajectory data (with codes for energy, temperature, coordinates, cell, velocities, stresses, etc.).

## File types and how to use
- Table 1 describes the file sets for each combination (e.g., enrofloxacin_cat, kaoAl_enro, kaoSi_enro, enrofloxacin_m1_cat, etc.).
- Table 2 describes file types:
  - .param: computational task and parameters (geometry optimization, MD; locations for further information).
  - .cell: structural input (lattice, atomic coordinates).
  - .out.cell: optimized final structure (same format as .cell).
  - .out.cif: final optimized structure in CIF format.
  - .castep: main CASTEP output (version and calculation details).
  - .md: MD trajectory (units, with codes E, T, R, h, hv, F, V, S, P).
- Accessibility:
  - Text files can be opened with standard editors (Notepad, etc.).
  - MD trajectories can be viewed with visualization tools such as OVITO.

## Provenance and completeness
- Data collected in 2023 on Leeds ARC4 and ARCHER2 HPC facilities.
- Curated by Dr Yunqing Wang (PDRA).
- The dataset is complete except for calculations that failed.
- CASTEP version information is included in the initial banner of .castep outputs.

## Reuse and licensing notes
- The computational workflow uses CASTEP, a widely used first-principles code that is free to use under academic licensing.
- Dataset documents the exact input files (.param, .cell) and output files, enabling reproducibility of the simulations (subject to CASTEP licensing and access to the appropriate software).

## Relevance to data leadership and broader data strategy
- Demonstrates end-to-end data capture for a complex scientific computation, including:
  - Transparent provenance (optimized structures, MD trajectories, and exact input parameters).
  - Rich metadata through explicit file descriptions and table-backed conventions.
  - Reproducibility through complete input/output file sets and versioning hints.
  - Discoverability via standardized file naming conventions and descriptive metadata in Tables 1 and 2.
- Supports cross-disciplinary data sharing for environmental AMR research by providing granular, trajectory-level data on mineral-antibiotic interactions.
- Highlights the importance of including both primary compounds and metabolites, multiple surface terminations, and explicit documentation of data quality controls (e.g., Hamiltonian drift criteria).

## Key context and implications
- Fits within the broader topic of “emerging contaminants” in environmental research and helps understand drivers of antimicrobial resistance in soils.
- Although focused on a specific mineral (kaolinite) and antibiotics, the dataset exemplifies a comprehensive approach to capturing and describing high-complexity computational data that can inform larger data ecosystems and collaboration across research groups.