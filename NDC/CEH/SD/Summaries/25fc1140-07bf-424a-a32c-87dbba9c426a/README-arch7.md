# Filler-induced heterogeneous nucleation of polymer crystals investigated by molecular dynamics simulations

## Overview
- All simulations were performed with LAMMPS version lammps/intel-2020.4/29Sep2021.
- The dataset contains the input files for the publication describing molecular dynamics simulations of filler-induced heterogeneous nucleation in polymers.
- Outputs include a data file generated at the end of each simulation and a LAMMPS trajectory file with unwrapped coordinates.

## Dataset structure
- Top-level folders:
  - two_wall_systems (surfaces/wall potentials at top and bottom of the cell)
  - bulk_systems (fully periodic without surfaces)
- Each top-level folder contains subfolders for cooling and heating, which are further subdivided by rate:
  - 0.25Gamma0, 0.5Gamma0, Gamma0, 2Gamma0, 10Gamma0
- In bulk_systems, additional subdivisions indicate chain stiffness:
  - k1 (ktheta = 1)
  - k2 (ktheta = 2)
  - k2.4 (ktheta = 2.4)
  - k3 (ktheta = 3)
  - k4 (ktheta = 4)
- In two_wall_systems, subdivisions specify chain stiffness and wall interaction strength, e.g.:
  - k2.4_wall090, k2.4_wall180, k2.4_wall270
- Note: surface (two_wall_systems) simulations only include ktheta = 2.4.

## File types and contents
- Required to run:
  - input file, named in.*
  - molecule template file, named *.txt or a data file named data.*
- Outputs:
  - a data file generated at the end of the simulation
  - a LAMMPS trajectory file using unwrapped coordinates

## Example directory paths
- Bulk system example (k = 3, cooling, Gamma0):
  - bulk_systems > cooling > Gamma0 > k3 > {chainfinaltest.txt, in.cool}
- Surface system example (k = 2.4, wall strength 1.8, heating, 2Gamma0):
  - two_wall_systems > heating > 2Gamma0 > k2.4_wall180 > {data.quench_npt, in.heat}

## Reproducibility and references
- References: Dominic Wadkin-Snaith, Paul Mulheran, Karen Johnston, Filler-induced heterogeneous nucleation of polymer crystals investigated by molecular dynamics simulations, Polymer, Volume 281, 2023, 126113, https://doi.org/10.1016/j.polymer.2023.126113

## Notes for GIS-oriented reuse
- The dataset is organized by hierarchical folders encoding simulation parameters (system type, phase change condition, rate, chain stiffness, wall interaction), which mirrors how geospatial data can be layered by parameter sets.
- Filenames and folder names encode key metadata (e.g., kt theta, wall strength, rate), enabling parametric querying and map-like visualization of parameter spaces.
- To reuse in GIS-like workflows, extract and index the parameter values from folder/file names to build a structured metadata catalog for visual exploration of how different conditions affect simulation outcomes.