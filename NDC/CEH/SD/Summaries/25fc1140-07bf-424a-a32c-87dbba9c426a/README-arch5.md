# This dataset contains the input files for the publication "Filler-induced heterogeneous nucleation of polymer crystals investigated by molecular dynamics simulations"

## Overview
- Dataset of molecular dynamics simulations prepared for the publication on filler-induced heterogeneous nucleation of polymer crystals.
- Simulations were performed using LAMMPS (version lammps/intel-2020.4/29Sep2021).
- The dataset documents the input and template files used to generate end-of-simulation data and trajectories.

## Dataset structure
- Top-level folders:
  - two_wall_systems (surfaces/wall potentials at top and bottom)
  - bulk_systems (fully periodic, no surfaces)
- Within each top-level folder:
  - cooling
  - heating
  - Each of these contains subfolders named by cooling/heating rates, such as:
    - 0.25Gamma0, 0.5Gamma0, Gamma0, 2Gamma0, 10Gamma0
- Additional organization:
  - bulk_systems contains subfolders for different chain stiffnesses:
    - k1, k2, k2.4, k3, k4
  - two_wall_systems contains subfolders for chain stiffness and wall strength combinations, e.g.:
    - k2.4_wall090, k2.4_wall180, k2.4_wall270
- Note: surface simulations only include chain stiffness ktheta=2.4.

## Contents and file types
- Each system/subfolder contains:
  - An input file named in.* (details simulation box, geometry, forcefield potentials, and ensemble)
  - A molecule template file named *.txt or a data file named data.* (coordinates for a single polymer chain)
- Outputs:
  - A data file generated at the end of the simulation
  - A LAMMPS trajectory file using unwrapped coordinates

## Accessing specific files (examples)
- Bulk system example:
  - Path: bulk_systems > cooling > Gamma0 > k3 > {chainfinaltest.txt, in.cool}
  - Files: in.cool (input), chainfinaltest.txt (molecule template)
- Surface system example:
  - Path: two_wall_systems > heating > 2Gamma0 > k2.4_wall180 > {data.quench_npt, in.heat}
  - Files: in.heat (input), data.quench_npt (data file)

## Software version
- LAMMPS version used: lammps/intel-2020.4/29Sep2021
- LAMMPS manual: https://docs.lammps.org/Manual.html

## Publication reference
- Wadkin-Snaith, Dominic; Mulheran, Paul; Johnston, Karen. Filler-induced heterogeneous nucleation of polymer crystals investigated by molecular dynamics simulations. Polymer, Volume 281, 2023, 126113. https://doi.org/10.1016/j.polymer.2023.126113

## Governance and provenance notes (Data Steward perspective)
- Clear, hierarchical folder structure facilitates discovery and intended reuse across multiple system types (bulk vs surface) and conditions (cooling vs heating, rate variations, stiffness, and wall interactions).
- Explicit metadata encoded in folder and file naming conventions (rates, stiffnesses, and wall strengths) supports traceability to the corresponding simulation scenarios.
- Reproducibility is supported by including both the input (in.* or in.heat) and the polymer template/data file required to run simulations.
- Outputs (data file and unwrapped trajectory) are produced to enable further analysis and verification.
- The documentation includes a precise reference to the publication, aiding proper attribution.
- Potential enhancements for stewardship (not described in the document): consider adding a README with a complete metadata schema, versioning notes, and a data usage/license statement to further improve discoverability, access permissions, and long-term preservation.