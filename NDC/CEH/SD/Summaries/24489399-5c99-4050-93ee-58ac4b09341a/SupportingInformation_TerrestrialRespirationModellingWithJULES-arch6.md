# Background, Experiment Design and Analytical Methods

## Summary

- Purpose and scope
  - Combines data-based plant respiration representations with the JULES land surface model within the IMOGEN climate-carbon cycle emulator.
  - Produces global-scale estimates of plant respiration, soil respiration, Net Primary Productivity (NPP), and Gross Primary Productivity (GPP) for 1860–2100 under a business-as-usual fossil fuel scenario (RCP8.5).

- Core methodology
  - Integrates temperature-dependent respiration equations derived from Atkin et al. (2015) and Heskel et al. (2016) with the JULES model (Clark et al. 2011).
  - IMOGEN drives JULES globally and leverages 34 Earth System Models from CMIP5 (Taylor et al. 2012) to create ensemble-based projections.

- Available data sets (four JULES/IMOGEN simulations)
  - Timeframe: 1860 to 2100 (inclusive); variables expressed as yearly averages.
  - Purpose: global estimates of respiration and productivity for climate change impact assessment.

- Model variants (four experiments)
  - standard: using the standard JULES configuration.
  - Rd25: using revised Rd25 (respiration at 25°C) baseline.
  - Rd25 plus b,c formulation: Rd25 with a revised temperature response across ranges (parameters b and c).
  - Rd25 plus bc plus acclimation: same as (iii) with additional acclimation effects.

- Data quality and validation
  - Independent quality control by two authors.
  - Rebuilt the 34 ESM-based Energy Balance Model parameters from scratch to minimize errors.
  - Emphasis on numerical stability and robust performance within Met Office atmospheric model framework.

- Data structure and access
  - Four primary variables (gridbox mean values):
    - Plant respiration
    - Soil respiration
    - Net Primary Productivity (NPP)
    - Gross Primary Productivity (GPP)
  - Units: kg/m2/s; provided as yearly averages for 1860–2100.
  - File format: NetCDF; self-describing headers; readable with standard tools (R, Python, NCO, etc.).
  - File naming convention:
    - GlobalRespirationJULES<exp><centre><model>1860-2100_v1.nc
    - <exp> = "standard", "Rd25", "Rd25plusbc", or "Rd25plusbcplusacclim"
    - <centre> and <model> correspond to CMIP5 CMIP names.
  - CMIP5 driver: IMOGEN emulates 34 Earth System Models via CMIP5 data.

- Appendix and metadata
  - Appendix lists model centres and corresponding GCM names (e.g., BCC, BNU, CCCma, CMCC, CNRM-CERFACS, CSIRO, IPSL, MIROC, NASA-GISS, NCAR, NOAA-GFDL, CESM variants, etc.).
  - Table 1 highlights the mapping between centres and GCM names used by IMOGEN.

- Related information and references
  - The simulations underpin a broader research program, including Huntingford et al. (2017).
  - Foundational references informing components:
    - Atkin et al. (2015) on leaf respiration variability
    - Heskel et al. (2016) on temperature response convergence
    - Clark et al. (2011) on JULES model
    - Huntingford et al. (2010, 2000) on IMOGEN and analogue climate scenarios
    - Meinshausen et al. (2011), Taylor et al. (2012) on RCPs and CMIP5
  - Additional context provided by related peer-reviewed papers and ongoing updates.