# All of the simulations for this publication were performed with LAMMPS version lammps/intel-2020.4/29Sep2021

## Overview
- This dataset contains the input files for the publication “Filler-induced heterogeneous nucleation of polymer crystals investigated by molecular dynamics simulations.”
- Simulations were performed using LAMMPS (details and manual link provided).

## Dataset structure
- two_wall_systems: contains surface (wall) potentials at the top and bottom of the simulation cell.
  - Subdivided by chain stiffness and wall interaction strength (e.g., k2.4_wall090, k2.4_wall180, k2.4_wall270).
  - Note: surface simulations included only chain stiffness ktheta = 2.4.
- bulk_systems: fully periodic systems without surfaces.
  - Subdivided into cooling and heating, each with multiple rate subfolders.
  - Rate subfolders include: 0.25Gamma0, 0.5Gamma0, Gamma0, 2Gamma0, 10Gamma0.
  - Within bulk_systems, further subdivided by chain stiffness: k1, k2, k2.4, k3, k4 (corresponding to ktheta values).

## File conventions
- Each run requires two files:
  - Input file named in.*
  - Molecule template file named *.txt or a data file named data.*
- Outputs:
  - A data file is generated at the end of the simulation.
  - A LAMMPS trajectory file is produced using unwrapped coordinates.

## Path examples
- Bulk system (k=3, cooling, Gamma0): bulk_systems > cooling > Gamma0 > k3 > {chainfinaltest.txt, in.cool}
- Surface system (k=2.4, wall strength 1.8, heating, 2Gamma0): two_wall_systems > heating > 2Gamma0 > k2.4_wall180 > {data.quench_npt, in.heat}

## Reference
- Wadkin-Snaith, Mulheran, Johnston, “Filler-induced heterogeneous nucleation of polymer crystals investigated by molecular dynamics simulations,” Polymer, 2023, 126113.
- LAMMPS documentation: https://docs.lammps.org/Manual.html