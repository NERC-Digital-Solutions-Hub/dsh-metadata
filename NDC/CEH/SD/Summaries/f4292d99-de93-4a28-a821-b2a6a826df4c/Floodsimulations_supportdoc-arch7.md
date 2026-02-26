# Outburst flood simulations of various dam failure scenarios from Tsho Rolpa glacial lake, Nepal, 2020: supporting document

## Overview
- Study creates glacial lake outburst flood (GLOF) scenarios for Tsho Rolpa Lake, Nepal using a simple dam breach model combined with a high-performance hydrodynamic model.
- Data includes 12 dam breach flow results (one per scenario) and 2-D flood hydrodynamics results (including the worst-case scenario).
- Location: downstream area of Tsho Rolpa Lake (27°30′–27°51′ N, 86°10′–86°29′ E).
- Map projection: WGS 1984 Transverse Mercator.
- Figure 1 illustrates maximum inundation depth and maximum flow velocity along the main channel from the lake to Manthali.

## Data contents
- Data collection method: numerical hydrodynamic modeling (GLOF model) using 2-D depth-averaged shallow water equations (SWEs).
- Data products:
  - 1 CSV file: Breach_flow_under_different_GLOF_scenarios.
  - 24 TIFF files: 12 TIFFs for maximum water depth (one per scenario) and 12 TIFFs for maximum water velocity (one per scenario).
- CSV structure: 25 columns total — Time (s) as the first column; 12 columns for water depth (one per scenario); 12 columns for discharge (one per scenario).

## Scenarios (GLOF variations)
- 12 GLOF scenarios differ by breach depth, water level, and breach characteristics (as summarized in Table 1 of the document).
- Reported quantities per scenario include:
  - Final breach depth (m) variants (e.g., 10, 20, 30) and combinations with current water level and other modifiers.
  - Final average breach width (m) across scenarios.
  - Initial lake volume above the final breach bottom (x10^6 m^3).
  - Total failure time (h).
- The dataset provides the 12 breach-depth/water-level combinations and the corresponding hydrodynamic outputs (depth and velocity).

## Methods and modeling
- Hydrodynamic model:
  - Fully 2-D, depth-averaged SWEs with a Godunov-type finite volume scheme (shock-capturing for transient floods).
  - Governing equations use q, f, g, and s terms, with h (water depth), qx = u h, qy = v h, zb (bed elevation), and Cf (bed friction via Manning coefficient n).
  - Includes bed slope terms and frictional source terms; implemented for parallel execution on GPUs using CUDA for efficiency.
- Calibration/validation:
  - No validation performed due to the model’s minimal parameter requirements and prior successful use in similar studies.
- Analytical approach:
  - Maximum water depth and maximum flow velocity are extracted from time-series outputs of the hydrodynamic simulations.

## Data units and quality
- Units:
  - Water depth: meters.
  - Flow velocity: meters per second.
- Quality control:
  - No external validation performed; relies on the established application of the SWEs and prior studies for similar flows.

## Data structure details
- Files:
  - Breach_flow_under_different_GLOF_scenarios.csv
  - 24 TIFF files: 12 depth rasters (maximum depth per scenario) and 12 velocity rasters (maximum velocity per scenario).
- Content layout:
  - CSV first column: Time (s).
  - Next 12 columns: water depth for each scenario.
  - Last 12 columns: discharge (unit-width) for each scenario.
- Spatial context:
  - Data covers the downstream area specified in the overview, with the outputs aligned to the WGS 1984 Transverse Mercator projection.