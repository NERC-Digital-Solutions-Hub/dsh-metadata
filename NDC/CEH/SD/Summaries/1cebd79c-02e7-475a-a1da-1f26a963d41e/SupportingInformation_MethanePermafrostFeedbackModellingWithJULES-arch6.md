# Background, Experiment Design and Analytical Methods

## Overview
- Presents 12 sets of model output from JULES (land surface model) combined with IMOGEN (climate-carbon cycle emulator) to study carbon budgets and warming targets.
- Aims to understand implications for meeting 1.5°C and 2°C targets, accounting for natural wetlands and permafrost feedbacks.
- Outputs cover global carbon stocks (land, atmosphere, ocean), greenhouse gas concentrations, land cover, and climate response variables, enabling analysis of fossil fuel emission residuals and feedbacks.

## Experimental Design
- Factorial design with three global warming pathways and four model configurations:
  - Pathways: 2deg (2°C by 2100), 1p5deg (1.5°C by 2100), 1p5degOS (1.5°C with overshoot to 1.75°C)
  - Configurations: BLco (baseline without methane feedback), CH4_lowQ10 (low methane temperature sensitivity), CH4_poorFEN (poor fen-like methane response), CH4_richFEN (rich fen-like methane response)
- Purpose: evaluate how methane feedbacks and permafrost/wetland processes influence carbon budgets and warming scenarios.

## Data Content and Variables
- Data modality: NetCDF files (self-describing with standard headers) accessible by common tools (R, Python, nco).
- Temporal coverage: 1850–2099.
- Key variables (with units and dimensions):
  - cv: Gridbox total vegetation carbon (kg m^-2)
  - cs_gb: Gridbox total soil carbon (kg m^-2)
  - cs_old_gc: Gridbox total labelled soil carbon (pre-industrial permafrost carbon) (kg m^-2)
  - fch4_wetl_cs: Scaled methane flux from wetlands (kg m^-2 s^-1) — 1960–2100
  - frac: Fractional cover of surface types
  - t_soil: Soil temperature by layer (K)
  - smcl: Soil moisture content by layer (kg m^-2)
  - fwetl: Wetland fraction
  - wood_products: Wood products carbon pool (K kg m^-2)
  - co2_ppmv: CO2 concentration in air (ppmv)
  - ch4_ppbv: CH4 concentration in air (ppbv)
  - dtemp_g: Global warming for land/overall (K)
  - dtemp_o: Global warming of ocean layers (K)
  - dtemp_l: Global warming over land (K)
  - Ocean_uptake: Global accumulated ocean uptake of perturbed CO2 (Pg C)
- Dimensions overview: time, latitude, longitude (and additional axes for some variables like soil layer, type, or ocean level as specified).

## File Naming and Organization
- File path structure: «exp»/«scenario»/«exp»_CEN_«centre»_MOD_«model»_«scenario».CarbonStocks.1850-2099.nc
  - Exp: BLco, CH4_lowQ10, CH4_poorFEN, CH4_richFEN
  - Scenario: 2deg, 1p5deg, 1p5degOS
  - centre/model: CMIP5 CMIP centres and GCMs
- Each folder contains a specific experiment configuration and scenario, enabling straightforward retrieval of a given simulation.

## Data Access and Usage
- Data are suitable for:
  - Analyzing carbon budgets and emissions residuals
  - Assessing the impact of methane feedbacks and permafrost/wetland processes on warming trajectories
  - Developing data products and self-service analyses around carbon stocks and climate responses
- Documentation references peer-reviewed work (Comyn-Platt et al. 2018) and underlying components (JULES, IMOGEN, CMIP5).

## Quality and References
- JULES: Maintained to high standards with robust numerical stability within Met Office model framework.
- Related foundational work and data sources cited, including:
  - Gedney (2004), Burke et al. (2018), Clark et al. (2011), Huntingford & Cox (2000, 2010), Taylor et al. (2012), Comyn-Platt et al. (2018).
- Appendix lists the CMIP5 centres and GCMs used to drive the IMOGEN emulator and JULES model variants.