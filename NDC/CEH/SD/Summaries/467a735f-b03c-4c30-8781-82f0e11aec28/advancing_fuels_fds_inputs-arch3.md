# Summary

- Purpose and relevance for monitoring frameworks
  - Provides reproducible inputs for wildfire simulations to evaluate fire behaviour, assess risk, and inform policy decisions and future management actions.
  - Emphasizes data provenance, transparency, and open access to support governance, evaluation of fuel treatment scenarios, and decision-making.

- Data components
  - LAS files (five): segmented 3D point clouds representing different forest fuel classes (grass, shrub, tree stem, tree branch+leaves, and a pruned leaf class leaf_crop_high). Collected from a 40 x 40 m Pinus ponderosa plot in Sycan Marsh, Oregon, using a Riegl-VZ400i TLS; LAS follows ASPRS specifications.
  - BDF files (bulk density): Fortran unformatted binary files encoding voxelized bulk density values (10 cm voxels) mapped to the LAS space; each BDF corresponds to a LAS segment and represents biomass density (g/cm^3) per voxel. A modified Python script stores voxels in a 2D array to reduce file size; generic bulk density values are assigned to fuel types.
  - FDS input files: simulation_1.fds, simulation_2.fds, simulation_3.fds defining three wildfire simulation configurations for the same forest plot (baseline, post-virtual treatment, and very high-resolution scenario).

- Site description
  - Sycan Marsh preserve in the Klamath Basin, Oregon, USA (over 8000 hectares), featuring marshland and surrounding forest; dataset focuses on a 40 x 40 m Pinus ponderosa plot within the preserve.

- Acquisition and processing details
  - Point cloud acquisition: conducted 2019-07-08 to 2019-07-12 using a RIEGL-VZ400i TLS, 750 kHz sampling rate, vertical density 0.21 degrees, mounted at ≥1.5 m height; maximum range 2000 m.
  - Point cloud segmentation: four fuel classes (grass, leaves, shrub, wood) with a virtual pruning treatment applied to create leaf_crop_high; segmentation performed using custom deep learning algorithms (code at https://github.com/3DFin).
  - Bulk density creation: voxelization at 10 cm, bulk density values assigned to voxels; BDF files generated with a modified 2D-voxel storage approach to reduce size; generic density values drawn from established literature (McGrattan et al., 2013).

- Virtual treatment and simulation scenarios
  - Virtual treatment: simulates pruning by removing leaf points within 3 meters of ground level to reduce vertical fuel continuity.
  - Simulation scenarios: 
    - simulation_1.fds – baseline wildfire scenario.
    - simulation_2.fds – scenario after virtual treatment.
    - simulation_3.fds – very high-resolution wildfire simulation.

- How to use the data
  - Prerequisites: install Fire Dynamics Simulator (FDS) from NIST, ensure environment is set up.
  - Running a simulation: navigate to the folder containing simulation_1.fds and run fds_local simulation_1.fds.
  - Outputs: FDS generates 3D visualizations, logs, and results; visualize with Smokeview (e.g., smokeview simulation_1).
  - Documentation and support: FDS-SMV manuals and NIST resources linked in the dataset description.

- Metadata, governance, and transparency considerations
  - Dataset provenance includes acquisition date, equipment, voxel size, segmentation methods, and transformation steps (e.g., pruning threshold).
  - Open data practices are demonstrated through explicit file formats (LAS, BDF, FDS) and public code references; a clarifying note on data transformation and storage practices highlights editorial considerations for reuse and governance.

- References
  - McGrattan, K., McDermott, R., Weinschenk, C., and Forney, G. (2013). Fire Dynamics Simulator Users Guide, Sixth Edition, NIST SP. Includes DOI and online access.