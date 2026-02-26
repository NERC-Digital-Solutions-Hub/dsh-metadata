# Background, Experiment Design and Analytical Methods

- Purpose: Assess carbon cycle implications of land-use change for Paris Climate Agreement targets using BECCS and forest regrowth/conservation pathways.
- Modeling chain:
  - JULES (version 4.8) large-scale land surface model with multi-layer soil carbon.
  - IMOGEN climate-carbon cycle emulator (inverted) to emulate climate/meteorology from 34 CMIP5 GCMs using a prescribed temperature pathway.
- Experimental design:
  - Six simulations combining three temperature pathways and two land-use scenarios.
  - Temperature pathways: 1.5°C by 2100 (1p5deg), 2°C by 2100 (2deg), and 2°C with CO2 from the 1.5°C pathway (2deg_1p5CO2) to separate climate vs CO2 fertilization effects.
  - Land-use scenarios: IM19 (IMAGE SSP2-SPA0-RCP1.9) and IM26 (IMAGE SSP2-SPA2-RCP2.6).
  - Directory structure for runs:
    - 1p5deg_IM19, 1p5deg_IM26, 2deg_IM19, 2deg_IM26, 2deg_IM19_1p5CO2, 2deg_IM26_1p5CO2
- Outputs: 6 model output sets providing land carbon stocks and surface energy-balance variables to evaluate land-based mitigation implications.

- Linked datasets:
  - CMIP5 GCM outputs used to drive JULES-IMOGEN (stored at EIDC).
  - Outputs for 1850–2000 available via linked dataset DOIs.

- Data quality and stewardship:
  - JULES is maintained to high standards due to ties with UK Earth System Modeling efforts; emphasis on numerical stability and accuracy within Met Office models.

- Variables and data structure:
  - Time coverage: 2000–2099 (1850–1999 data available in linked Comyn-Platt et al., 2018 dataset).
  - CarbonStocks files: gridbox vegetation carbon (cv, kg m-2), soil carbon (cs_gb, kg m-2), fractional cover (frac), net primary productivity (npp, kg m-2 s-1), harvest (kg m-2 s-1), BECCS pool carbon (ccs_gb, Kg m-2), agricultural fractions (Frac_agr, Frac_biocrop, Frac_past), wood products pools, CO2 mole fraction (co2_ppmv).
  - WaterCycle files: soil temperature (t_soil, K), soil moisture (smcl), soil moisture fraction (Swet_tot), surface moisture flux (Fqw_gb), sensible heat flux (Ftl_gb), wetlands fraction (fwetl), runoff (runoff), water-table depth (zw).
  - Ancillary fields needed to run JULES-IMOGEN (grid setup, CO2, O3/CH4/N2O & non-CO2 radiative forcing, land cover, initial conditions).
  - 17-tile grid-box structure per location; NPP and yields require weighting by tile fractions (frac) across tiles such as various broadleaf, conifer, grass, crops, pastures, urban, water, bare soil, ice.

- File naming and access:
  - NetCDF files are self-describing and readable with standard tools (R, Python, NCO).
  - File naming convention: BL_CEN_<centre>_MOD_<model>_<scenario>.CarbonStocks.2000-2099.nc and similarly .WaterCycle.2000-2099.nc.
  - Outputs cover 34 ESMs from CMIP5; 2000–2099 for current experiments.
  - Appendix provides list of modelling centres and GCM names used (e.g., BCC, BNU, CCCma, CNRM-CERFACS, MOHC, NASA-GISS, NCAR, NorESM, NOAA-GFDL, CESM variants, etc.).

- Important methodological notes:
  - An explicit guidance section explains calculating grid-box totals:
    - Each grid-box contains 17 tiles; NPP per PFT must be weighted by frac to obtain grid-box totals.
  - Ancillary documentation includes initial/boundary conditions, CO2 prescribing for mixed climate-CO2 scenarios, land-cover files, and rose-suites required to reproduce the simulations.
  - History and context: builds on Harper et al. (2018, 2016) and Comyn-Platt et al. (2018); IMOGEN allows rapid exploration of climate-carbon interactions using a pattern-scaling approach.

- Relevance for environmental monitoring and policy:
  - Provides standardized, multi-scenario outputs of land carbon stocks and surface energy budgets across time and space.
  - Enables comparison of climate pathways and land-use futures to inform policy targets (Paris Agreement, 1.5°C vs 2°C).
  - Dataset curation supports reproducibility, data sharing, and integration with other environmental monitoring datasets via established portals and DOIs.

- References and related works:
  - Harper et al. (2018a, 2018b), Comyn-Platt et al. (2018), Harper et al. (2016).
  - IMOGEN development papers (Huntingford & Cox, 2000; Huntingford et al., 2010).
  - CMIP5 overview (Taylor et al., 2012).