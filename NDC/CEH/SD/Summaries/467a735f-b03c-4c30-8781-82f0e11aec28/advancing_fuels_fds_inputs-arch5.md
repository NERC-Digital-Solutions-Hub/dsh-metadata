# Summary

## Overview
- Dataset of inputs for wildfire simulations in the Fire Dynamics Simulator (FDS) for forest environments.
- Supports modelling and simulation to understand fire behaviour in forest ecosystems.

## Components and formats
- LAS (point clouds): five segmented files representing different fuel classes (grass, shrub, wood/tree stem, leaf, and leaf after virtual treatment). Follows ASPRS LAS specification.
- BDF (bulk density files): Fortran unformatted binary files encoding bulk density values mapped to the 3D forestplot space; voxelized at 10 cm resolution; stored as a 2D array to reduce size.
- FDS input files: three plain-text FDS configurations (simulation_1.fds, simulation_2.fds, simulation_3.fds) detailing environmental conditions, fuel properties, and ignition points for three scenarios.

## Site and data collection details
- Site: 40 x 40 m Pinus ponderosa forest plot in Sycan Marsh Preserve, Klamath Basin, Oregon, USA.
- Acquisition window: 2019-07-08 to 2019-07-12.
- Instrument: Riegl-VZ400i terrestrial laser scanner (TLS), 750 kHz sampling, vertical sampling density 0.21 degrees, mounted at least 1.5 m above ground.
- Segmentation: four fuel classes plus a virtual pruning treatment; segmentation performed with custom deep learning algorithms; code available at https://github.com/3DFin.

## Data preparation and density files
- Bulk density maps created using a modified script based on FDS User Guide 17.2.2; voxels stored in a 2D array to reduce size.
- Generic bulk density values assigned to different fuels following McGrattan et al. (2013).

## Virtual treatment and scenarios
- Virtual treatment: simulate ladder-down pruning by removing leaf points within 3 m of ground, reducing vertical fuel continuity.
- Simulation variants: baseline (simulation_1), post-treatment (simulation_2), and very high-resolution scenario (simulation_3).

## How to use
- Steps to run an FDS simulation (example with simulation_1.fds):
  - Install FDS from NIST.
  - Open a terminal and navigate to the directory containing the input file.
  - Run: fds_local simulation_1.fds
  - Outputs include 3D visualizations and data logs; view results with Smokeview (smokeview simulation_1).
- Documentation and further guidance are available in the FDS-SMV manuals.

## Provenance and references
- Site description, acquisition details, segmentation approach, and processing described here.
- Reference: McGrattan et al. 2013, Fire Dynamics Simulator Users Guide.

## Considerations for Data Stewards
- Standards and interoperability:
  - LAS files conform to ASPRS LAS specification.
  - BDF uses a 2D voxel-based storage approach derived from a modified FDS workflow.
  - FDS inputs follow NIST-format conventions.
- Metadata and provenance:
  - Detailed site description, acquisition period, instrument specs, and segmentation methods.
  - Virtual treatment parameters clearly defined.
  - Processing workflow and code references (GitHub) provided for reproducibility.
- Quality and lineage:
  - Segmentation performed with custom deep learning algorithms; DL model resources available publicly.
  - Bulk density values mapped to voxels with standardized references (McGrattan 2013).
- Access, reuse, and governance:
  - Clear workflow for reproducibility via FDS; guidance to run simulations and view outputs.
  - Licensing and usage rights are not specified; advisable to document licensing and versioning for future stewardship.
- Challenges to anticipate:
  - Large data volumes (point clouds and voxel densities) and multiple formats requiring interoperability.
  - Ensuring consistency across datasets when updating fuel classes or pruning parameters.
  - Need for ongoing governance to manage updates, metadata completeness, and reprocessing needs.