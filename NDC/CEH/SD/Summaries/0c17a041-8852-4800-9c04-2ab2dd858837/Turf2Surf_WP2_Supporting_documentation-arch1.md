# Turf2Surf WP2 Supporting documentation for data

## Overview
- documentation for Turf2Surf WP2 focusing on nitrogen and phosphorus impacts on carbon exchange between land and atmosphere.
- project aims include linking plant and soil nutrients to ecosystem processes and incorporating parameters into the JULES model.
- principal data types cover aboveground biomass, productivity, photosynthesis, leaf traits, soil chemistry, root data, and elemental composition.

## Study area and context
- Conwy catchment, North Wales (~500 km2), diverse landscapes enabling holistic ecological, biogeochemical, and hydrological studies.
- climatic gradient across the catchment; range of habitats including blanket bog, moorland, woodlands, grasslands, lakes, floodplains, and estuary interactions.
- stakeholders include water utilities, farming, forestry, conservation groups, and local communities.
- data are intended to support broad-scale and site-specific analyses of pressures on resources and ecosystem services.

## Sampling design and habitats
- 17 sites across the Conwy catchment with multiple habitat types (e.g., blanket bog, heaths, conifer and broadleaf woodlands, grasslands, arable land).
- Table 1 lists unique site numbers, plots per site, locations, and dominant plant communities.
- Sampling captures a wide range of plant communities to enable cross-site comparisons and model parameterization.

## Data domains and key measures

### 1) Aboveground plant data
- 1.1 Aboveground net primary productivity (NPP) and standing biomass
  - annual NPP measured 2013–2015 for dominant species at all sites; four plots per site.
  - winter clipping with grazing exclusion (where applicable) to standardize growth.
  - standing biomass measured at 10 of 17 sites; biomass estimation for grasses/bogs via 1 m x 1 m quadrats; woodland biomass via tree cores and leaf litter.
  - NPP adjustments account for plant life-cycle strategies.
- 1.2 Plant photosynthesis measures
  - Vcmax, Jmax, Asat measured for dominant species using CIRAS-I and Licor devices over multiple years.
  - A-Ci curve fitting and temperature corrections performed with established models and scripts (GitHub: mdekauwe/FitFarquharModel).
  - Data processing and interpretation linked to JULES parameterization of photosynthesis processes.

### 2) Plant traits and community traits
- 2.1 Leaf traits and community metrics
  - measurements of leaf N and P, LDMC, SLA, LMA, canopy height, bryophyte cover.
  - LMA determined from 10 leaves per sampling area; leaf area via ImageJ; dry weight after 65°C drying.
  - N and P quantified with appropriate laboratory methods; SLA derived as inverse of LMA.
- All trait data contribute to parameterizing JULES and understanding plant functional strategies.

### 3) Soil and belowground data
- 3.1 General soil measures
  - intact soil cores collected spring 2014, depth to 1 m, across 17 habitats (3 cores per habitat).
  - depth-stratified analyses (0–15, 15–30, 30–45, 45–60, 60–75, 75–90, 90+ cm).
  - measured: soil water content (SWC), bulk density (BD), LOI and LOI-C, pH, EC, total C (C_tot) and total N (N_tot).
- 3.2 Phosphorus (P) fractions
  - Olsen P, Root-P, Complex-P, Enzyme-P, and Protons-P fractions measured with multiple extraction schemes and colorimetric assays.
  - standardized colorimetric procedures (Malachite Green) for P quantification; root P extracted with CaCl2 for comparison with root-accessible P pools.
- 3.3 Available carbon and nitrogen
  - DOC and TDN analyzed from 0.5 M K2SO4 extracts; NO3 and NH4 quantified via standardized microplate methods.
  - detailed extraction, QA/QC, and instrumental analysis described.
- 3.4 Soil available cations
  - Ca, Na, K extracted with 0.5 M acetic acid; measured using a flame photometer.
- 3.5 Root biomass and growth
  - total and fine root biomass measured at several sites using 15 cm soil cores; roots scanned with WinRhizo for morphometrics and then dried for biomass.
  - in-growth root cores deployed to assess root growth over a growing season; detailed field setup and measurement described.
- 3.6 Soil elements by TXRF
  - Total elemental composition (many elements: Al, Fe, Ca, K, etc.) analyzed by TXRF (Bruker S2 PICOFOX).
  - sample prep includes digestion, grinding, and disc preparation; limitations discussed in a companion TXRF limitations file.
- Data processing and integration notes emphasize linking plant and soil nutrients to ecosystem processes for JULES.

## Dataset structure and access
- Five data files are provided:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Column mappings
  - Column A: unique Site number (as in Table 1)
  - Column B: Habitat name
  - Column C: Detailed habitat description
  - Column D: Site name
  - Column E: Ecosystem Component (Plant, soil, or roots)
  - Column F: For Plant components, specific plant species; otherwise NA
  - Columns G and H: Plot number (1–4) and Replicate number (when applicable)
  - Column I: Soil depth interval for soil and roots components
- Missing values are indicated as NA
- Dataset design supports cross-tabulations across sites, habitats, and ecosystem components; enables linking to model parameters and downstream analyses.

## Data processing, tooling, and accessibility
- Authors and data stewards per section (e.g., Simon Smart for NPP, Lina Mercado for photosynthesis, CEH Bangor for soil measures).
- Scripts and modeling workflows referenced (e.g., Farquhar model implementation, Levenberg–Marquardt fitting, and JULES parameter linking) with public code access where noted.
- TXRF limitations documented in a separate file; multiple QA/QC steps described for C, N, P analyses.
- Data are intended to be discoverable and usable, with metadata and dataset provenance tracked.

## Versioning and authorship
- Version dates: 01/06/2016, 25/08/2016, 04/11/2016.
- Authors include Sabine Reinsch (corresponding author), Helen Glanville, Simon Smart, Lina Mercado, and others across CEH and partner universities.
- Contact details provided per data domain for data provenance and queries.

## Practical implications for analysis
- Rich, multi-domain dataset suitable for correlating plant productivity and photosynthesis metrics with soil nutrient pools and root dynamics.
- Suitable for testing hypotheses about nutrient limitation, carbon flux coupling, and ecosystem responses across a climatic and habitat gradient.
- Provides parameterizable data for integration into the JULES model and for exploring trait-based predictors of ecosystem processes.
- Be mindful of data gaps at certain sites or habitats, depth-specific data limitations, and TXRF limitations when interpreting elemental results.