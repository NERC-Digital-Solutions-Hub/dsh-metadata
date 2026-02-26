# README for 'Sorption simulation data of veterinary antibiotic interactions with kaolinite surfaces' dataset

- **Scope and purpose**
  - Dataset comprises input and output files from first-principles molecular dynamics calculations of antibiotics interacting with kaolinite surfaces.
  - Focuses on four veterinary antibiotics and their metabolites: enrofloxacin, ciprofloxacin (metabolite of enrofloxacin), florfenicol, and florfenicol amine (metabolite of florfenicol).
  - Aims to illuminate sorption dynamics of veterinary medicines on soil mineral structures, contributing to understanding of environmental contaminants and antimicrobial resistance (AMR).
  - Collected under the NERC Exploring the Frontiers grant NE/X009572/1 in 2023; data generated on Leeds ARC4 and ARCHER2 HPC resources; complete except for calculations that failed.

- **Data content and structure**
  - Contains both optimized molecular structures and complete MD trajectories (approximately 10 ps) for each antibiotic on kaolinite surfaces.
  - Kaolinite surfaces studied: aluminium-terminated (Al-terminated) and silicon-terminated (Si-terminated).
  - Data organization includes optimized structures, surfaces with adsorbed antibiotics (single molecules and pairs), metabolites, and combinations with multiple species.
  - File types and data products include:
    - Input: .cell and .param (geometry and simulation parameters).
    - Outputs: .out.cell, .out.cif, .castep (CASTEP output).
    - Trajectories: .md (molecular dynamics trajectories).
  - Files are described under a standardized naming convention (Table 1) and file-type descriptions (Table 2). Examples include entries for enrofloxacin, enrofloxacin metabolite, florfenicol, florfenicol metabolite, and various surface-type combinations (e.g., kaoAl_enro, kaoSi_flor, kaoAl_enroflor, etc.).

- **Experimental design and methodology**
  - Geometry optimization performed with CASTEP (first-principles DFT) to optimize antibiotic molecules and kaolinite surfaces.
  - Subsequent molecular dynamics simulations (MD) run using CASTEP; trajectories run for ~10 picoseconds.
  - Data quality ensured via convergence-tested cut-off energies and maintaining Hamiltonian drift below 0.01 eV per atom per second.
  - All relevant input files (.cell, .param) are included to enable replication of the simulations; CASTEP version is recorded in the initial banner of .castep outputs.

- **File formats and how to use them**
  - Text-based inputs and outputs:
    - .param: CASTEP parameter file describing the type of simulation (e.g., geometry optimization, MD) and simulation-specific keywords.
    - .cell: structural input file detailing lattice parameters and atomic coordinates.
    - .out.cif and .out.cell: final structures from optimization and the corresponding optimized cell.
    - .castep: main CASTEP output file; includes calculation parameters, CASTEP version, and citations.
  - MD trajectories:
    - .md: trajectory data containing energies, temperature, atomic coordinates, cell matrix, forces, velocities, stress, etc.
  - Readability and tooling:
    - Text files readable with standard editors (Notepad, etc.).
    - MD trajectories compatible with visualization tools like OVITO (open-source).

- **Reproducibility, access, and licensing**
  - The dataset provides the necessary inputs to reproduce identical CASTEP calculations (subject to CASTEP licensing).
  - CASTEP is a widely used first-principles code available to academics under license; details and access are provided by CASTEP.
  - Documentation within the dataset includes version numbers and references to further information for each file type.

- **Relevance to GIS Specialists**
  - While not a GIS dataset, the work produces mechanistic parameters and trajectories that can inform spatially-explicit environmental models of antibiotic fate in soils.
  - Potential to convert key sorption and interaction metrics into map-based environmental risk assessments (e.g., sorption propensity on mineral surfaces as inputs to soil and groundwater transport models).
  - Highlights data management considerations important for GIS workflows: multi-file datasets, large MD trajectory data, and the need for clear metadata to integrate with spatial datasets.
  - Emphasizes reproducibility and provenance, aiding integration with GIS data pipelines and policy-relevant analyses.

- **Provenance and citation context**
  - Associated with the NERC grant NE/X009572/1, “Antibiotic chemistry in agricultural soils: modelling mineral-antibiotic interactions from first principles.”
  - Data collection occurred in 2023; produced by Dr. Yunqing Wang; HPC resources used include ARC4 (Leeds) and ARCHER2.

- **Notes**
  - The dataset is complete except for calculations that failed.
  - The descriptive tables (Table 1 and Table 2) outline the file handles, descriptions, and the types of files included for each dataset entry.