# Background, Experiment Design and Analytical Methods

- Purpose: Examine carbon cycle implications of land-use change for Paris Climate Agreement targets using two BECCS/forest pathways and a multi-model framework.
- Modelling suite:
  - JULES (Joint UK Land Environment Simulator) large-scale land surface model (v4.8) with a multi-layer soil-carbon module.
  - IMOGEN climate-carbon cycle emulator to drive JULES; uses pattern scaling of 34 CMIP5 GCMs.
  - The combination enables exploration of land-based climate mitigation under specified warming targets.
- Experimental design:
  - Six simulations: a factorial combination of three temperature scenarios and two land-use scenarios.
  - Temperature pathways: 2deg (2°C by 2100), 1p5deg (1.5°C by 2100), and 2deg with CO2 from the 1.5°C pathway (2deg_1p5CO2) to separate climate vs CO2 fertilization effects.
  - Land-use pathways: IM19 (IMAGE SSP2-SPA0-RCP1.9) and IM26 (IMAGE SSP2-SPA2-RCP2.6).
  - Resulting directory structure for runs: 1p5deg_IM19, 1p5deg_IM26, 2deg_IM19, 2deg_IM26, 2deg_IM19_1p5CO2, 2deg_IM26_1p5CO2.
- Data scope and availability:
  - Outputs cover 2000–2099; historical 1850–1999 data are in a linked dataset from Comyn-Platt et al. (2018).
  - Linked CMIP5 GCM outputs stored in the EIDC and other DOIs; historical outputs (1850–2000) available via specified DOIs.
- How the data are used:
  - To understand land-based climate mitigation effects on carbon stocks, surface energy budget, and related variables under Paris targets.
  - 6 simulation sets form the basis for analyses in Harper et al. (2018) and related works.

## Data and Variables

- CarbonStocks dataset includes:
  - cv: Gridbox total vegetation carbon (kg m-2)
  - cs_gb: Gridbox total soil carbon (kg m-2)
  - frac: Fractional cover of each surface type (dimension: time, type, latitude, longitude)
  - npp: Net primary productivity per vegetated tile (kg m-2 s-1; tile-weighted by frac for grid-box totals)
  - harvest: Harvest on crop tiles (kg m-2 s-1)
  - ccs_gb: BECCS pool carbon in the grid box (Kg m-2)
  - Frac_agr, Frac_biocrop, Frac_past: Fractions of grid box covered by crops, bioenergy crops, and pasture
  - wood_products: Carbon content in wood product pools (Kg m-2), including effects of vegetation clearing
  - co2_ppmv: CO2 concentration (ppmv)
- WaterCycle dataset includes:
  - t_soil: Sub-surface soil temperature (K)
  - smcl: Sub-surface soil moisture (kg m-2)
  - Swet_tot: Soil moisture saturation fraction
  - Fqw_gb: Surface moisture flux (Kg m-2 s-1)
  - Ftl_gb: Surface sensible heat flux (W m-2)
  - fwetl: Wetland fraction
  - runoff: Grid-box runoff rate (Kg m-2 s-1)
  - zw: Depth to water table (m)
- Time and space:
  - Variables provided for 2000–2099; 1850–1999 data available in linked datasets.
- Notes on usage:
  - NPP totals require weighting by frac across 17 tiles per grid box; tiles include various tree, grass, crop, pasture, urban, water, bare soil, and ice categories.

## Data Access and Linkages

- Linked datasets:
  - CMIP5 GCM outputs used to drive JULES-IMOGEN (stored in the EIDC with a DOI).
  - Outputs for 1850–2000 available via another DOI.
- File naming and structure:
  - NetCDF files are self-describing and readable with standard tools (R, Python, nco, etc.).
  - Naming convention: BL_CEN_<centre>_MOD_<model>_<scenario>.CarbonStocks.2000-2099.nc and BL_CEN_<centre>_MOD_<model>_<scenario>.WaterCycle.2000-2099.nc
  - <scenario> corresponds to 2deg or 1p5deg; <centre> and <model> match CMIP5 identifiers.
  - Directories reflect land-use and CO2 experiments.
- Ancillary materials:
  - Ancillary_files directory contains initial/boundary condition files, grid definitions, CO2 concentrations, non-CO2 forcings, and land-cover data for IM1.9 and IM2.6 scenarios.
  - Rose suite configurations (IM1.9 and IM2.6 variants) are listed and accessible via the Met Office code portal (registration required).

## Data Structure, Access, and Usage Notes

- Data structure and units:
  - Variables include time, latitude, longitude; several have additional dimensions such as pft (plant functional type) for NPP and harvest.
- Practical notes for analysts:
  - The IMOGEN emulator uses 34 GCMs to emulate climate responses; integrally linked to large Earth system modelling context.
  - The 17-tile framework within each grid box is critical for properly aggregating NPP and related variables.
  - For climate attribution and mitigation analysis, the 1p5deg vs 2deg with 1.5CO2 contrast isolates climate change effects from CO2 fertilization.

## Appendix and References

- Appendix lists climate modelling centres and corresponding GCM names used in IMOGEN (e.g., BCC, BNU-ESM, CanESM2, CNRM-CM5, etc.).
- References:
  - Harper et al. (2018a, 2018b) on land-use emissions and vegetation representation in JULES.
  - Comyn-Platt et al. (2018) on carbon budgets for 1.5°C and 2°C targets with wetlands and permafrost feedbacks.
  - Foundational works on JULES and IMOGEN development and CMIP5 context.

## Practical Notes for Analysts

- Data coverage spans 2000–2099 (and historical data 1850–1999 in linked datasets), suitable for assessing land-use pathways and warming targets.
- The dataset supports calculating grid-box totals via weighted sums by fractional cover; careful handling of asset tiles is essential for accurate NPP and carbon stock estimates.
- Access to the full suite requires navigating DOIs, EIDC links, and Met Office rose-suites registration; ensure proper metadata and provenance tracking for reproducibility.