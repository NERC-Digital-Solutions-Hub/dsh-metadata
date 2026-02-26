# Turf2Surf WP2 Supporting documentation for data

## Overview and aims
- Focuses on coupled nutrient cycling in terrestrial and freshwater ecosystems, linked to water quality, carbon sequestration and biodiversity.
- WP2 studies nitrogen and phosphorus related impacts on carbon exchange between land and atmosphere; data intended to support integration into ecological models (e.g., JULES) and cross-site analyses.

## Project details
- Members: Bridget Emmett, Davey Jones, Simon Smart, Lina Mercado, Helen Glanville, Maria C Blanes, Harry Harmens, Sabine Reinsch.
- Authors: Sabine Reinsch (corresponding), Helen Glanville, Simon Smart.
- Version dates: 01/06/2016; 25/08/2016; 04/11/2016.
- Data responsibility: specific individuals lead data collection, processing and QA for plant biomass, physiology, leaf traits, soils, P fractions, C/N, cations, roots and TXRF.

## Study area: Conwy catchment
- Location: North Wales, ~500 km2, diverse landscapes and climatic gradient.
- Purpose: establish a baseline of consistent data across habitats to understand ecological, biogeochemical and hydrological processes and pressures on resources.
- Habitats: blanket bog, moorland, conifer woodlands, grasslands, lakes/reservoirs, flood plains, salt marshes; broad stakeholder involvement.

## Habitats and sampling
- Table 1 documents 23 sites with varied habitats (e.g., blanket bog, acid grassland, conifer woodland, mixed deciduous woodland, oakwood, hay meadows, arable, silage, purple moor pastures, montane sites).
- Sampling design includes multiple plots per habitat (up to 4 plots per site) across a diversity of dominant plant communities.

## Measurements and data processing

### 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
- Data responsible: Simon Smart.
- NPP: measured annually (2013–2015) for dominant species at all sites; four plots per site; winter clipping and grazing protection where applicable; life-history adjustments to NPP.
- Standing biomass: measured at 10 of 17 sites (3–9 replicates per habitat); methods differ by habitat (herbaceous biomass cut in grassy/bog habitats; tree cores and wood density for woodland plots; leaf biomass included).

### 3.1.2 Plant photosynthesis measures
- Data responsible: Lina Mercado.
- Parameters: Asat, Vcmax, Jmax measured for dominant species (Asat field measurements 2013–2014; Vcmax/Jmax via A-Ci curves using LICOR 6400 and CIRAS-I setups).
- Temperature corrections to 25°C; model fitting with Farquhar framework (code available: GitHub mdekauwe/FitFarquharModel).
- Purpose: link photosynthesis to soil/plant nutrients and parameterize JULES models.

### 3.1.3 Leaf traits and plant community traits
- Data responsible: Lina Mercado, Simon Smart.
- Traits: leaf N, leaf P, LDMC, SLA, LMA, canopy height, bryophyte cover.
- Methods: Leaf sampling 2013–2014; LMA determined from 10 leaves per site, area via ImageJ, dry weight after 65°C drying; N and P analyses by standard lab methods.
- Purpose: derive trait-based parameters to feed into ecosystem models (JULES) and relate to nutrient status.

### 3.2.1 General soil measures
- Data responsible: Helen Glanville.
- Sampling: intact cores to 1 m depth across 17 habitats (3 cores per habitat; depth intervals 0–15 cm to 90+ cm).
- Measurements: soil water content (SWC), bulk density (BD), loss-on-ignition (LOI and LOI-C), pH, electrical conductivity (EC), total C and N (via thermal oxidation).
- QA/QC: multi-person, multi-method approach; detailed processing and calibration notes available.

### 3.2.2 Phosphorus
- Data responsible: Helen Glanville.
- Fractionation scheme: Olsen P, Root-P, Complex-P, Enzyme-P, Proton-P (methods emulate plant/microbial P access and sorption dynamics).
- Analysis: colorimetric assays (Malachite Green) after various extractions; detailed reagent steps provided.
- Purpose: capture multiple P pools relevant to plant uptake and soil chemistry.

### 3.2.3 Available carbon and nitrogen
- Data responsible: Helen Glanville, others.
- Method: 0.5 M K2SO4 extraction for available C and N; NO3 via vanadate method; NH4 via salicylate-nitroprusside method; DOC/TDN analyses by CEH Bangor (Thermalox analyzer for C and TDN).

### 3.2.4 Soil available cations (Ca, Na, K)
- Data responsible: Helen Glanville.
- Method: extraction with 0.5 M acetic acid; measurement by flame photometry; QA/QC and data handling as above.

### 3.2.5 Root biomass
- Data responsible: Helen Glanville, others.
- Standing root biomass: 15 cm cores; root washing, separation into >2 mm and <2 mm fractions; root scanning with WinRhizo to obtain length/diameter metrics; dry weight for biomass.
- In-growth roots: 63 mm tubes with 15 cm length; planted in ground for 3–4 months; roots processed similarly to standing biomass.
- Purpose: quantify belowground allocation and root dynamics for ecosystem modeling.

### 3.2.6 Soil elements – TXRF
- Data responsible: Helen Glanville and collaborators.
- Method: TXRF (S2 PICOFOX) on 17 sites; sample prep includes grinding, drying, suspension with TritonX and internal standards; disc-based microanalysis with gain correction.
- Scope: broad elemental suite (Al, Fe, Ca, K, Ti, S, Ba, Mn, P, Sr, Zr, Cl, V, Rb, Zn, Cr, Nd, La, Cu, Y, Ni, Pb, Ga, Nb, Th, Co, Sc, As, Cs, U, Sn, Ge, I, Br, Sb, Se, Cd, Hg).
- Limitations: documented in Turf2Surf_WP2_TXRF_Limitations_Glanville.rft.

## Dataset structure
- Five data files:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Key columns:
  - Site number; Habitat and detailed Habitat description; Site name; Ecosystem Component (Plant, Soil, Roots).
  - For Plants: species information; Plot number; Replicate number.
  - For Soil/Roots: soil depth interval.
- Data handling:
  - Missing values indicated as NA; some depths/reps restricted by field conditions.
- Purpose: enable cross-component analysis (plant and soil) and integration with models like JULES; supports data reuse and self-service analysis.

## Data management and usage
- Clear provenance: data responsibility assigned to named researchers per measurement type; multiple collaborators ensure QA and cross-checks.
- Model integration: WP2 data linked to JULES parameterization efforts; dataset and scripts available for reproducible processing and model fitting (e.g., photosynthesis model code).
- Accessibility: structured dataset with consistent site/habitat coding to facilitate cross-site comparisons and potential dashboards or data products.

## Access, references and notes
- Code and methodological references provided for photosynthesis modeling (Farquhar et al. 1980; De Pury & Farquhar 1997; Medlyn et al. 2002; Kattge & Knorr 2007).
- TXRF limitations documented in a dedicated RFT file.
- Contact points for data responsibility listed within each section (e.g., ssma@ceh.ac.uk for NPP; L.Mercado@exeter.ac.uk for photosynthesis; h.c.glanville@bangor.ac.uk for soil measurements).
- Data designed to support broader data use across topics and to aid integration into policy-relevant and resource-management contexts.