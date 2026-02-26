# Summary

- This dataset provides inputs for wildfire simulations in Fire Dynamics Simulator (FDS) within forest environments, supporting modelling and analysis of fire behaviour in forest ecosystems.

## Dataset scope and purpose
- Five segmented LAS point clouds representing different fuel classes in a 40 x 40 m Pinus ponderosa forest plot.
- Each LAS has an associated BDF (bulk density file) detailing voxelized bulk density values.
- Three FDS input files define separate simulation configurations (three scenarios).

## Spatial extent and site
- Location: Sycan Marsh preserve, Klamath Basin, Oregon, USA.
- Site description: Large wetlands area (>8000 ha) with surrounding forested areas; the forest plot is a 40 x 40 m area within the preserve.

## Data formats and components
- LAS: High-resolution 3D point clouds following ASPRS LAS specification.
  - grass_crop.las, shrub_crop.las, wood_crop.las, leaf_crop.las, leaf_crop_high.las (the latter after virtual pruning treatment).
- BDF: Fortran unformatted (binary) bulk density files aligned with each LAS; voxelized at 10 cm resolution; stored initially as 3D voxels but later converted to a 2D array to reduce size.
- FDS: Three input files (simulation_1.fds, simulation_2.fds, simulation_3.fds) detailing environmental conditions, fuel properties, and ignition points for three scenarios.

## Data acquisition and segmentation
- Point cloud acquisition: 2019-07-08 to 2019-07-12 using RIEGL-VZ400i TLS; 750 kHz laser sampling rate; vertical sampling density 0.21 degrees; mounted ≥1.5 m high; near-infrared 1050 nm; max range ~2000 m.
- Segmentation: Four fuel classes (grass, leaves, shrub, wood) with an additional virtual pruning treatment applied to leaves; segmentation performed using custom deep learning algorithms (code available at https://github.com/3DFin).

## Bulk density and processing details
- BDF creation: Based on a modified Python script (inspired by FDS User Guide 17.2.2); voxelized at 10 cm, with densities assigned from generic vegetation values (McGrattan et al. 2013).
- Virtual treatment: Simulates pruning by removing all leaf points within 3 meters of ground level, reducing vertical fuel continuity.

## How to run FDS simulations (GIS workflow)
- Prerequisite: Install Fire Dynamics Simulator (FDS) from NIST.
- Steps:
  - Open a terminal and navigate to the directory containing simulation_1.fds (or another .fds file).
  - Run: fds_local simulation_1.fds
  - After completion, view outputs (3D visualizations, logs) with Smokeview: smokeview simulation_1
- Outputs: 3D visualizations, data logs, and other results for analyzing forest fire dynamics.
- Documentation and references: FDS-SMV manuals on NIST site.

## GIS considerations and potential uses
- Multi-format data integration: aligns LAS point clouds with 10 cm voxel BDF data for spatially explicit fuel modeling.
- Supports scenario analysis: baseline vs. virtual treatment (pruning) and a high-resolution scenario.
- Useful for risk mapping, fuel load assessment, and spatial-fire modelling workflows in GIS environments.

## References
- McGrattan, K., McDermott, R., Weinschenk, C. and Forney, G. (2013). Fire Dynamics Simulator Users Guide, Sixth Edition, NIST SP. Online: https://doi.org/10.6028/NIST.sp.1019.