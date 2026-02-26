# Background, Experiment Design and Analytical Methods

- Purpose and scope
  - Describes a dataset used in the Comyn-Platt et al. (2018) study to understand climate–carbon–wetland feedbacks and their implications for warming targets.
  - Combines a global land-surface model (JULES v4.8) with an emulator (IMOGEN) to explore the carbon cycle and climate response under different warming pathways.
  - Aims to support analysis of environmental health and policy performance by providing long-term, standardized model outputs.

- Modelling framework and workflow
  - JULES: Global land-surface model with multi-layer soil-carbon dynamics; used to generate carbon stocks and surface processes.
  - IMOGEN: Intermediate-complexity emulator that patterns-climate variability from CMIP5 GCMs to drive JULES outputs; supplies prescribed temperature pathways.
  - The combination yields estimates of anthropogenic fossil fuel emissions as the residual annual change in carbon stores (land, atmosphere, ocean).

- Experimental design (factorial)
  - Temperature pathways (3 total):
    - 2deg: Stabilisation at 2°C by 2100 from below
    - 1p5deg: Stabilisation at 1.5°C by 2100 from below
    - 1p5degOS: Stabilisation at 1.5°C by 2100 with overshoot to 1.75°C
  - Model configurations (4 total) regarding methane feedback:
    - BLco: Baseline, no methane feedback
    - CH4_lowQ10: Low temperature sensitivity of methanogenesis
    - CH4_poorFEN: Methanogenesis sensitivity like poor fen wetlands
    - CH4_richFEN: Methanogenesis sensitivity like rich fen wetlands
  - 12 simulation runs: All combinations of the 3 pathways × 4 configurations

- Data and outputs
  - Primary outputs: Carbon stocks (land, atmosphere, ocean); global warming indicators; fractional land-cover; methane flux; soil temperature and moisture; wetland fraction; wood products pool; CO2 and CH4 concentrations.
  - Time coverage: 1850–2099 (inclusive).
  - Additional metrics: Dtemp (global, land, ocean), ocean uptake of perturbed CO2, and related climate-feedback variables.
  - File contents: NetCDF files with self-describing headers; designed for use with common analysis tools.

- Variables and meanings (selected)
  - cv: Gridbox total vegetation carbon (kg m-2)
  - cs_gb: Gridbox total soil carbon (kg m-2)
  - cs_old_gc: Gridbox labelled soil carbon (pre-industrial permafrost carbon) (kg m-2)
  - fch4_wetl_cs: Scaled methane flux from wetlands (kg m-2 s-1; 1960–2100)
  - frac: Fractional cover of surface types
  - t_soil: Sub-surface soil temperature (K)
  - smcl: Sub-surface soil moisture (kg m-2)
  - fwetl: Wetland fraction
  - co2_ppmv, ch4_ppbv: Atmospheric CO2 and CH4 concentrations
  - dtemp_g/o/l: Global/land/ocean warming (K)
  - Ocean_uptake: Global accumulated ocean uptake of perturbed CO2 (Pg C)
  - wood_products: Carbon in wood-product pools

- Data structure and accessibility
  - Time series and spatial grids stored in NetCDF files; standard dimensions include time, latitude, longitude (and others for some variables like surface type and global dimensions for atmospheric gases).
  - File naming and organization:
    - exp/scenario/exp_CEN_center_MOD_model_CarbonStocks.1850-2099.nc
    - Exp: BLco, CH4_lowQ10, CH4_poorFEN, CH4_richFEN
    - Scenario: 2deg, 1p5deg, 1p5degOS
    - Center/model identifiers correspond to CMIP5 GCM nomenclature
  - Access and usage: NetCDF headers enable reading with common tools (R, Python, nco) for visualization and analysis.

- Quality control and context
  - JULES is maintained to high standards due to ties with UK Earth System Modelling efforts; emphasis on numerical stability and accuracy within the Met Office modelling framework.
  - Documentation connects to broader literature on methanogenesis, permafrost, and the IMOGEN/JULES modelling chain.

- Practical relevance for analysts monitoring the environment
  - Provides a structured, repeatable dataset to assess how different climate–carbon feedbacks could influence emissions budgets and warming trajectories.
  - Facilitates cross-dataset integration by offering standardized outputs (carbon stocks, greenhouse gas concentrations, temperature responses) suitable for monitoring environmental health and policy performance over long timescales.
  - Appendix lists climate modelling centres and GCMs used to drive the IMOGEN emulator, aiding transparency and dataset provenance.

- References and context
  - Core studies and model descriptions underpinning the dataset include Comyn-Platt et al. (2018), Gedney et al. (2004), Burke et al. (2018), Clark et al. (2011), Huntingford et al. (2000, 2010), Taylor et al. (2012).