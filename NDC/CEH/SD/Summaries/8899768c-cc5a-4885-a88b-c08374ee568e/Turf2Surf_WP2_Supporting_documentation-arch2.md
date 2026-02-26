# Turf2Surf WP2 Supporting documentation for data

## Overview
- Focus: coupled nutrient cycling in terrestrial and freshwater ecosystems; links nitrogen and phosphorus dynamics to water quality, carbon exchange, and biodiversity.
- Aim within WP2: understand how N and P impacts influence land–atmosphere carbon exchange; integrate plant and soil nutrient data into the JULES model.
- Outputs: standardized data on plant productivity, photosynthesis, leaf/plant traits, soil properties, and soil chemistry to support environmental monitoring and policy evaluation.
- Data management: datasets stored and prepared for uploading to relevant portals; data processing and QA/QA checks described; scripts and methods referenced for reproducibility.

## Study Area: Conwy Catchment
- Location: North Wales, ~500 km2 with diverse landscapes and a strong climatic gradient.
- Ecological focus: ecological, biogeochemical, and hydrological processes from gene to landscape scale; emphasis on pressures affecting resources and ecosystem services.
- Habitats and stakeholders: blanket bog, montane moorland, conifer woodlands, grasslands, lakes/reservoirs, flood plains, salt marsh; engaged stakeholders include water industries, farmers, foresters, conservation groups, and local communities.

## Habitats and Sampling Sites
- 23 habitat/site entries (Site numbers and descriptions) with varying numbers of plots (1–4 per site) representing dominant plant communities.
- Sampling locations include blanket bog, heaths, upland and lowland woodlands, grasslands, hay meadows, agricultural plots, montane areas, and more.
- Data design supports comparative surveys and integration of diverse habitat types.

## Measurements and Data Processing

### 3.1.1 Aboveground Net Primary Productivity (NPP) and Standing Biomass
- Data responsible: Simon Smart.
- NPP: annual measurements (2013–2015) for dominant species across all sites; 4 plots per site; winter cutting with grazing-exclusion cages where relevant; life-cycle adjustments applied.
- Standing biomass: measured at 10 of 17 sites; herbaceous biomass in grasses/bogs; tree/shrub biomass via 200 m2 plots, tree cores, and DBH-based biomass calculations; leaf biomass included.
- Purpose: link plant productivity to soil processes and parameterize JULES (NPP data processing described in separate Turf2Surf WP2 NPP document).

### 3.1.2 Plant Photosynthesis Measures
- Data responsible: Lina Mercado.
- Parameters: Vcmax (max carboxylation at 25°C), Jmax (electron transport at 25°C), Asat (photosynthetic rate at saturating light/CO2).
- Methods: field measurements (Asat 2013–2014) with CIRAS-I, CO2 concentrations; 2014–2016 CO2 curves with Licor 6400; data modeled using De Kauwe package with Farquhar model; temperature corrections applied.
- Purpose: parameterize photosynthetic responses for incorporation into JULES.

### 3.1.3 Leaf Traits and Plant Community Traits
- Data responsible: Lina Mercado and Simon Smart.
- Traits: leaf N and P (%), leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover.
- Methods: LMA from 10 leaves per area; leaf area via ImageJ; N and P analyses with Vario and SEAL; SLA derived from LMA.
- Purpose: characterize resource-use strategies and support model parameterization.

### 3.2.1 General Soil Measures
- Data responsible: Helen Glanville.
- Sampling: intact soil cores to 1 m depth from 17 habitats; depth-stratified intervals; SWC and bulk density; LOI and LOI-C; pH and EC; total C and N via thermal oxidation (LECO).
- QA/QC and data processing described; link to WP2 objectives to integrate soil parameters into JULES.

### 3.2.2 Phosphorus (P) Fractions
- Data responsible: Helen Glanville.
- Fractions measured: Olsen P, Root-P (CaCl2 extractable P), Complex-P (citrate extractable P), Enzyme-P (phosphatase and phytase activity), Protons-P (1 M HCl soluble P).
- Methods: colorimetric Malachite Green for P; standard protocols and extractants described; data used to assess labile and recalcitrant P pools and potential root/microbial access.

### 3.2.3 Available Carbon and Nitrogen
- Data responsible: Helen Glanville.
- Method: 0.5 M K2SO4 extraction for available C and N; NO3 and NH4 analyses via colorimetric methods (vanadate, salicylate-nitroprusside, etc.); DOC and TDN measured at CEH Bangor using Thermalox and NDIR methods; QA/QC procedures noted.

### 3.2.4 Soil Available Cations (Ca, Na, K)
- Data responsible: Helen Glanville.
- Method: 0.5 M acetic acid extraction; measurement by flame photometry; standard curves used for concentration calculations.

### 3.2.5 Root Biomass
- Data responsible: Helen Glanville.
- Methods: 15 cm soil cores; separation of large vs. fine roots; WinRhizo for root morphology metrics; dry weight biomass calculated; in-growth root cores to assess root production over a growing season; detailed protocols for sampling and processing.

### 3.2.6 Soil Elements – TXRF
- Data responsible: Helen Glanville.
- Method: TXRF analysis (S2 PICOFOX) for 17 sites; sample prep includes grinding, suspension, and disc deposition; analyses conducted with internal standard for QA; limitations discussed in dedicated file.
- Purpose: broad elemental profiling to interpret biogeochemical context.

## Dataset Structure
- Five data files:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Key column semantics:
  - Site number (unique identifier) and Habitat/Description; Site name; Ecosystem Component (Plant, Soil, Roots); Species name for Plant components; Plot number; Replicate number.
  - For Soil and Roots: NA where not applicable; I-depth information provided for soil components.
  - Depth intervals apply to Soil and Roots; missing values marked NA.
- Purpose: standardized, multi-dimensional dataset to enable monitoring, cross-site comparisons, and integration with ecological models and policy evaluation.

## Data Management and Usage
- Data are intended for broader reuse by other research projects and policy monitoring efforts.
- WP2 aims to make datasets valuable beyond single-use analyses by enabling integration with other datasets and ensuring accessible underlying data behind outputs.
- Data responsible points of contact and references to processing scripts/modelling tools are provided to support reproducibility and reuse.

## Abbreviations (selected)
- Asat: photosynthetic rate at saturating light
- BD: bulk density
- Jmax: electron transport capacity
- NPP: aboveground net primary production
- N: nitrogen
- NH4: ammonium
- NO3: nitrate
- P: phosphorus
- SLA: specific leaf area
- LDMC: leaf dry matter content
- LMA: leaf mass per area
- Vcmax: maximum carboxylation rate
- SWC: soil water content
- TXRF: total X-ray fluorescence analysis
- JULES: Joint UK Land Environment Simulator (model)