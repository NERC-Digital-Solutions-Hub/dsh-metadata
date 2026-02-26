# Background, Experiment Design and Analytical Methods

- Purpose and scope
  - Examines carbon cycle implications of land-use change for the Paris Climate Agreement under two land-use pathways with varying BECCS or forest regrowth/conservation.
  - Uses JULES (version 4.8) global land surface model with multi-layer soil carbon, coupled to IMOGEN climate-carbon cycle emulator to emulate 34 CMIP5 GCMs via a prescribed temperature pathway.
  - Outputs focus on land carbon stocks and surface energy budget variables to assess land-based climate mitigation implications.
  - Main dataset described for Harper et al. (2018); historical context and linked datasets provided.

- Experimental design
  - Factorial design across three global warming pathways and two land-use scenarios, yielding six core simulations; expanded with a CO2 pathway isolation scenario.
  - Temperature pathways: 1.5°C, 2°C, and 2°C with CO2 from the 1.5°C scenario to separate climate vs CO2 fertilization effects.
  - Land-use scenarios: IM19 (IMAGE SSP2-SPA0-RCP1.9) and IM26 (IMAGE SSP2-SPA2-RCP2.6).
  - Six simulations (directory structure reflects scenario names):
    - 1p5deg_IM19, 1p5deg_IM26, 2deg_IM19, 2deg_IM26, 2deg_IM19_1p5CO2, 2deg_IM26_1p5CO2
  - Linked datasets include CMIP5 GCM outputs used to drive JULES-IMOGEN and outputs for 1850–2000.

- Data and variables
  - Outputs include carbon stocks (vegetation, soil), BECCS pool (ccs_gb), wood products pools, and crop/land-cover fractions (Frac_agr, Frac_biocrop, Frac_past).
  - Net primary productivity (NPP) and harvest for crop-related PFTs; CO2 concentration in air (co2_ppmv).
  - Water-cycle and energy-balance variables: soil temperature (t_soil), soil moisture (smcl), surface/total moisture fluxes (Fqw_gb, Swet_tot), surface energy fluxes (Ftl_gb), runoff, groundwater depth (zw), etc.
  - Variables are provided for 2000–2099; 1850–1999 data exist in a separate linked dataset.
  - Data are organized into two main file types per dataset: CarbonStocks and WaterCycle, with descriptive variable headers (units, dimensions) in NetCDF files.

- Data structure and access
  - NetCDF files are self-describing and readable with standard tools (R, Python, nco, etc.).
  - IMOGEN emulates 34 Earth System Models via CMIP5, with filenames following:
    - BL_CEN_<centre>_MOD_<model>_<scenario>.CarbonStocks.2000-2099.nc
    - BL_CEN_<centre>_MOD_<model>_<scenario>.WaterCycle.2000-2099.nc
  - Directory organization mirrors land-use and CO2 experiments; variables cover time, latitude, longitude, and other dimensions (e.g., PFTs, surface types).

- Data provenance and quality
  - JULES is maintained to high standards due to ties to UK Earth System Model development; emphasis on numerical stability, accuracy, and compatibility with Met Office models.
  - Detailed references provided for the dataset and underlying model components (JULES, IMOGEN, CMIP5 context).

- Ancillary files and run instructions
  - Ancillary_files directory includes:
    - Model grid definitions (grid_info.nc, imogen_order.dat, points.all.dat)
    - Initial/boundary CO2 settings (SSP22.6_IMAGE_concs_co2.txt and related)
    - Prescribed CO2 conditions for 2C climate with 1.5C CO2 levels
    - Non-CO2 radiative forcing and atmospheric constituent files (O3, CH4, N2O, qnonco2 files)
    - Land-cover data for IM1.9 and IM2.6 scenarios (landcover NetCDFs)
    - Initial condition files for each GCM and temperature scenario starting in 2000
  - Rose suite configuration (IM1.9/IM2.6) listed with registration-accessible identifiers for reproducibility.

- Practical notes for use
  - To compute grid-box total NPP, apply a weighted sum using the 17 tile fractions (Frac_agr, Frac_biocrop, etc.) within each grid box.
  - Each grid box comprises 17 tiles (13 plant types + 4 non-veg tiles); track that NPP per PFT is volume-weighted by tile fractions.
  - Outputs are designed to support analysis of carbon stocks, BECCS pools, crop/grass fractions, and climate–land-use interaction under specified warming targets.

- References and context
  - Main dataset reference: Harper et al. 2018 (Nature Communications) on land-use emissions and Paris targets.
  - Related datasets and methodological context: Comyn-Platt et al. 2018 (Nature Geoscience), Harper et al. 2016/2018 (JULES improvements), IMOGEN model descriptions (Huntingford et al., 2000/2010), CMIP5 framework (Taylor et al., 2012).