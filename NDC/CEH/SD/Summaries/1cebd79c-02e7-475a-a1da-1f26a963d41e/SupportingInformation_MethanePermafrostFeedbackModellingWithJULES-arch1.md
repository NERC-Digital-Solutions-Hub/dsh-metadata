# Background, Experiment Design and Analytical Methods

- Purpose and context
  - Dataset used in the published Comyn-Platt et al. (2018) article; describes data underlying carbon-budget analyses for 1.5°C and 2°C warming targets.
  - Combines the Joint UK Land Environment Simulator (JULES, v4.8) with a multi-layer soil-carbon model and operates within the IMOGEN climate–carbon cycle emulator to derive anthropogenic fossil fuel emission budgets from pattern-scaled CMIP5 GCMs.

- Modelling framework
  - JULES used for global land-surface processes; IMOGEN provides an inverted, pattern-scaled climate/meteorology driver to emulate 34 CMIP5 GCMs.
  - Outputs include global warming variables, land-cover, natural wetlands, CH4 fluxes, soil temperature/moisture, and carbon stocks.

- Experimental design (factorial)
  - 12 simulations representing a 3 × 4 factorial:
    - Temperature pathways (three): 2deg (2°C target by 2100), 1p5deg (1.5°C target by 2100), 1p5degOS (1.5°C with overshoot to ~1.75°C).
    - Model configurations (four): BLco (baseline, no methane feedback), CH4_lowQ10 (low methane-temperature sensitivity), CH4_poorFEN (poor fen wetlands methane response), CH4_richFEN (rich fen wetlands methane response).

- Data scope and outputs
  - Time period: 1850–2099 (NetCDF files self-describing for standard tools).
  - Key variables (examples):
    - cv: gridbox vegetation carbon; cs_gb: soil carbon; cs_old_gc: pre-industrial permafrost carbon; fch4_wetl_cs: scaled methane flux from wetlands.
    - frac: fractional land-cover; t_soil: soil temperature; smcl: soil moisture; fwetl: wetland fraction; wood_products: wood product carbon.
    - co2_ppmv: CO2 in air; ch4_ppbv: CH4 in air; dtemp_g/o/l: global/land/ocean warming; Ocean_uptake: ocean uptake of perturbed CO2.
  - Outputs are designed to compute anthropogenic fossil fuel emissions as the residual yearly changes among carbon pools.

- Data structure and accessibility
  - File format and organization
    - NetCDF files; self-describing headers; accessible with standard tools (R, Python, nco).
    - File naming structure: exp/scenario/exp_CEN_center_MOD_scenario.CarbonStocks.1850-2099.nc
    - Directory layout reflects the four experiment configurations (BLco, CH4_lowQ10, CH4_poorFEN, CH4_richFEN) and three temperature pathways (2deg, 1p5deg, 1p5degOS).
  - Metadata and usability
    - Variables include units and dimensions (time, latitude, longitude, etc.).
    - The dataset is designed to support visualization and further analysis, with documentation referenced in companion papers.

- Quality control and context
  - JULES is maintained to high standards due to its role in UK Earth System Modeling; modelling outputs are robust and designed for integration into policy-relevant assessments.
  - The dataset builds on prior research linking methanogenesis (Gedney et al., 2004) and permafrost dynamics (Burke et al., 2018) within the JULES/IMOGEN framework.

- Appendix and references
  - Appendix lists the climate modelling centres and GCM names used in IMOGEN (mapping to CMIP5 models).
  - References include key methodological papers for JULES, IMOGEN, and related climate–carbon cycle studies (e.g., Comyn-Platt et al. 2018; Huntingford & Cox 2000; Taylor et al. 2012).