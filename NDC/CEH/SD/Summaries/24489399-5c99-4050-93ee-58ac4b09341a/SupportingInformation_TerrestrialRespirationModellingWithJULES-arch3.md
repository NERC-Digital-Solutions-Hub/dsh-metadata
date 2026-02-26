# Background, Experiment Design and Analytical Methods

- Purpose and context
  - Investigates plant respiration and its role in the global carbon cycle within climate change, combining data-based respiration equations with the JULES land surface model and the IMOGEN climate-carbon cycle emulator.
  - Uses recent respiration research (Atkin et al. 2015; Heskel et al. 2016) to inform temperature-dependent respiration formulations within JULES, then runs global simulations via IMOGEN.

- Experiment design and scenarios
  - Four JULES/IMOGEN simulation variants:
    - standard: using the standard JULES configuration
    - Rd25: revised Rd25 (respiration at 25°C) for baseline comparisons
    - Rd25 plus b,c formulation: Rd25 with a revised temperature response across ranges (parameters b and c)
    - Rd25 plus bc plus acclimation: as (iii) with additional acclimation effects
  - Scope: global estimates of respiration, Net Primary Productivity (NPP), and Gross Primary Productivity (GPP) from 1860 (pre-industrial) to 2100, under a business-as-usual fossil fuel scenario (RCP8.5).
  - Model integration: IMOGEN emulates 34 Earth System Models from CMIP5 to drive JULES.

- Data sources and framework
  - Based on data-driven descriptions of leaf/plant respiration linked to leaf temperature (Atkin et al. 2015; Heskel et al. 2016) and integrated into JULES (Clark et al. 2011).
  - Analysis framework described in Huntingford et al. (2017, submitted) with prior work: Huntingford et al. (2010, 2000); Atkin (2015); and CMIP5 references (Taylor et al. 2012; Meinshausen et al. 2011).

- Data products and structure
  - Four gridbox-averaged variables provided: plant respiration, soil respiration, NPP, and GPP; units kg/m2/s; yearly averages from 1860 to 2100.
  - Data format: NetCDF files, self-describing via headers; accessible with standard tools (R, Python, nco) for visualization and analysis.
  - File naming convention: GlobalRespirationJULES<exp><centre><model>1860-2100_v1.nc, where <exp> is one of standard, Rd25, Rd25plusbc, Rd25plusbcplusacclim; <centre> and <model> correspond to CMIP5 centres/models.

- Appendix: data provenance and model identifiers
  - Provides mappings of CMIP5 centres to internal GCM names (e.g., BCC, BNU, CCCma, CMCC, CNRM-CERFACS, CSIRO variants, INM, IPSL variants, MIROC, NASA-GISS variants, NCAR, NCC, NOAA-GFDL, NSF-DOE-NCAR) to ensure traceability with the CMIP5 portal.

- Quality control and reproducibility
  - Independent verification of the new respiration description by two authors.
  - 34 ESM-based energy balance model parameters rebuilt from scratch to reduce errors.
  - Emphasis on numerical stability and robust performance within the Met Office operational modelling suite.

- Other information and references
  - A body of peer-reviewed work underpins the datasets and methods (Atkin 2015; Clark 2011; Heskel 2016; Huntingford et al. 2010, 2017; Meinshausen 2011; Taylor 2012), supporting the study’s framework and its relevance for future climate-change scenario analyses.