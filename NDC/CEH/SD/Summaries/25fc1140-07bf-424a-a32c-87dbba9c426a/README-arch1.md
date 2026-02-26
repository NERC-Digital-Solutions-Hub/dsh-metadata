# Filler-induced heterogeneous nucleation of polymer crystals investigated by molecular dynamics simulations

## Overview
- Dataset containing input files for the publication on filler-induced heterogeneous nucleation of polymer crystals studied via molecular dynamics.
- Simulations performed with LAMMPS version lammps/intel-2020.4/29Sep2021.
- The dataset supports reproducibility and cross-comparison across system types, chain stiffness, surface interactions, and thermal protocols.

## Dataset structure

- Two main system categories:
  - two_wall_systems: surfaces (wall) potentials at top and bottom of the simulation cell.
  - bulk_systems: fully periodic (no surfaces).
- Each category includes cooling and heating subfolders, with further subdivisions by rate:
  - Rates: 0.25Gamma0, 0.5Gamma0, Gamma0, 2Gamma0, 10Gamma0.
  - Note: bulk_systems only include Gamma0 cooling/heating.
- Chain stiffness classifications (in bulk_systems):
  - k1 (ktheta=1), k2 (ktheta=2), k2.4 (ktheta=2.4), k3 (ktheta=3), k4 (ktheta=4).
- Surface systems (two_wall_systems) further subdivided by chain stiffness and wall strength:
  - Examples: k2.4_wall090 (ktheta=2.4, epsilon_w=0.9), k2.4_wall180 (ktheta=2.4, epsilon_w=1.8), k2.4_wall270 (ktheta=2.4, epsilon_w=2.7).
- Surface simulations are limited to ktau=2.4 for the chain stiffness.

## Files and content

- Each simulation requires two files:
  - input file: named in.*
  - molecule template file: named *.txt or a data file named data.*.
- Input file contents: simulation box dimensions, geometry, forcefield potentials, and ensemble to run.
- Molecule template file contents: coordinates of all beads for a single polymer chain.
- Outputs: a data file generated at the end of the simulation and a LAMMPS trajectory with unwrapped coordinates.

## How to navigate and reproduce (examples)

- Bulk system example (ktheta=3, cooling at Gamma0):
  - Path: bulk_systems > cooling > Gamma0 > k3 > {chainfinaltest.txt, in.cool}
  - chainfinaltest.txt = molecule template; in.cool = input file.
- Surface system example (ktheta=2.4, wall strength epsilon_w=1.8, heating at 2Gamma0):
  - Path: two_wall_systems > heating > 2Gamma0 > k2.4_wall180 > {data.quench_npt, in.heat}
  - data.quench_npt = data file; in.heat = input file.

## Output products and metadata

- For each run, a data file (final state) and a trajectory file (with unwrapped coordinates) are produced.
- The dataset is organized to enable analysis of how cooling/heating rate, chain stiffness, and wall interactions influence nucleation.

## Software and provenance

- LAMMPS version: lammps/intel-2020.4/29Sep2021.

## Reference

- Wadkin-Snaith, Dominic; Mulheran, Paul; Johnston, Karen. Filler-induced heterogeneous nucleation of polymer crystals investigated by molecular dynamics simulations. Polymer, 2023, 126113. DOI: https://doi.org/10.1016/j.polymer.2023.126113

## Considerations for data analysts

- Enables correlating thermal protocol, chain stiffness, and surface interactions with nucleation outcomes.
- Access to both input and template/data files supports reruns, validation, and extraction of model parameters.
- Be mindful of limitations:
  - Surface simulations limited to kt=2.4.
  - Bulk simulations available only for Gamma0 cooling/heating.