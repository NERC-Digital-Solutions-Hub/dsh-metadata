# Background, Experiment Design and Analytical Methods

- Purpose and context
  - Integrates data-based plant respiration with a large-scale land-surface model to understand how climate change affects respiration and the carbon cycle.
  - Uses Atkin et al. (2015) and Heskel et al. (2016) plant respiration temperature relationships within the JULES model, coupled to the IMOGEN climate-carbon cycle emulator.
  - Provides global-scale estimates of respiration and related diagnostics (e.g., Net Primary Productivity, NPP) under a business-as-usual fossil-fuel scenario (RCP8.5) from 1860 to 2100.

- Model framework and data sources
  - JULES (Joint UK Land Environment Simulator) as the land-surface model; IMOGEN emulator driving JULES globally.
  - IMOGEN emulates 34 Earth System Models selected from the CMIP5 database.
  - Four experiment configurations using the four JULES/IOMGEN setups described below.

- Four experiment configurations
  - standard: standard JULES configuration.
  - Rd25: revised baseline respiration at 25°C (Rd25).
  - Rd25 plus b,c formulation: Rd25 with a revised temperature response across ranges, incorporating two parameters b and c.
  - Rd25 plus bc plus acclimation: same as (iii) with additional acclimation effects.
  - All configurations are designed to enable comparison of respiration fluxes under different temperature response assumptions.

- Outputs and data products
  - Four annual variables at gridbox level (kg/m2/s):
    - plant respiration
    - soil respiration
    - Net Primary Productivity (NPP)
    - Gross Primary Productivity (GPP)
  - Time series cover 1860–2100 (inclusive), global-scale.
  - Data stored as self-describing NetCDF files for easy use with standard tools.

- Data structure and file naming
  - NetCDF files named: GlobalRespirationJULES<exp><centre><model>1860-2100_v1.nc
  - <exp> corresponds to standard, Rd25, Rd25plusbc, Rd25plusbcplusacclim.
  - <centre> and <model> align with CMIP5 CMIP data portal naming (GCM centre and model).

- Appendix and model mapping
  - Appendix provides a mapping of 34 Earth System Models and their CMIP5 centre/model names (e.g., bcc-csm1-1, CanESM2, GISS-E2-H, NorESM1-M, MPI-ESM-LR, etc.).
  - Ensures traceability between IMOGEN outputs and CMIP5 model configurations.

- Data access and usability
  - Data are suitable for standard visualization and analysis in R, Python, and NCO (netCDF operators).
  - Self-describing headers facilitate extraction of gridbox means, regional aggregates, and time-series analyses.

- Quality control and validation
  - Independent verification by two authors of the new respiration description integrated into JULES.
  - Re-built the 34-parameter Energy Balance Model and spatial patterns from scratch to minimize errors.
  - Alignment with Met Office standards for numerical stability and accuracy within the operational atmospheric-model suite.

- Reference framework and supporting literature
  - Atkin et al. 2015; Heskel et al. 2016: temperature dependence of leaf respiration and convergence across biomes.
  - Clark et al. 2011: JULES model description (carbon fluxes and vegetation dynamics).
  - Huntingford et al. 2010/2017: IMOGEN system and related climate-change applications; paper on improved respiration representations (2017, submitted).
  - Meinshausen et al. 2011; Taylor et al. 2012: CMIP5 and RCP framework.

- How this supports environmental monitoring
  - Delivers standardized, long-term, global-scale respiration and productivity datasets suitable for monitoring environmental health and policy performance.
  - Provides multiple respiration representations to assess sensitivity and uncertainty in the carbon cycle under climate change.
  - Data and outputs are designed for broad accessibility and integration into monitoring portals and dashboards.