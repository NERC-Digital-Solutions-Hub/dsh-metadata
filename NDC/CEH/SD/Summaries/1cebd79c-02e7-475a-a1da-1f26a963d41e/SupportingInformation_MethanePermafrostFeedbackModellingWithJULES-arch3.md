# Background, Experiment Design and Analytical Methods

- Purpose: Describe a dataset and analytical framework used to explore climate-carbon cycle interactions and their implications for meeting warming targets, supporting monitoring and evaluation of policy scenarios.
- Context for monitoring: Provides a structured set of model outputs (land surface, atmosphere, wetlands, permafrost, and methane feedbacks) that can inform environmental health and policy scrutiny, including how natural feedbacks modify carbon budgets under different warming scenarios.

## Experimental Design and Data Sources

- Models used: Joint UK Land Environment Simulator (JULES; v4.8) with a multi-layer soil-carbon model, operated globally within an inverted IMOGEN climate-carbon cycle system.
- Emulation approach: IMOGEN uses a pattern-scaling method to emulate 34 CMIP5 GCMs, enabling a climate and meteorology context for JULES outputs.
- Output sets: 12 simulations derived from factorial combinations of three temperature pathways and four methane/feedback configurations.
- Purpose of outputs: To derive carbon stocks, greenhouse gas fluxes, and warming metrics needed to calculate anthropogenic fossil fuel emissions as the residual of yearly changes.

## Experimental Pathways and Configurations

- Temperature pathways (three): 
  - 2deg: Stabilisation at 2°C by 2100 from below
  - 1p5deg: Stabilisation at 1.5°C by 2100 from below
  - 1p5degOS: Overshoot to 1.75°C with eventual stabilisation at 1.5°C by 2100
- Model configurations (four methane/soil carbon setups):
  - BLco: Baseline without methane feedback
  - CH4_lowQ10: Low temperature sensitivity of methanogenesis
  - CH4_poorFEN: Poor fen-like methanogenesis sensitivity
  - CH4_richFEN: Rich fen-like methanogenesis sensitivity

## Data Structure, Variables and Timeframe

- Timeframe: 1850–2099 (inclusive)
- Data format: NetCDF files; self-describing headers; readable with standard tools (R, Python, nco)
- Key variables (with units and dimensions): 
  - cv: Gridbox total vegetation carbon (kg m^-2)
  - cs_gb: Gridbox total soil carbon (kg m^-2)
  - cs_old_gc: Gridbox total labelled soil carbon (pre-industrial permafrost carbon; kg m^-2)
  - fch4_wetl_cs: Scaled methane flux from wetlands (kg m^-2 s^-1)
  - frac: Fractional cover of surface types (dimension: time, type, lat, lon)
  - t_soil: Sub-surface soil temperature (K)
  - smcl: Sub-surface soil moisture content (kg m^-2)
  - fwetl: Wetland fraction (dimension: time, lat, lon)
  - wood_products: Wood products carbon pools (K g m^-2)
  - co2_ppmv: CO2 concentration (ppmv; global)
  - ch4_ppbv: CH4 concentration (ppbv; global)
  - dtemp_g, dtemp_o, dtemp_l: Global warming signals (K) for ground/ocean/land
  - Ocean_uptake: Global accumulated ocean uptake of perturbed CO2 (Pg C)
- Global scope: Variables provided to support analyses of land, atmosphere, ocean carbon stocks and temperature responses.

## File Organisation and Access

- File naming convention: exp/scenario/exp_CEN_center_MOD_model_scenario.CarbonStocks.1850-2099.nc
  - exp: one of BLco, CH4_lowQ10, CH4_poorFEN, CH4_richFEN
  - scenario: 2deg, 1p5deg, or 1p5degOS
  - centre/model: GCM centre and model names from CMIP5, as listed in the appendix
- Organisation: Output stored in separate folders by experiment configuration, with subfolders for each scenario
- Accessibility: NetCDF files are designed to be readable with standard data analysis tools; metadata is embedded in headers for ease of use

## Quality Control, Data Governance and Usage

- Quality control: JULES maintained to high standards due to ties to UK Earth System Modelling effort; emphasis on numerical stability and accuracy within Met Office model framework
- Data provenance and transparency: Datasets are described with explicit variable definitions, units, and dimensions; outputs used to calculate fossil fuel emission budgets as the yearly residual of changes
- Metadata considerations: NetCDF headers provide structure and units; some metadata may require careful verification to ensure suitability for specific monitoring needs
- Data sharing and governance: Outputs are designed for openness and reuse; underlying data and descriptions support clear communication of methods and findings to stakeholders

## Context and References

- Related foundational work: Permafrost thaw and wetlands feedbacks studied in Burke et al. (2018); methane wetland studies (Gedney et al., 2004); JULES model description and carbon fluxes (Clark et al., 2011); IMOGEN framework (Huntingford and Cox, 2000; Huntingford et al., 2010); CMIP5 overview (Taylor et al., 2012)
- Usage note: The simulations underpin analyses presented in Comyn-Platt et al. (2018); the methodology is linked to broader climate-carbon cycle research and supports interpretation of policy-relevant warming targets

## Appendix: Modelling Centres and GCMs

- Table listing participating modelling centres and corresponding GCM names used to drive JULES via IMOGEN (e.g., BCC, BNU, CCCma, CMCC, CNRM-CERFACS, CSIRO, INM, IPSL, MIROC, MOHC, MPI-M, MRI, NASA-GISS, NCAR, NCC, NOAA-GFDL, NSF-DOE-NCAR)
- Provides the precise centre/model combinations that underpin the 34 CMIP5-based configurations used for pattern scaling in IMOGEN