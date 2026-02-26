# Fire Dynamics Simulator (FDS) Inputs for Wildfire Simulation in a 40x40 m Pinus ponderosa Forest Plot (Sycan Marsh, Oregon)

- Overview
  - A dataset of inputs for wildfire simulations in Fire Dynamics Simulator (FDS) across forest environments, enabling modelling of fire behaviour and the effects of a virtual treatment on fuel structure.

- Dataset Components
  - LAS point clouds (five files) representing segmented fuel classes for a 40x40 m Pinus ponderosa forest plot.
  - BDF bulk density files (associated with each LAS) containing voxel-based bulk density values (10 cm voxel size).
  - FDS input files (three simulations) detailing configurations for different wildfire scenarios.

- Site and Acquisition
  - Location: Sycan Marsh preserve, Klamath Basin, Oregon, USA.
  - Plot: 40 x 40 meters, Pinus ponderosa.
  - Acquisition window: 2019-07-08 to 2019-07-12.
  - Scanning device: Riegl-VZ400i terrestrial laser scanner, near-infrared, mounted on a tripod (min height 1.5 m).

- Processing and Preparation
  - Point cloud segmentation into four fuel classes: grass, shrub, wood (tree stem), and leaf (tree branch+leaves); a virtual pruning treatment also applied to the leaf class.
  - Segmentation performed with custom Deep Learning algorithms (code available at https://github.com/3DFin).
  - Bulk density files generated via a modified Python script to store voxel data in a 2D array, reducing file size; generic bulk density values assigned to fuels per McGrattan et al. (2013).

- Data Formats and Standards
  - LAS: 3D point clouds following ASPRS LAS specifications.
  - BDF: Fortran unformatted binary files mapping bulk density to voxels (10 cm voxels); stored as 2D arrays.
  - FDS: Plain-text input files following NIST FDS conventions (simulation_1.fds, simulation_2.fds, simulation_3.fds).

- Virtual Treatment
  - A “pruning” scenario where all leaf points within 3 meters of ground level are removed to simulate reduced vertical fuel continuity.

- Simulation Scenarios
  - simulation_1.fds: Baseline wildfire simulation using original fuel data.
  - simulation_2.fds: Simulation after applying the virtual pruning treatment.
  - simulation_3.fds: Very high-resolution wildfire simulation for increased detail.

- How to Use the Data
  - Install FDS (from NIST) and run simulations using the provided .fds files (e.g., fds_local simulation_1.fds).
  - Outputs include 3D visualizations and data logs; view results with Smokeview (e.g., smokeview simulation_1).
  - Documentation and guidance are available in the FDS-SMV manuals referenced by NIST.

- Reproducibility and References
  - Segmentation methods and code available via GitHub: https://github.com/3DFin.
  - Bulk density methodology aligns with McGrattan et al. (2013) Fire Dynamics Simulator Users Guide (NIST SP 1019).
  - FDS usage and output analysis guided by NIST FDS-SMV documentation.

- Governance and Data Management Considerations for Data Leaders
  - Diverse data formats (LAS, BDF, FDS) require clear metadata and discoverability for cross-format integration.
  - Standards adherence (LAS ASPRS, NIST FDS) supports interoperability across tools.
  - Reproducibility ensured through explicit configuration files, processing scripts, and published segmentation methods.
  - Data lines of provenance include acquisition details, voxelization parameters (10 cm), and virtual treatment parameters (3 m pruning threshold).
  - Potential for broader reuse in forest fire modelling and cross-site comparative studies, facilitated by documented processing steps and open-source segmentation code.