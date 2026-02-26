# Implications of improved representations of plant respiration in a changing climate

- Overview
  - Addresses how climate change perturbs the natural land carbon cycle, focusing on plant respiration in addition to photosynthetic CO2 draw-down.
  - Integrates recent data-based respiration relationships (leaf-level temperature dependence) with the JULES land surface model, and uses IMOGEN to couple to a climate–carbon system.
  - Builds on Atkin et al. (2015) and Heskel et al. (2016) to derive analytical temperature-dependent respiration equations and applies them within JULES in an IMOGEN emulator context.
  - Employs a global, scenario-based approach to explore respiration and related diagnostics (e.g., Net Primary Productivity, NPP).

- Data and modelling framework
  - IMOGEN emulator drives JULES using 34 Earth System Models from the CMIP5 database, spanning 1860–2100 under a business-as-usual fossil fuel pathway (RCP8.5).
  - Four experimental configurations of JULES/IMOGEN simulations:
    - standard
    - Rd25 (revised Rd25 at 25°C)
    - Rd25 plus b,c formulation (temperature response with coefficients b and c)
    - Rd25 plus bc plus acclimation (adds acclimation effects)
  - Purpose: to assess implications of improved representations of plant respiration on global carbon fluxes and productivity.

- Data products and access
  - Variables provided (gridbox means): plant respiration, soil respiration, Net Primary Productivity (NPP), and Gross Primary Productivity (GPP).
  - Units: kg/m²/s; yearly averages; time span 1860–2100.
  - Data format: NetCDF files, self-describing headers; compatible with standard tools (R, Python, nco).
  - File naming convention: GlobalRespirationJULES<exp><centre><model>1860-2100_v1.nc
    - <exp> corresponds to one of: standard, Rd25, Rd25plusbc, Rd25plusbcplusacclim
    - <centre> and <model> match those used in CMIP5 CMIP data portals.
  - Appendix provides a mapping of GCM centres to model names (a long list of coded centre-model pairs).

- Quality control and robustness
  - Independent verification: two authors reviewed the new data-based respiration description and its integration into the JULES model.
  - Rebuild of 34 ESM-based Energy Balance Model parameters from scratch to reduce error risk.
  - Emphasis on numerical stability and accuracy within the Met Office’s Earth system modelling context.

- Data provenance and usage context
  - IMOGEN emulates 34 CMIP5 Earth System Models to enable global-scale assessment of respiration under climate change.
  - Connects point- and process-level respiration research (Atkin et al., Heskel et al.) with large-scale modelling (JULES) to inform climate impact analyses.
  - References include foundational papers on JULES, IMOGEN, respiration temperature responses, and CMIP5/RCP frameworks.

- Appendix and references
  - Provides a comprehensive list of CMIP5 GCM centres and corresponding model names used to drive IMOGEN/JULES.
  - Key references cited for methods and data sources include Atkin et al. (2015), Heskel et al. (2016), Clark et al. (2011), Huntingford et al. (2010, 2017), and Meinshausen et al. (2011).