# Filler-induced heterogeneous nucleation of polymer crystals investigated by molecular dynamics simulations

## Overview
- Dataset containing input files for a published molecular dynamics study on filler-induced heterogeneous nucleation in polymers.
- Simulations run with LAMMPS (version specified: lammps/intel-2020.4/29Sep2021).
- Aims to enable reproduction and analysis of how cooling/heating rates, chain stiffness, and wall interactions affect nucleation.

## Dataset structure and contents
- Two main system categories:
  - two_wall_systems: surfaces (wall) potentials at the top and bottom of the simulation cell.
  - bulk_systems: fully periodic systems without surfaces.
- Within each category:
  - Cooling and heating subfolders.
  - Subfolders for cooling/heating rates: 0.25Gamma0, 0.5Gamma0, Gamma0, 2Gamma0, 10Gamma0 (bulk_systems only Gamma0Cooling/Heating are used).
- Chain stiffness variants:
  - bulk_systems: k1, k2, k2.4, k3, k4 (ktheta values 1, 2, 2.4, 3, 4).
  - two_wall_systems: same stiffness variants plus wall interaction strength indicators (e.g., k2.4_wall090, k2.4_wall180, k2.4_wall270 corresponding to epsilon_w = 0.9, 1.8, 2.7).
- Surface simulations: only ktheta = 2.4 used.
- Each directory contains:
  - An input file named in.* detailing box dimensions, geometry, forcefields, and ensemble settings.
  - A molecule template file (named *.txt) or a data file named data.* describing polymer chain coordinates.
- Outputs:
  - A data file generated at the end of the simulation.
  - A LAMMPS trajectory file with unwrapped coordinates.

## How to locate and reproduce examples
- Bulk system example: bulk_systems > cooling > Gamma0 > k3 > {chainfinaltest.txt, in.cool}
- Surface system example: two_wall_systems > heating > 2Gamma0 > k2.4_wall180 > {data.quench_npt, in.heat}
- Each example includes the input and molecule template/data files necessary to run the simulation.

## Files and running prerequisites
- Essential files:
  - Input file: in.* (specifies simulation box, geometry, potentials, ensemble)
  - Molecule template: chain template *.txt or data file data.* (polymer bead coordinates)
- No additional files are required beyond these two to run a simulation, with outputs produced as described.

## Reproducibility and reference
- Publication associated: Filler-induced heterogeneous nucleation of polymer crystals investigated by molecular dynamics simulations, Polymer, 2023 (Wadkin-Snaith, Mulheran, Johnston; DOI provided in references).
- Versioning and provenance:
  - LAMMPS version and environment details are specified.
  - Explicit directory structure and naming conventions enable consistent replication of scenarios across rates, stiffness, and wall interactions.

## Relevance to environmental monitoring and data use
- Demonstrates how standardized, well-documented simulation inputs and data outputs enable transparent tracking of environmental conditions modeled at the molecular level.
- Aligns with monitoring goals by:
  - Providing verified, well-structured data that can be stored, searched, and re-used.
  - Facilitating comparison across simulation conditions (rates, stiffness, surface interactions) to assess how micro-environmental factors influence nucleation phenomena.
  - Emphasizing reproducibility through explicit file naming, versioning, and a clear data-output pipeline.

## Reference
- Dominic Wadkin-Snaith, Paul Mulheran, Karen Johnston, Filler-induced heterogeneous nucleation of polymer crystals investigated by molecular dynamics simulations, Polymer, Volume 281, 2023, 126113, https://doi.org/10.1016/j.polymer.2023.126113