# Background, Experiment Design and Analytical Methods

## Objective and context
- Plant respiration is a significant component of the land carbon cycle, influenced by leaf-level temperature.
- The study combines data-based respiration assessments (Atkin et al., 2015; Heskel et al., 2016) with the JULES land surface model to derive large-scale respiration estimates.
- JULES is embedded within the IMOGEN climate-carbon cycle emulator to explore climate change impacts globally.

## Modeling framework
- JULES: Joint UK Land Environment Simulator used for carbon fluxes and vegetation dynamics.
- IMOGEN: An intermediate-complexity climate-carbon cycle model that runs JULES globally and links to CMIP5 Earth System Models (ESMs).
- CMIP5-based ensemble: IMOGEN emulates 34 different ESMs (GCMs) to explore global respiration and related diagnostics (e.g., Net Primary Productivity, NPP).

## Experimental design (four data sets)
- Four JULES/IMOGEN experiment configurations for global estimates (1860–2100) under a business-as-usual fossil-fuel scenario (RCP85):
  - standard: using the standard JULES formulation.
  - Rd25: revised Rd25 (respiration at 25°C) baseline for flux comparisons.
  - Rd25 plus b,c formulation: Rd25 with a revised temperature response across ranges, governed by parameters b and c.
  - Rd25 plus bc plus acclim: same as (iii) with additional acclimation effects.
- All analyses are described in Huntingford et al. (Submitted 2017).

## Data products and structure
- Four gridbox-mean variables provided: plant respiration, soil respiration, NPP, and GPP.
- Units: kg/m2/s; available as yearly averages from 1860 to 2100 inclusive.
- NetCDF files are self-describing and readable with standard tools (R, Python, NCO) for visualization and analysis.
- File naming convention: GlobalRespirationJULES<exp><centre><model>1860-2100_v1.nc
  - <exp> = standard, Rd25, Rd25plusbc, Rd25plusbcplusacclim
  - <centre> and <model> correspond to CMIP5 CMIP data portal identifiers.

## Quality control and validation
- Independent verification: two authors reviewed the new respiration description and re-built the 34 ESM-based energy balance model parameters to reduce errors.
- JULES’ robustness is maintained to high standards to ensure numerical stability within the Met Office operational model suite.

## Data content details
- Variables provided per gridbox: 
  - Plant respiration
  - Soil respiration
  - Net Primary Productivity (NPP)
  - Gross Primary Productivity (GPP)
- All four have units of kg/m2/s; annual means across 1860–2100.
- Data are designed to be traceable, with clear metadata and CMIP5 model provenance.

## Appendix: CMIP5 modelling centers and models
- Provides a list mapping CMIP5 centres to GCM names used in IMOGEN/JULES simulations (e.g., BCC-CSM1-1, CanESM2, HadGEM2-CC/ES, MPI-ESM-LR/MR, GISS, CCSM4, NorESM1-M, CESM1 variants, etc.).
- Ensures reproducibility by aligning IMOGEN outputs with CMIP5 model identifiers.

## Related work and references
- Foundational studies and datasets informing the approach:
  - Atkin et al. (2015) on global leaf respiration variability
  - Heskel et al. (2016) on convergence of leaf respiration temperature responses
  - Clark et al. (2011) on JULES model description
  - Huntingford et al. (2010, 2017) on IMOGEN and respiration implications
  - Meinshausen et al. (2011) on RCP scenarios
  - Taylor et al. (2012) on CMIP5 overview
- These references underpin the data-based respiration formulation, model integration, and scenario design used in the four experimental configurations.