# Outburst flood simulations of various dam failure scenarios from Tsho Rolpa glacial lake, Nepal, 2020: supporting document

## Overview of the data
- 12 Glacial Lake Outburst Flood (GLOF) scenarios simulated using a simple dam breach model, followed by a high-performance 2-D hydrodynamic model to predict flood flow dynamics.
- Data products include: dam breach flow results for 12 GLOF scenarios and 2-D flood hydrodynamics results (including the worst-case scenario figure).
- Study area: downstream region of Tsho Rolpa Lake (27°30′–27°51′ N, 86°10′–86°29′ E); map projection is WGS 1984 Transverse Mercator.
- Outputs presented as tables and maps showing maximum inundation depth and maximum flow velocity along the main channel from the lake to Manthali.

## Data content
- 1 CSV file: Breach_flow_under_different_GLOF_scenarios.
- 24 TIFF files: 12 TIFFs of maximum water depth per scenario and 12 TIFFs of maximum water velocity per scenario.
- The CSV contains 25 columns: Time (s); 12 columns for water depth under each scenario; 12 columns for discharge under each scenario.
- The dataset also references scenario-specific parameters such as final breach depth, initial lake volume above the final breach bottom, final average breach width, and total failure time.

## Collection and modeling methods
- Numerical modeling approach:
  - Dam breach breaching model to generate breach flow results.
  - Fully hydrodynamic 2-D depth-averaged shallow water equations (SWEs) to simulate flood hydrodynamics.
  - Governing equations solved with a finite-volume Godunov-type scheme with shock-capturing on uniform grids.
  - Parallelized high-performance computing on GPUs using NVIDIA CUDA for efficiency in large-scale simulations.
- Key model components:
  - Depth h, unit-width discharges qx = uh, qy = vh.
  - Bed elevation zb and bed roughness Cf = gn^(2/3) with Manning n.
  - Source terms include friction and bed slope effects.
- Calibration: No validation performed due to the model’s conservative mass/momentum framework and prior successful applications.
- Analytical outputs: Extracted maximum water depth and maximum flow velocity from time-series results.

## Nature and units of recorded values
- Water depth: meters (m).
- Flow velocity: meters per second (m/s).
- Outputs include maximum inundation depth and maximum velocity for each scenario, as well as time-series data for breach flow.

## Quality control and limitations
- No validation performed; calibration steps are not reported (consistent with the stated model confidence in prior applications).
- Describes reliance on minimal parameters and mass/momentum conservation as justification for limited calibration.

## Data structure details
- Data files:
  - 1 CSV: Breach_flow_under_different_GLOF_scenarios (Time + 12 depths + 12 discharges).
  - 24 TIFFs: 12 for maximum water depth (one per scenario) and 12 for maximum water velocity (one per scenario).
- Spatial scope: downstream area of Tsho Rolpa Lake; coordinate system and projection specified (WGS 1984 Transverse Mercator).
- Temporal scope: time in seconds as recorded in the CSV; derived hydrodynamic results from simulations.

## Use and accessibility implications for environmental monitoring
- Provides standardized, scenario-based flood hazard metrics (depth, velocity) that can be used for risk assessment, early warning planning, and policy evaluation downstream of a glacial lake.
- The data are organized for straightforward cross-scenario comparison (depths, discharges, breach widths, and volumes) and include both time-series and map-based outputs (TIFFs).
- Although calibration/validation are not performed, the dataset offers a reproducible framework (SWEs, breach modeling, GPU-accelerated computation) that can be integrated with other environmental monitoring datasets to enhance understanding of flood hazards and inform resilience planning.