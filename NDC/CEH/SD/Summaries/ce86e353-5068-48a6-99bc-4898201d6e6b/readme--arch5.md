# Sorption simulation data of veterinary antibiotic interactions with kaolinite surfaces

## Overview
- A dataset of input and output files from first-principles molecular dynamics calculations on kaolinite interacting with four veterinary antibiotics (enrofloxacin, florfenicol, ciprofloxacin, florfenicol amine) and their metabolites.
- Provides insight into sorption dynamics on Al-terminated and Si-terminated kaolinite surfaces.
- Collected in 2023 on high-performance computing resources (Leeds ARC4 and ARCHER2) by Dr Yunqing Wang under the NERC grant NE/X009572/1.
- Complete dataset except for calculations that failed; supports understanding of emerging environmental contaminants and antimicrobial resistance drivers.

## Experimental design and data collection
- Geometry optimization of kaolinite surfaces and antibiotics using CASTEP (first-principles DFT, version 22.11).
- Antibiotics placed above kaolinite surfaces (Al-terminated or Si-terminated) with trajectories run for ~10 ps using first-principles MD.
- Data quality controlled with convergence-tested cut-off energies and Hamiltonian drift kept below 0.01 eV s^-1 atom^-1.
- All input files (.cell, .param) and optimization results (.out.cell, .out.cif) are included; CASTEP version appears in the initial banner of .castep outputs.

## Data included and file organization
- The dataset uses a structured naming convention with multiple file handles, each representing specific systems (e.g., enrofloxacin_cat, kaoAl_enro, kaoSi_enro, enrofloxacin_m1_cat, etc.).
- For each system, the dataset includes:
  - Optimized structures: enrofloxacin_cat, enrofloxacin_m1_cat, florfenicol_cat, florfenicol_m1_ca, etc. with corresponding .out.cell and .out.cif.
  - Kaolinite surfaces with antibiotics or antibiotic metabolites: al-terminated (kaoAl_*) and si-terminated (kaoSi_*), each with .cell, .param, .castep, and .md trajectory files.
  - Complex systems (e.g., enroflor, flor-me, metmet, etc.) combining antibiotics and metabolites on surfaces.
- File types described in Table 2:
  - .param: CASTEP parameter input for each calculation (task, settings, etc.).
  - .cell: CASTEP structural input (lattice, atomic positions, etc.).
  - .out.cif and .out.cell: final/optimized structures in CIF and CASTEP formats.
  - .castep: main CASTEP output file (with version and calculation details).
  - .md: molecular dynamics trajectory data (energy, temperature, coordinates, cell, forces, etc.).
- Text files are readable in standard editors; MD trajectories can be viewed with OVITO or similar visualization tools.
- Aims to enable exact replication using CASTEP by including all relevant input, parameters, and trajectory data.

## Accessing and using the data
- Documentation indicates how to reproduce simulations using CASTEP (parameters and cell files provided).
- MD trajectories are compatible with common visualization tools (e.g., OVITO) for analysis of sorption dynamics.
- The dataset is suitable for researchers studying mineral–antibiotic interactions, environmental AMR drivers, and sorption processes in soils.

## Data quality and completeness
- Data are complete for successful calculations; some calculations failed and are noted as not included.
- All relevant metadata provided: CASTEP version, convergence criteria, and initial banners in .castep outputs.
- Data collected under a clearly defined experimental design with explicit surface terminations and molecular configurations.

## Provenance, licensing, and governance
- Provenance: NERC Exploring the Frontiers grant NE/X009572/1; project conducted in 2023 at Leeds University (ARC4) and ARCHER2; principal investigator/driving researcher Yunqing Wang.
- Licensing and reuse: CASTEP is free to use under academic license; dataset references CASTEP licensing and provides links to obtain the software. Explicit licensing for the dataset itself is not stated in the excerpt.
- Governance implications for Data Stewards:
  - Clear metadata and file-level documentation support discoverability and reuse.
  - Reproducibility is facilitated by including raw inputs, parameters, and trajectory data.
  - Large, multi-format data with potential interoperability considerations; guidance provided for readers to access, view, and replicate analyses.
  - Data provenance tied to a specific grant and project, enabling traceability and accountability.