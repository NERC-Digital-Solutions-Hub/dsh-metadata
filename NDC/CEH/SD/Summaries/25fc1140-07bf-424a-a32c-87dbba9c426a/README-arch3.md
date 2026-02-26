# Filler-induced heterogeneous nucleation of polymer crystals investigated by molecular dynamics simulations

## Purpose and scope
- Provides input and data files for a publication investigating filler-induced heterogeneous nucleation of polymer crystals via molecular dynamics (MD) simulations using LAMMPS.
- Compares bulk systems (fully periodic) and two-wall surface systems, across cooling and heating processes and multiple rate settings, with varying chain stiffness and wall interaction strengths.

## Dataset structure
- Root is organized into two main branches:
  - bulk_systems: fully periodic systems (no surfaces).
  - two_wall_systems: systems with surfaces (walls) at top and bottom.
- Each branch subdivides by process and parameters:
  - Processes: cooling and heating.
  - Rates: 0.25Gamma0, 0.5Gamma0, Gamma0, 2Gamma0, 10Gamma0 (bulk_systems includes Gamma0 only for cooling/heating).
- Chain stiffness subfolders:
  - bulk_systems: k1, k2, k2.4, k3, k4 (ktheta values).
  - two_wall_systems: combinations of chain stiffness and wall strength, e.g., k2.4_wall090, k2.4_wall180, k2.4_wall270 (only ktheta=2.4 used for surface simulations).

## Files and contents
- Each subfolder contains:
  - in.*: the MD input file specifying simulation box, geometry, forcefield, and ensemble.
  - a molecule template file: either *.txt (coordinates of a single polymer chain) or a data file named data.*.
- Outputs generated:
  - a data file capturing simulation results.
  - a LAMMPS trajectory file with unwrapped coordinates.

## Running simulations (workflow)
- The dataset is designed to require only two files to run per simulation:
  - input file (in.*) and molecule template (or data file).
- Example paths:
  - bulk system, k=3, cooling at Gamma0: bulk_systems > cooling > Gamma0 > k3 > {chainfinaltest.txt, in.cool}
  - surface system, k=2.4, wall strength 1.8, heating at 2Gamma0: two_wall_systems > heating > 2Gamma0 > k2.4_wall180 > {data.quench_npt, in.heat}
- The input file defines simulation box, geometry, forcefield potentials, and ensemble; the template defines polymer chain coordinates.

## Software and reproducibility
- Simulations performed with LAMMPS: lammps/intel-2020.4/29Sep2021.
- Documentation reference: LAMMPS Manual (https://docs.lammps.org/Manual.html).

## Data provenance and governance
- Provisions for reproducibility via explicit directory naming that encodes key parameters (process, rate, chain stiffness, wall strength).
- Data and metadata are organized to enable replication of specific cases (e.g., bulk vs. surface, different stiffnesses and wall interactions).
- Note: potential barriers to data sharing noted in broader monitoring contexts (metadata completeness, data governance) but mitigated here by explicit file naming and standardized input/template files.

## Publication and references
- Related publication: Wadkin-Snaith, Mulheran, Johnston, Filler-induced heterogeneous nucleation of polymer crystals investigated by molecular dynamics simulations, Polymer, 2023, 126113. DOI: https://doi.org/10.1016/j.polymer.2023.126113