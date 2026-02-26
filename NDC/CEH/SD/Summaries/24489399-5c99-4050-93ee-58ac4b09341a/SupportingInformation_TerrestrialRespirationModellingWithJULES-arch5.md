# Background, Experiment Design and Analytical Methods

- Purpose and context
  - Addresses how plant respiration (in addition to CO2 uptake by photosynthesis) is affected by climate change, using data-based respiration representations integrated into the JULES land surface model and the IMOGEN climate-carbon cycle system.
  - Combines Atkin et al. (2015) and Heskel et al. (2016) respiration data with JULES, and runs global IMOGEN simulations to assess respiration and related diagnostics (including NPP) from 1860 to 2100 under a business-as-usual RCP85 scenario.
  - Four JULES/IMOGEN simulation sets are provided, emulating 34 Earth System Models from CMIP5.

- Datasets and experiments
  - Four experiment variations:
    - standard (baseline JULES)
    - Rd25 (revised Rd at 25°C)
    - Rd25 plus b,c formulation (temperature-response revision with parameters b and c)
    - Rd25 plus bc plus acclimation (adds acclimation effects)
  - Core data derived from the IMOGEN emulator using CMIP5 model ensemble; global estimates of plant respiration, soil respiration, Net Primary Productivity (NPP), and Gross Primary Productivity (GPP).

- Documentation and provenance
  - The analyses follow Huntingford et al. (2017, submitted) and build on Atkin (2015), Clark (2011), Heskel (2016), and related work.
  - Quality control and validation described to ensure robustness within the UK Earth System Model framework.

- Data and access overview
  - Four variables provided as gridbox means:
    - Plant respiration
    - Soil respiration
    - Net Primary Productivity (NPP)
    - Gross Primary Productivity (GPP)
  - Units: kg/m2/s; yearly averages; 1860–2100 inclusive.
  - Data are stored in self-describing NetCDF files readable with standard tools (R, Python, nco, etc.).
  - File naming convention: GlobalRespirationJULES<exp><centre><model>1860-2100_v1.nc
    - <exp> = standard, Rd25, Rd25plusbc, Rd25plusbcplusacclim
    - <centre> and <model> correspond to CMIP5 centre/model names.

- Data structure and model ensemble details
  - IMOGEN emulates 34 Earth System Models from CMIP5 for global spatial scales.
  - Appendix lists mappings between GCM centres and model names to CMIP5 identifiers.
  - Data availability aligns with CMIP5 framework to facilitate cross-model comparisons.

- Quality control and robustness
  - Independent validation: two authors checked the integration of the new respiration description into JULES.
  - Re-built the 34 ESM-based Energy Balance Model parameters from scratch to minimize errors.
  - Emphasis on numerical stability and accuracy within the Met Office operational modelling suite.

- Appendix and references
  - Appendix: comprehensive mapping of climate modelling centres and CMIP5 model names (GCMname and centre pairs).
  - References: key peer-reviewed sources for respiration data, JULES, IMOGEN, CMIP5 context, and the underpinning studies (Atkin 2015; Clark 2011; Heskel 2016; Huntingford et al. 2010/2017; Meinshausen et al. 2011; Taylor et al. 2012).

- Other information for data governance
  - The datasets are designed for broad usability with standard data formats and widely used analysis tools, supporting discoverability and reuse.
  - Documentation points to additional peer-reviewed sources and the primary Huntingford et al. (2017) paper as the basis for the simulations.