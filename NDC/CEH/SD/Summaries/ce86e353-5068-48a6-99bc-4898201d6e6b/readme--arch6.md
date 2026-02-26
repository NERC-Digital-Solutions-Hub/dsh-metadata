# Sorption simulation data of veterinary antibiotic interactions with kaolinite surfaces

- Context and purpose:
  - Data from the NERC grant “Antibiotic chemistry in agricultural soils: modelling mineral-antibiotic interactions from first principles” (Grant NE/X009572/1).
  - Comprises input and output files from first-principles molecular dynamics studying kaolinite interactions with four veterinary antibiotics: enrofloxacin, florfenicol, ciprofloxacin (metabolite of enrofloxacin), and florfenicol amine (metabolite of florfenicol).
  - Provides insight into sorption dynamics of veterinary medicines on a soil mineral (kaolinite) and relates to environmental contaminants and antimicrobial resistance (AMR).
  - Collected in 2023 on Leeds ARC4 and ARCHER2; dataset largely complete aside from some failed calculations; curated by PDRA Dr Yunqing Wang.

- Experimental design:
  - Geometry optimization of kaolinite surfaces and antibiotics using CASTEP (first-principles DFT).
  - Antibiotics placed above kaolinite surfaces (Al-terminated or Si-terminated) as single molecules or in pairs; followed by first-principles MD simulations (~10 ps) also in CASTEP.
  - Data quality ensured with convergence-tested cut-off energies and low Hamiltonian drift (<0.01 eV s⁻¹ per atom) during MD.
  - All input files (.cell, .param) included; CASTEP version shown in initial banner of .castep outputs.

- Data included:
  - CASTEP-optimized molecules and MD trajectories for all successful simulations.
  - File naming follows the conventions described in Table 1; Table 2 lists file types and descriptions.
  - Key file groups:
    - enrofloxacin_cat, enrofloxacin metabolite (enrofloxacin_m1_cat), florfenicol_cat, florfenicol_m1_ca, and related metabolite/surface combinations.
    - Surfaces: kaoAl_… (Al-terminated) and kaoSi_… (Si-terminated) for each antibiotic or metabolite.
    - Complex systems: various combinations of antibiotics and metabolites on Al- or Si-terminated kaolinite (e.g., kaoAl_enroflor, kaoAl_metmet, kaoSi_enroflor, etc.).
  - File types described in Table 2, including: .param (simulation parameters), .cell (structural input), .out.cif (final optimized structure), .out.cell (final optimized structure in cell format), .castep (main CASTEP output), .md (molecular dynamics trajectory).

- File formats and how to use:
  - Text-based inputs/outputs: .param, .cell, .out.cif, .out.cell are readable in standard text editors.
  - CASTEP trajectory: .md files contain energies, temperature, coordinates, cell derivatives, forces, velocities, stress, and pressure; can be analyzed with compatible visualization tools.
  - Visualization guidance: OVITO is recommended for MD trajectories; CASTEP version information is included in .castep outputs.

- Contextual notes:
  - The dataset supports exploration of sorption dynamics on mineral surfaces, comparative analysis of Al-terminated vs Si-terminated kaolinite, and assessment of interactions involving antibiotics and their metabolites.
  - Aimed at enabling reproducibility and potential re-use for related environmental modelling and AMR research.