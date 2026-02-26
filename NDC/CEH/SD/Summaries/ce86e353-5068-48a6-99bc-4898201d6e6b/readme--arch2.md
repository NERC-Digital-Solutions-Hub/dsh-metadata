# README for 'Sorption simulation data of veterinary antibiotic interactions with kaolinite surfaces' dataset

## Overview
- A dataset of input and output files from first-principles molecular dynamics (MD) calculations modeling the interaction of four veterinary antibiotics with kaolinite surfaces.
- Antibiotics: enrofloxacin, florfenicol, ciprofloxacin (metabolite of enrofloxacin), and florfenicol amine (metabolite of florfenicol).
- Examines sorption dynamics on aluminium-terminated (kaolinite Al) and silicon-terminated (kaolinite Si) kaolinite surfaces.
- Part of the NERC Exploring the Frontiers grant on antibiotic chemistry in agricultural soils and antimicrobial resistance (AMR); data collected in 2023 on ARCHER2 and ARC4 at Leeds.
- Complete dataset except for calculations that failed; produced by Dr Yunqing Wang.

## Data contents
- Final, complete MD trajectories for the sorption process of each antibiotic (and relevant metabolites) on both Al-terminated and Si-terminated kaolinite surfaces.
- Includes optimized molecular structures and all MD input files.
- File types and organization described in Table 1; Table 2 provides detailed file-type descriptions.
- File formats are standard: .cell, .param (CASTEP input); .out.cell, .out.cif (geometry-optimized structures); .castep (CASTEP outputs); .md (MD trajectories).
- Text files can be read with common editors; MD trajectories can be viewed with visualization tools such as OVITO.

## Experimental design
- Geometry optimization of kaolinite surfaces and antibiotics using CASTEP (first-principles DFT).
- Surfaces tested: aluminium-capped (Al-terminated) and silicon-capped (Si-terminated) kaolinite.
- Antibiotics placed above surfaces (single molecules or pairs) and subjected to first-principles MD simulations.
- MD trajectories run for ~10 picoseconds.
- Data quality ensured by convergence-tested cut-off energies for optimization and by maintaining Hamiltonian drift at a low level (< 0.01 eV per atom per second).
- All relevant input parameters (.param) and structural definitions (.cell) are included to enable replication of simulations.

## File types and descriptions (highlights)
- .param: CASTEP simulation parameters (task type, etc.).
- .cell: CASTEP structural definitions (lattice, atomic coordinates).
- .out.cell: optimized final structure in CASTEP cell format.
- .out.cif: final optimized structure in CIF format.
- .castep: main CASTEP output file (version, calculation details, results).
- .md: molecular dynamics trajectory data (energies, temperature, coordinates, cell derivatives, forces, etc.).
- Naming conventions (e.g., enrofloxacin_cat, kaoAl_enro, kaoSi_enro, etc.) describe molecule, metabolite status, and surface termination; Table 1 in the README details all combinations.

## Data quality and completeness
- The dataset is complete for successful simulations; includes all optimized structures and MD trajectories except for calculations that failed.
- Data quality was controlled via convergence criteria and stable Hamiltonian drift during MD.

## Reproducibility and accessibility
- Input files (.param and .cell) can be used to reproduce identical CASTEP simulations.
- MD trajectories (.md) are suitable for visualization and analysis with standard tools (e.g., OVITO).
- Metadata and file types are described to facilitate data reuse and integration with other environmental datasets.

## Context and environmental relevance
- Addresses the environmental fate of antibiotics in soils, a key factor in environmental health monitoring and AMR risk assessment.
- Provides a mechanistic, first-principles view of sorption dynamics on common soil mineral components, contributing to understanding drivers of AMR in agricultural settings.
- Supports data-driven monitoring by delivering standardized, machine-readable results suitable for integration with broader environmental datasets and policy evaluations.

## Implications for monitoring and policy
- Enables quantitative assessment of antibiotic sorption to soil minerals, informing models of environmental distribution, persistence, and potential mobility.
- Data can be combined with other environmental datasets to enhance monitoring programs and evaluate policy effectiveness related to antibiotic usage, soil health, and AMR mitigation.
- Emphasizes the importance of accessible, well-documented datasets to support transparency and data reuse in environmental monitoring.