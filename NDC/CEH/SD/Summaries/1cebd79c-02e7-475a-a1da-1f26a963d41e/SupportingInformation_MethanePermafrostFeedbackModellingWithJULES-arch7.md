# Background, Experiment Design and Analytical Methods

- This dataset corresponds to the data used in the published Comyn-Platt et al. (2018) article, with a summary description provided here and full details in the associated data citation article.
- Objective: to explore climate-carbon-cycle feedbacks and fossil-fuel emission budgets using an integrated modelling framework.
- Modelling framework:
  - JULES (Joint UK Land Environment Simulator, version 4.8) large-scale global land surface model with a multi-layered soil-carbon component.
  - IMOGEN emulator (inverted climate-carbon cycle impacts system) to emulate climate and meteorology from CMIP5 GCMs via pattern scaling.
- Experimental design:
  - 12 simulations across a factorial combination of three global warming pathways and four methane-related model configurations.
  - Temperature pathways: 2deg (2°C by 2100), 1p5deg (1.5°C by 2100), 1p5degOS (1.5°C by 2100 with overshoot to 1.75°C).
  - Model configurations: BLco (baseline), CH4_lowQ10, CH4_poorFEN, CH4_richFEN (vary methane feedback and fen-type wetland properties).
- Output purpose: provide carbon stocks, greenhouse gas fluxes, and warming indicators to assess anthropogenic fossil-fuel emission budgets and climate-carbon feedbacks.

## Data content for GIS and map-based visualisation

- Carbon stocks and pools
  - cv: gridbox total vegetation carbon (kg m-2)
  - cs_gb: gridbox total soil carbon (kg m-2)
  - cs_old_gc: labelled soil carbon pre-industrial permafrost carbon (kg m-2)
  - wood_products: carbon content of wood products pools (kg m-2)
- Methane and greenhouse gas fluxes
  - fch4_wetl_cs: scaled methane flux from wetlands (kg m-2 s-1; 1960-2100 period available)
  - ch4_ppbv: methane mixing ratio (ppbv; global)
  - co2_ppmv: CO2 mixing ratio in air (ppmv; global)
- Surface types and climate state
  - frac: fractional cover of each surface type (dimension: time, type, latitude, longitude)
  - fwetl: wetland fraction (dimension: time, latitude, longitude)
  - t_soil: sub-surface soil temperature by soil layer (K; time, soil, latitude, longitude)
  - smcl: sub-surface soil moisture by soil layer (kg m-2; time, soil, latitude, longitude)
- Global warming indicators
  - dtemp_g: global warming (K; time, global)
  - dtemp_l: warming over land (K; time, global)
  - dtemp_o: warming of each ocean layer (K; time, olevel)
- Ocean uptake
  - Ocean_uptake: global accumulated ocean uptake of perturbed CO2 (Pg C; time, global)

## Data structure, access, and formats

- File format: NetCDF, self-describing with headers; suitable for reading in standard GIS/analysis tools.
- Accessibility: standard packages (R, Python, NCO, etc.) can read and visualise the data.
- Time coverage: 1850–2099 (inclusive) for applicable variables.
- Spatial structure: gridded global data for most variables; some have a global dimension (co2_ppmv, ch4_ppbv, dtemp_g) instead of a latitude/longitude grid.
- Variable metadata: includes descriptions, units, and dimensions (time, latitude, longitude; or time, type, latitude, longitude; or time, global; etc.).

## Data organization and naming

- File naming pattern: exp/scenario/exp_CEN_center_MOD_model_Scenario.CarbonStocks.1850-2099.nc
  - exp: one of BLco, CH4_lowQ10, CH4_poorFEN, CH4_richFEN
  - scenario: 2deg, 1p5deg, 1p5degOS
  - center/model: GCM centre and model names matching CMIP5 portal
- Directory structure: separate folders for each experiment configuration with subfolders per scenario.

## Quality, provenance and context

- JULES modelling system is maintained to high standards due to its link to UK Earth System Modelling efforts; aims for numerical stability and accuracy.
- Data and simulations underpin the research in Comyn-Platt et al. (2018); linked to foundational studies on methanogenesis, permafrost, wetland carbon, and the IMOGEN framework.
- References provide context for model components (JULES, IMOGEN) and supporting climate-science literature.

## GIS usage considerations and workflow notes

- Multi-model ensemble: useful for ensemble visualisations and uncertainty assessments; consider weighting or comparing configurations across the three warming pathways.
- Data handling: large and potentially complex; plan for data management, chunking, and possible downscaling or regridding to compatible GIS grids.
- Metadata and standards: ensure metadata alignment with local GIS data standards; verify coordinate reference systems and grid definitions when integrating with other spatial datasets.
- Visualization opportunities:
  - Map carbon stocks (cv, cs_gb, cs_old_gc) and their changes over time.
  - Visualise wetland dynamics (fwetl, fwetl) and methane fluxes (fch4_wetl_cs).
  - Map soil temperature/moisture profiles (t_soil, smcl) and global warming indicators (dtemp_g, dtemp_o, dtemp_l).
  - Track atmospheric drivers (co2_ppmv, ch4_ppbv) and ocean uptake (Ocean_uptake).
- Data integration: combine with other land-use, climate, or policy datasets to assess impacts under different warming targets and methane feedback scenarios.

## References and provenance

- Core datasets and modelling framework: Comyn-Platt et al. (2018), Gedney et al. (2004), Burke et al. (2018), Clark et al. (2011), Huntingford & Cox (2000), Huntingford et al. (2010), Taylor et al. (2012).
- Appendix: List of modelling centres and GCMs used to drive JULES via IMOGEN (CMIP5-based).