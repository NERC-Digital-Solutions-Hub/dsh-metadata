# Turf2Surf WP2 Supporting documentation for data

## Aim
- Document data from Turf2Surf WP2 focusing on nitrogen and phosphorus impacts on carbon exchange between land and atmosphere within coupled nutrient cycling in terrestrial and freshwater ecosystems.
- Emphasize data standardization, quality assurance, and the linkage of plant and soil nutrient data to ecosystem processes and models (e.g., JULES).

## Project and team
- Members: Bridget Emmett (CEH), Davey Jones (Bangor University), Simon Smart (CEH), Lina Mercado (Exeter University), Helen Glanville (Bangor University), Maria C Blanes (CEH), Harry Harmens (CEH), Sabine Reinsch (CEH).
- Authors: Sabine Reinsch (corresponding), Helen Glanville, Simon Smart.
- Data responsibilities span aboveground and belowground plant and soil measurements, with data processing linked to the JULES model.

## Study area
- Conwy catchment, North Wales (~500 km2) with diverse landscapes and a climatic gradient (precipitation 500–1064 mm).
- Rich set of habitats: blanket bog, montane moorland, conifer plantations, various grasslands, lakes/reservoirs, flood plains, salt marshes, woodlands.
- Stakeholders include water utilities, farmers, foresters, tourism, conservation groups and local communities.
- Extensive baseline data exist for comparative research across ecological, biogeochemical, and hydrological processes.

## Habitats and sampling sites
- 17 habitats sampled; site list includes 23 unique plots/sites with varied dominant vegetation (e.g., blanket bog, heather on bog, acid grassland, conifer woodland, oakwood, broadleaved woodland, hay meadows, improved and semi-improved grasslands, arable, montane sites).
- Sampling design includes multiple plots per habitat (mostly 1–4 plots per site) for representative dominant species.
- Aboveground net primary productivity (NPP) measured annually (2013–2015) across dominant plant species at all sites; standing biomass measured at 10 of 17 sites.

## Key data and methods

### 3.1.1 Aboveground net primary productivity and standing biomass
- Data responsibility: Simon Smart.
- NPP: annual measurements for dominant species at all sites; four plots per site; winter clipping and grazing protection where applicable; adjustments for life-history strategies.
- Standing biomass: measured at 10 sites using herbaceous biomass in 1 m x 1 m quadrats and tree/shrub biomass via random 200 m2 plots and tree cores; biomass per m2 calculated with species- and site-specific approaches.
- Aim: link plant productivity and biomass to nutrient cycling, informing JULES parameterization.

### 3.1.2 Plant photosynthesis measures
- Data responsibility: Lina Mercado.
- Parameters: Asat, Vcmax, Jmax (25°C) measured for dominant species.
- Methods: field CO2 curves using CIRAS-I with various CO2 setups; 2013–2016 measurements; data processed with Farquhar-based models and temperature corrections; scripts available for fitting (GitHub link provided).
- Output contributes to understanding photosynthetic capacity for model integration (JULES).

### 3.1.3 Leaf traits and plant community traits
- Data responsibility: Lina Mercado and Simon Smart.
- Measurements: leaf N and P, leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover.
- LMA: derived from leaf area via ImageJ; leaves dried at 65°C for weight; N and P analyses via Vario and chemical digestion.
- Purpose: relate leaf economics to nutrient availability and carbon flux; link to plant and soil processes in JULES.

### 3.2.1 General soil measures
- Data responsibility: Helen Glanville.
- Methods: intact soil cores (0–1 m) from 17 habitats; depth-stratified sampling (0–15 up to 90+ cm); analyses include soil water content, bulk density, LOI and LOI-C, pH, EC, total C and N (thermal oxidation).
- QA/QC and multi-operator involvement to ensure robust soil baselines for carbon and nutrient pools.

### 3.2.2 Phosphorus
- Data responsibility: Helen Glanville.
- Phosphorus pools measured: Olsen P, Root-P (CaCl2 extraction), Complex-P (10 mM citrate extraction), Enzyme-P (phosphatase and phytase activity), Proton-P (1 M HCl).
- Analytical method: colorimetric malachite green for P; standardized protocols with detailed extraction steps.
- Goal: resolve multiple P pools and availability drivers for plant uptake and soil biogeochemistry.

### 3.2.3 Available carbon and nitrogen
- Data responsibility: Helen Glanville.
- Methods: soil C and N extraction with 0.5 M K2SO4; nitrate and ammonium analyzed by colorimetric/standard methods; DOC and TDN via CEH Bangor with TOC analyzer and QA protocols.
- Output: dissolved and mineral N and C pools informing soil–plant–microbial interactions.

### 3.2.4 Soil available cations (Ca, Na, K)
- Data responsibility: Helen Glanville.
- Methods: extraction with 0.5 M acetic acid; analysis by flame photometry.
- Purpose: characterize exchangeable cation pools influencing soil chemistry and nutrient availability.

### 3.2.5 Root biomass
- Data responsibility: Helen Glanville.
- Methods: 15 cm soil cores to assess total and fine roots; WinRhizo scanning for root traits; drying for biomass; in-growth root cores to measure root growth over a season; multiple sites included.
- Output: belowground biomass and growth dynamics to complement aboveground measurements.

### 3.2.6 Soil elements – TXRF
- Data responsibility:Helen Glanville.
- Method: TXRF (Bruker S2 PICOFOX) for total elemental analysis (multi-element suite) on 17 sites; sample prep includes drying and grinding; internal standards used; dataset supports broad soil chemical characterization.
- Limitations discussed in accompanying TXRF limitations file.

## Dataset structure
- Data files:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Common schema:
  - Site number (Table 1) identifying habitat and site details.
  - Habitat name and detailed habitat description.
  - Site name.
  - Ecosystem component (Plant, Soil, or Roots).
  - If Plant, species information; otherwise NA.
  - Plot number (1–4) and Replicate number (for non-co-located measurements).
  - Soil depth interval for Soil and Roots (NA for others).
- Data gaps indicated as NA; dataset structure supports cross-comparison and integration with models.

## Abbreviations
- The documentation includes a list of abbreviations for key measurements (e.g., Asat, BD, Jmax, N, P, SLA, Vcmax, etc.) and model references (e.g., JULES, NPP, LOI), facilitating consistent interpretation across datasets and analyses.