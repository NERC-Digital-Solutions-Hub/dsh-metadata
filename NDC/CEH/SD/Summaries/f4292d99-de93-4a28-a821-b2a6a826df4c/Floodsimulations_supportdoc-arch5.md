# Outburst flood simulations of various dam failure scenarios from Tsho Rolpa glacial lake, Nepal, 2020: supporting document

## Overview
- Provides dam breach and flood hydrodynamics data for 12 GLOF scenarios from Tsho Rolpa Lake, Nepal, using a simple dam breach model followed by a high-performance 2-D hydrodynamic simulation.
- Data focus: downstream area (27°30′–27°51′ N, 86°10′–86°29′ E) with map projection WGS 1984 Transverse Mercator.
- Supports analysis of maximum inundation depth and maximum flow velocity across scenarios.

## Data Content and Formats
- Files:
  - 1 CSV file: Breach_flow_under_different_GLOF_scenarios
  - 24 TIFF files: 12 for maximum water depth (one per scenario) and 12 for maximum water velocity (one per scenario)
- CSV structure:
  - 25 columns total
  - First column: Time (s)
  - Next 12 columns: water depth of dam breach flow under each scenario
  - Last 12 columns: discharge (unit-width) of dam breach flow under each scenario
- Units:
  - Water depth: meters
  - Flow velocity: meters per second
  - Time: seconds
- Scenario details:
  - 12 GLOF scenarios with varying final breach depths and water levels
  - Includes maximum depth/velocity results and corresponding times from the simulations
- Visualization:
  - Figure 1 presents maximum inundation depth and maximum flow velocity for the worst-case scenario along the main channel from the lake to Manthali

## Data Generation Methods
- Hydrodynamic modeling approach:
  - 2-D depth-averaged shallow water equations (SWEs) to simulate flood processes after dam breach
  - Governing equations implemented in a conservative, Godunov-type finite-volume scheme with automatic shock-capturing
  - Parallelized for high-performance computing on GPUs using NVIDIA CUDA
- Calibration and validation:
  - No validation performed; the study relies on the conservation-based SWE model and prior successful applications
  - Calibration steps and parameter values are minimal and not detailed beyond essential terms
- Analytical processing:
  - Maximum water depth and maximum flow velocity are extracted from the time-series simulation outputs

## Data Structure and Access
- Data composition:
  - 1 CSV file with 25 columns
  - 24 TIFF files: 12 depth maps (one per scenario) and 12 velocity maps (one per scenario)
- Content focus:
  - Depth maps reflect the maximum water depth for each scenario
  - Velocity maps reflect the maximum flow velocity for each scenario

## Quality, Uncertainty, and Limitations
- No validation is reported; reliance on the model’s mass/momentum conservation and prior use for justification
- Users should be aware of potential uncertainties due to lack of empirical validation and the inherent limitations of the underlying 2-D SWE model
- Data interoperability considerations arise from using a mix of CSV and TIFF formats for multi-scenario outputs

## Provenance and Metadata Considerations for Data Stewards
- Key provenance elements to capture:
  - Data creators/authors, date of creation, and project context (GLOF scenarios at Tsho Rolpa Lake)
  - Model details: 2-D SWEs, Godunov-type scheme, Manning roughness (Cf) expression, bed elevation z_b, and other parameters
  - Computational platform: GPU/CUDA implementation
  - Data location and projection: downstream area coordinates; WGS 1984 Transverse Mercator
  - Data products: per-scenario maximum depth and maximum velocity, plus time-series provenance
- Recommended metadata fields:
  - Abstract/summary, purpose, geographic extent, coordinate reference system, unit definitions, variable definitions, data dictionary, file naming conventions, versioning, access/authors, lineage, and any known limitations
  - Update and maintenance policies (if future updates are planned)
  - Software and scripts used for generation and extraction

## Implications for Data Stewardship (Challenges and Opportunities)
- Aligns with typical data stewardship duties: ensuring data are discoverable, usable, and well-governed
- Highlights common steward challenges:
  - Incomplete user needs or unclear downstream use cases
  - Timely data acquisition from dynamic simulations
  - Ensuring consistency in metadata and interoperability across formats
  - Handling large, multi-format datasets and potential non-interoperable legacy formats
- Governance actions to improve usability:
  - Provide structured metadata and a data dictionary
  - Document model assumptions, parameter values, and validation status
  - Establish clear access, versioning, and update procedures
  - Ensure interoperable metadata standards to facilitate discovery and reuse by diverse users