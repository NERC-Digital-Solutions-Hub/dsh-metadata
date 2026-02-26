# Background, Experiment Design and Analytical Methods

- This document provides a summary description of a dataset used in Harper et al. (2018) to study land-use and climate interventions under the Paris Agreement, using JULES (Joint UK Land Environment Simulator) and IMOGEN to emulate climate–carbon cycle impacts across multiple GCMs.
- The dataset links land-use scenarios, temperature pathways, and CO2 regimes to carbon stocks and surface energy budget variables, enabling analysis of land-based climate mitigation implications.

## Experimental Design

- Six simulations representing a factorial combination of three global warming/CO2 pathways and two land-use scenarios:
  - Temperature/CO2 pathways: 2°C (2deg), 1.5°C (1p5deg), and 2°C with 1.5°C CO2 (2deg_1p5CO2)
  - Land-use scenarios: IM19 and IM26 (IMAGE SSP2-SPA0-RCP1.9 and SSP2-SPA2-RCP2.6)
- Directory structure for the six simulations:
  - 1p5deg_IM19
  - 1p5deg_IM26
  - 2deg_IM19
  - 2deg_IM26
  - 2deg_IM19_1p5CO2
  - 2deg_IM26_1p5CO2
- Models and links:
  - JULES large-scale global land surface model (v4.8) with multi-layer soil carbon
  - IMOGEN emulator using CMIP5 GCM outputs to represent 34 GCMs in CMIP5
- Related datasets:
  - CMIP5 GCM outputs used to drive JULES-IMOGEN (linked in EIDC)
  - Outputs for 1850–2000 available in a linked dataset
- Relevance: Experimental design aligns with Comyn-Platt et al. (2018) and Harper et al. (2018) for evaluating land-use emissions and mitigation targets.

## Data and Variables

- Time coverage:
  - Variables provided for 2000–2099 (inclusive)
  - 1850–1999 data exist in a linked dataset from Comyn-Platt et al. (2018)
- CarbonStocks variables (dimensions and units provided in file headers):
  - cv: gridbox total vegetation carbon (kg m-2); time, latitude, longitude
  - cs_gb: gridbox total soil carbon (kg m-2); time, latitude, longitude
  - frac: fractional cover of each surface type (dimensioned by time, type, latitude, longitude)
  - npp: net primary productivity on vegetated tiles (kg m-2 s-1); time, pft, latitude, longitude
  - harvest: harvest on crop tiles (kg m-2 s-1); time, pft, latitude, longitude
  - ccs_gb: grid box accumulated carbon in BECCS pool (kg m-2); time, latitude, longitude
  - Frac_agr: fraction of grid box cropped (time, latitude, longitude)
  - Frac_biocrop: fraction of grid box with bioenergy crops (time, latitude, longitude)
  - Frac_past: fraction of grid box pasture (time, latitude, longitude)
  - wood_products: carbon content in wood products pools (kg m-2); time, latitude, longitude
  - co2_ppmv: CO2 concentration in ppmv (time, global)
- WaterCycle variables (dimensions and units provided in file headers):
  - t_soil: sub-surface soil temperature (K); time, soil, latitude, longitude
  - smcl: sub-surface soil moisture content (kg m-2); time, soil, latitude, longitude
  - Swet_tot: soil moisture as fraction of saturation; time, latitude, longitude
  - Fqw_gb: soil moisture flux from surface (kg m-2 s-1)
  - Ftl_gb: surface sensible heat flux (W m-2)
  - fwetl: wetland fraction (dimensionless)
  - runoff: grid box runoff rate (kg m-2 s-1)
  - zw: depth to water table (m)
- Ancillary and metadata:
  - NetCDF files are self-describing; standard tools (R, Python, NCO) can read them
  - Variable values are structured to support grid-box summations and area-weighted analyses

## Data Structure and Access

- File naming:
  - CarbonStocks: BL_CEN_<centre>_MOD_<model>_<scenario>.CarbonStocks.2000-2099.nc
  - WaterCycle: BL_CEN_<centre>_MOD_<model>_<scenario>.WaterCycle.2000-2099.nc
  - <centre> is the GCM centre; <model> is the GCM model; <scenario> is one of 2deg, 1p5deg, 2deg_IMxx_1p5CO2, etc.
- Temporal coverage:
  - Primary data: 2000–2099
  - Historical period (1850–1999) data available in linked Comyn-Platt et al. dataset
- Data interpretation notes:
  - IMOGEN emulates 34 CMIP5 models to drive JULES; file headers provide model-specific context
  - The dataset supports investigating land-use emissions and climate mitigation under specified warming targets

## Ancillary Files and Running the Model

- Ancillary files included to run the rose suites for JULES-IMOGEN:
  - Model grid definitions (grid_info.nc, imogen_order.dat, points.all.dat)
  - Initial CO2 concentration (SSP2.6_IMAGE_concs_co2.txt; updated within JULES-IMOGEN)
  - CO2 concentration prescriptions for 2C climate with 1.5C CO2 (co2_experiment)
  - Non-CO2 radiative forcing and atmospheric composition (HadGEM_O3coeffs_imogen.nc; SSP2-6_IMAGE_concs_ch4_n2o.txt; SSP2-6_IMAGE_qnonco2.txt)
  - Land cover files for IM1.9 and IM2.6 scenarios (landcover_1700-2100_ImogenGrid.nc)
  - Initial condition files for each GCM and temperature scenario (to start at 2000)
- Rose suites:
  - IM1.9 and IM2.6 configurations with different temperature scenarios and CO2 prescriptions; details available from code.metoffice.gov.uk (registration required)

## Important Usage Notes

- Calculating grid-box totals:
  - Each grid box comprises 17 tiles (13 plant types and 4 non-vegetated tiles)
  - NPP per PFT assumes full-gridbox occupation; to compute grid-box total NPP, perform a weighted sum using frac as weights
- Tile naming (examples of 17 tiles):
  - brdlf decid trees, tropical broadleaf evergreen trees, temperate broadleaf evergreen trees, ndlf decid trees, ndlf evergreen trees, natural C3 grass, C3 crops (incl. bio), C3 pasture, natural C4 grass, C4 crops (incl. bio), C4 pasture, decid shrubs, evergreen shrubs, urban, water, bare soil, ice

## Appendix and References

- Appendix provides a list of CMIP5 modelling centres and GCM names used in IMOGEN (mapping to CMIP5 data portal terminology)
- Main references:
  - Harper et al. 2018a and 2018b for JULES/IMOGEN methodology and plant functional types
  - Comyn-Platt et al. 2018 for carbon budgets under 1.5°C and 2°C targets
  - Huntingford and Cox (2000), Huntingford et al. (2010) for IMOGEN framework
  - Taylor et al. (2012) for CMIP5 overview and experimental design