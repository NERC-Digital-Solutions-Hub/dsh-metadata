# Background, Experiment Design and Analytical Methods

- Purpose and context
  - Examines carbon cycle implications of land-use change for the Paris Climate Agreement under two BECCS/forest regrowth pathways.
  - Uses JULES (land surface model) with a multi-layer soil carbon module, coupled to IMOGEN (an intermediate climate-carbon cycle emulator) to explore climate–land-use interactions.
  - Emulates climate outcomes from CMIP5 using a prescribed temperature pathway to assess land-based mitigation effects.

- Modelling framework and data sources
  - JULES v4.8 (grid-scale vegetation and soil carbon, energy budget) linked to IMOGEN, which applies pattern scaling across 34 CMIP5 GCMs.
  - The study explores six simulations derived from two land-use pathways (IM19 and IM26) and three temperature pathways (2°C, 1.5°C, and 2°C with 1.5°C CO2 levels to isolate climate vs CO2 fertilization effects).
  - CMIP5 GCM outputs underpin the IMOGEN emulator; related historical data (1850–1999) referenced from a linked dataset.

- Experimental design
  - Factorial design: 3 temperature pathways × 2 land-use scenarios = 6 simulation configurations.
  - Directory naming conventions reflect the combination, e.g., 1p5deg_IM19, 1p5deg_IM26, 2deg_IM19, 2deg_IM26, 2deg_IM19_1p5CO2, 2deg_IM26_1p5CO2.
  - 12 simulations are described for the global warming scenarios and land-use configurations.

- Outputs and variables
  - CarbonStocks: cv (gridbox vegetation carbon), cs_gb (gridbox soil carbon), ccs_gb (BECCS pool), wood_products; all in kg m-2 with time, latitude, longitude; includes fractional cover (frac) and NPP (npp) by vegetation tiles.
  - Harvest data for crop tiles (non-zero for certain plant functional types).
  - WaterCycle: t_soil, smcl, Swet_tot, Fqw_gb (moisture flux), Ftl_gb (sensible heat flux), fwetl (wetland fraction), runoff, zw (water table depth).
  - Frac_agr, Frac_biocrop, Frac_past for land-cover fractions; includes tile-level breakdowns of 17 surface tiles (e.g., various forest, grass, crops, pasture, urban, water, bare soil, ice).
  - Additional variables such as CO2 mixing ratio (co2_ppmv).
  - Outputs span 2000–2099 (1850–1999 data available in linked dataset).

- Data structure and accessibility
  - NetCDF files are self-describing and tailored for standard analysis in R, Python, and other tools; follows a clear naming convention.
  - Main file naming: BL_CEN_<centre>_MOD_<model>_<scenario>.CarbonStocks.2000-2099.nc and .WaterCycle.2000-2099.nc, with <centre> and <model> matching CMIP5 catalogue identifiers.
  - Data are organized by experiment directories corresponding to land-use and climate scenarios.

- Ancillary files and running the model
  - Ancillary_files directory contains:
    - Grid information (grid_info.nc, imogen_order.dat, points.all.dat).
    - CO2 initialization and scenario-specific CO2 prescriptions (e.g., SSP2.6_IMAGE_concs_co2.txt; co2_experiment).
    - Non-CO2 forcings (O3, CH4, N2O) and total radiative forcing files.
    - Land cover definitions for IM1.9 and IM2.6 (JULES grid representations).
    - Initial condition files for each GCM and temperature scenario to start in 2000.
  - Appendix provides a list of climate modelling centres and GCM names used in IMOGEN, linking to the broader CMIP5 framework.

- Notes on data use and calculation
  - Grid boxes contain 17 tiles; NPP per Plant Functional Type (PFT) assumes full-tile occupancy, so grid-box totals require a weighted sum using frac.
  - Describes how to compute grid-box totals for NPP and other variables using the fractional tiles.

- Data provenance and references
  - Primary dataset references Harper et al. (2018) Nature Communications and related Comyn-Platt et al. (2018) for carbon budgets and wetland/permafrost feedbacks.
  - JULES development and IMOGEN emulator references are provided for methodological context.
  - Appendices include detailed rosen suite names and model-centre mappings used to drive JULES via IMOGEN.

- Relevance for monitoring and policy evaluation
  - Provides a structured, multi-scenario framework to monitor land-use emissions, vegetation and soil carbon stocks, and BECCS contributions under Paris Agreement targets.
  - Offers transparent data products and metadata (including data provenance and file structure) to support data governance, reproducibility, and evidence-based decision-making.
  - Highlights data access considerations (e.g., linked DOIs for datasets, registration for rose suites) and calculation notes essential for accurate interpretation and communication of results.