# Outburst flood simulations of various dam failure scenarios from Tsho Rolpa glacial lake, Nepal, 2020: supporting document

## Overview
- 12 GLOF scenarios simulated using a simple dam breach model to generate breach flow results.
- A high-performance 2-D hydrodynamic model (depth-averaged shallow water equations) simulates flood flow after breaches.
- Data covers downstream area of Tsho Rolpa Lake, Nepal (coordinates provided) with map projection WGS 1984 Transverse Mercator.

## Data content
- Data set comprises:
  - 1 CSV file: Breach_flow_under_different_GLOF_scenarios
  - 24 TIFF files: 12 TIFFs for maximum water depth (one per scenario) and 12 TIFFs for maximum water velocity (one per scenario).
- CSV structure: 25 columns – Time (s) as the first column; 12 depth values (one per scenario) as the next 12 columns; 12 discharge values (one per scenario) as the final 12 columns.

## Data structure and formats
- Spatial outputs are provided as georeferenced TIFF rasters (depth and velocity) corresponding to each scenario.
- Temporal data captured in the CSV includes time series of depth and discharge per scenario.

## Methods and model details
- Collection method: numerical modeling using a fully hydrodynamic 2-D SWEs model, solved with a finite volume Godunov-type scheme with shock-capturing.
- Parallel computation employed via CUDA on GPUs to enable large-scale simulations.
- Model features emphasize mass and momentum conservation with minimal parameters; no external validation performed.

## Variables and units
- Units:
  - Water depth: meters
  - Flow velocity: meters per second
  - Time: seconds
- Outputs include maximum water depth and maximum flow velocity per scenario derived from simulation time series.

## Quality, validation, and limitations
- Calibration/validation: No validation performed; justification rests on model simplicity and prior applications.
- Implications: users should treat results as scenario-based projections with the caveat of lacking empirical validation and potential sensitivity to chosen parameters (e.g., roughness, bed elevation).

## Data governance considerations for Data Leaders
- Data provenance: outputs come from a consistent hydrodynamic modeling framework; includes both depth and velocity fields across all scenarios.
- Documentation needs: ensure metadata links each TIFF/CSV to its specific scenario, breach depth, water level, and initial conditions.
- Discoverability and accessibility: dataset is split across one CSV and multiple TIFF files; maintain a catalog that maps scenario identifiers to file names and spatial extents.
- Metadata completeness: include coordinate system, projection, spatial resolution, time steps, and parameter choices (e.g., Manning n, bed elevation z_b).
- Data quality planning: consider adding a validation plan or notes on expected uncertainties to improve trustworthiness and enabling cross-team reuse.
- Reuse considerations: suitable for hazard assessment, scenario planning, and cross-agency risk discussions; may require alignment with other data layers (topography, infrastructure, population).

## Potential use cases for policy and data teams
- Flood risk assessment and scenario planning for downstream communities.
- Comparative analysis of how varying breach depths and water levels influence inundation extent and peak velocities.
- Cross-team collaboration on data standards, metadata schemas, and data dissemination practices for similar hydrodynamic datasets.

## Next steps and recommendations
- Enhance metadata: explicitly document scenario mappings, file naming conventions, resolution, time steps, and parameter values used in simulations.
- Consider validation: where feasible, incorporate limited validation checks or align with existing validated models to bolster confidence.
- Establish data governance: create a data catalog entry, versioning, and access controls to improve discoverability and future updates.