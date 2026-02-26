# Background, Experiment Design and Analytical Methods

- Overview of the climate-vegetation modelling approach:
  - Anthropogenic CO2 drives global warming; attention also on plant respiration and its temperature dependence.
  - Combines data-based leaf respiration relationships (Atkin et al. 2015; Heskel et al. 2016) with the JULES land surface model.
  - Uses IMOGEN to emulate climate-carbon cycle impacts globally.

- Experiment sets and time frame:
  - Four JULES/IMOGEN simulation setups to estimate global respiration and related diagnostics (e.g., NPP) from 1860 to 2100.
  - Scenarios are designed for a business-as-usual fossil fuel pathway (RCP8.5).

- Models and data scope:
  - IMOGEN emulates 34 Earth System Models from the CMIP5 database.
  - Outputs include respiration (plant and soil) and productivity metrics (NPP, GPP) at global scale.

- Data products and purpose for GIS:
  - Purpose-built, data-driven estimates to explore how respiration and productivity respond to climate change.
  - Outputs intended for integration into map-based analyses and visualizations.

- Key experiments (exp): four variants of the JULES-based framework:
  - standard: standard JULES configuration
  - Rd25: respiration at 25°C as a baseline
  - Rd25plusbc: Rd25 with a revised temperature response (parameters b and c)
  - Rd25plusbcplusacclim: as (iii) with additional acclimation effects

- Documentation of full methodology:
  - All methods and data references are detailed in Huntingford et al. (2017, submitted) and related foundational papers.

- Quality control and data robustness:
  - Independent verification of the new respiration description by two authors.
  - Rebuilds of all 34 ESM-based energy balance parameters from scratch to minimize errors.
  - JULES is maintained to high standards for numerical stability within Met Office atmospheric modelling.

- Data structure and file format:
  - Four variables provided as gridbox means:
    - Plant respiration
    - Soil respiration
    - Net Primary Productivity (NPP)
    - Gross Primary Productivity (GPP)
  - Units: kg/m2/s
  - Temporal resolution: yearly averages
  - Time span: 1860–2100 (inclusive)
  - File format: NetCDF, self-describing headers; accessible with standard tools (R, Python, nco)

- File naming and organisation:
  - GlobalRespirationJULES<exp><centre><model>1860-2100_v1.nc
  - <exp> options: standard, Rd25, Rd25plusbc, Rd25plusbcplusacclim
  - <centre> and <model> correspond to CMIP5 GCM centre and model names (matching CMIP5 portal)

- Appendix: CMIP5 model centres and model names:
  - Provides the mapping of centres and model names used in the IMOGEN emulator (extensive list of centres and corresponding GCM names).

- References and related information:
  - Key foundational works on leaf respiration, JULES, IMOGEN, and climate scenarios (Atkin et al. 2015; Heskel et al. 2016; Clark et al. 2011; Huntingford et al. 2010/2017; Meinshausen et al. 2011; Taylor et al. 2012).

- GIS implications and usage notes:
  - NetCDF format with gridbox-level outputs is well-suited for GIS workflows.
  - Variables (respiration, NPP, GPP) can be mapped and analyzed over time (1860–2100) at global resolution.
  - Data can be regridded or integrated with other spatial datasets; compatible with common GIS and data science toolchains (R, Python).