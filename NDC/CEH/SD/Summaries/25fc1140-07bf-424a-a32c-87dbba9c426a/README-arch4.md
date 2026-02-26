# Filler-induced heterogeneous nucleation of polymer crystals investigated by molecular dynamics simulations

- The dataset contains input files for a publication on molecular dynamics simulations of polymer nucleation, performed with LAMMPS (version lammps/intel-2020.4/29Sep2021).
- Outputs include a generated data file and a LAMMPS trajectory with unwrapped coordinates.
- Publication reference: Dominic Wadkin-Snaith, Paul Mulheran, Karen Johnston, Polymer, 2023, 126113 (DOI provided).

## Data assets included

- Two essential files to run simulations:
  - Input file (named in.*)
  - Molecule template file (named *.txt) or a data file named data.*
- A data file is produced at the end of each simulation; a trajectory file is produced as well.
- The dataset covers multiple simulation conditions (temperatures/enthalpy changes via cooling/heating, and different rates).

## Folder and file structure

- Top-level split into:
  - two_wall_systems (surface-present systems)
  - bulk_systems (fully periodic, no surfaces)
- Each type contains:
  - cooling and heating subfolders
  - within those, rate subfolders: 0.25Gamma0, 0.5Gamma0, Gamma0, 2Gamma0, 10Gamma0
- Additional subdivisions:
  - bulk_systems: chain stiffness subfolders k1, k2, k2.4, k3, k4
  - two_wall_systems: chain stiffness and wall strength combinations, e.g., k2.4_wall090, k2.4_wall180, k2.4_wall270
- Note: surface (two_wall_systems) simulations were only performed for chain stiffness ktheta=2.4.
- Example paths:
  - bulk_systems > cooling > Gamma0 > k3 > {chainfinaltest.txt, in.cool}
  - two_wall_systems > heating > 2Gamma0 > k2.4_wall180 > {data.quench_npt, in.heat}

## Reproduction and reuse

- To reproduce, run with two required inputs:
  - in.* (simulation box, geometry, forcefield, ensemble)
  - data template (*.txt) or data.* (polymer chain coordinates)
- Outputs to expect:
  - data file at the end of the run
  - LAMMPS trajectory file using unwrapped coordinates

## Metadata, provenance, and referencing

- Parameters reflected in folder structure and file naming:
  - cooling/heating modes
  - cooling/heating rates (e.g., Gamma0, 2Gamma0)
  - chain stiffness values (ktheta: 1, 2, 2.4, 3, 4)
  - wall interaction strengths (epsilon_w values in wall-system folders)
- Publication reference included with DOI for traceability.
- The dataset links directly to the published study, enabling contextual understanding of simulation settings.

## Considerations for Data Leaders

- Strengths:
  - Clear, hierarchical organization by system type, process (cooling/heating), rate, and material parameters.
  - Explicit pairings of input and template/data files facilitate reproducibility.
  - Includes both inputs and outputs (data file and trajectory), enabling reanalysis and validation.
- Opportunities for improvement:
  - Provide explicit metadata descriptors (units, parameter definitions, seeds) in a centralized metadata file.
  - Adopt standardized data schemas or schemas extensions to improve interoperability across similar datasets.
  - Ensure long-term accessibility and licensing information for reuse beyond the publication.