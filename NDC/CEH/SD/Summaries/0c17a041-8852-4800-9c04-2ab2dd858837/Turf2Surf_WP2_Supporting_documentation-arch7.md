# Turf2Surf WP2 Supporting documentation for data

## Overview
- Turf2Surf WP2 investigates coupled nutrient cycling in terrestrial and freshwater ecosystems and links nitrogen and phosphorus impacts to carbon exchange between land and atmosphere.
- The document describes data collection, processing and dataset structure for Conwy catchment study (North Wales), focusing on above- and below-ground processes, plant traits, soils, and phosphorus and carbon pools to inform the JULES model.

## Study area and scope
- Conwy catchment in North Wales (~500 km2) with diverse landscapes and climatic gradient (precipitation ~500 mm to >1000 mm).
- Habitats include blanket bog, montane/moorland, conifer and broadleaf woodlands, grasslands, lakes/reservoirs, flood plains, and salt marshes.
- Stakeholders across water industries, farming, forestry, tourism and conservation.
- Aims to understand pressures on natural resources and ecosystem services from gene to landscape scale.

## Habitats and sampling sites
- 17 primary sites across the catchment (covering bogs, grasslands, woodlands, montane areas, arable/paddocks, etc.). Each site contains multiple plots to represent dominant plant species.
- Site descriptions include longevity and age classes for habitats such as Llyn Serw bogs (varying ages), Capel Curig bog/grassland, Ingleborough NNR limestone habitats, Red Kite Woods, Montane areas, and others.
- Table 1 (Habitat and location details) documents unique site numbers, number of plots, and dominant species where possible.

## Key datasets and measurements

### 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
- Annual NPP measured on dominant species at all sites (2013–2015) with four plots per site.
- Winter vegetation clipping and grazing exclusion (where applicable) to standardize growth.
- Aboveground standing biomass measured at 10 of 17 sites (3–9 replicates per habitat) using:
  - Grassy/bog sites: harvest in 1 m x 1 m quadrats, dry and weigh.
  - Woodland: two 200 m2 plots per site with tree cores to estimate biomass using allometric formulas.
- NPP and data processing linked to Turf2Surf WP2, with detailed methodology in Turf2Surf_WP2_NPP_Smart.rft.
- Data contributed by Simon Smart; NPP processing by Simon Smart; code and methods available via project documentation.

### 3.1.2 Plant photosynthesis measures
- Parameters: Asat (photosynthetic rate at saturating irradiance/CO2), Vcmax (maximum carboxylation rate), Jmax (electron transport capacity) at 25°C.
- Measurements on all dominant species at most sites.
- Methods evolved over years, from CIRAS-I with CO2 chambers to LICOR 6400 with 50–2000 ppm CO2.
- Vcmax and Jmax curve-fitting via Farquhar-based models and temperature corrections; analyses executed in scripts (e.g., mdekauwe/FitFarquharModel) to standardize to 25°C.
- Data processing and measurement responsibility: Lina Mercado, Simon Smart; Vcmax/Jmax calculations by L. Mercado.
- Purpose: parameterize ecosystem processes for incorporation into the JULES model.

### 3.1.3 Leaf traits and plant community traits
- Traits measured at most sites in 2013–2014:
  - Leaf nitrogen (N) and phosphorus (P) percentages
  - Leaf dry matter content (LDMC)
  - Specific leaf area (SLA) and leaf mass per area (LMA)
  - Canopy height and bryophyte cover
- LMA measured on 10 leaves per sampled area; leaf area calculated with ImageJ; leaves dried to determine mass for LMA; SLA derived as inverse of LMA.
- N and P analyzed via standard lab methods (vegetation digestion, colorimetric analyses).
- Data processing and leaf trait measurements linked to JULES parameters.
- Responsible: Lina Mercado and Simon Smart; analysis and processing collaborators.

### 3.2.1 General soil measures
- Intact soil cores collected in spring 2014 from 17 habitats to 1 m depth; cores split into depth intervals (0–15, 15–30, 30–45, 45–60, 60–75, 75–90, 90+ cm).
- Measurements include:
  - Soil water content (SWC) via fresh/dry weights
  - Bulk density (BD) from dried samples
  - Loss on ignition (LOI) and LOI-C to estimate organic matter and carbon
  - pH and electrical conductivity (EC)
  - Total carbon (C_tot) and total nitrogen (N_tot) by thermal oxidation (Elementar Vario Cube Select)
- Data processing and QA/QC by a team including Helen Glanville and colleagues.
- Purpose: establish baseline soil properties across habitats for ecosystem modelling and GIS mapping.

### 3.2.2 Phosphorus
- Olsen P, root-available P, complex-P and enzyme-P fractions measured to capture multiple P pools.
- Methods include:
  - Olsen P extraction with 0.5 M NaHCO3 (pH 8.5) and colorimetric detection using Malachite Green
  - Root-P measured with 0.01 M CaCl2 extraction and colorimetric detection
  - Complex-P via 10 mM citrate extraction with Malachite Green detection
  - Enzyme-P using enzyme extracts (phosphatase and phytase) with Malachite Green detection
  - Proton-P via 1 M HCl extraction and colorimetric detection
- All P fractions expressed in comparable units for cross-site comparison.
- Data processing and analysis led by Helen Glanville and team.

### 3.2.3 Available carbon and nitrogen
- Soil available C and N measured after extraction with 0.5 M K2SO4 (1:5 soil:solution).
- Nitrate (NO3) analyzed by vanadate method; Ammonium (NH4) by salicylate-nitroprusside and hypochlorite reagent.
- DOC and TDN measured at CEH Bangor using appropriate instrumentation (Total carbon via catalytic oxidation; Total Dissolved Nitrogen similarly measured).
- Detailed QA/QC and standard curve procedures noted.

### 3.2.4 Soil available cations (Ca, Na, K)
- Extracted with 0.5 M acetic acid; cations quantified with flame photometry.
- Data processing and analysis coordinated to link soil chemistry with plant-soil interactions in JULES.

### 3.2.5 Root biomass
- Total and fine root biomass measured at a subset of sites (Capel Curig, Nant-yBrwyn, Red Kite Woods, Alan Davies farm sites, etc.).
- 15 cm soil cores split into 0–5, 5–10, 10–15 cm; roots cleaned, scanned with WinRhizo (length, diameters, branching) and dried for biomass.
- In-growth cores used to study root growth over a growing season; cores installed and later collected for analysis.
- Data handling and root trait analysis conducted by Helen Glanville and collaborators; in-growth core design by Glanville and Mesa.

### 3.2.6 Soil elements - TXRF
- Total elemental analysis (Al, Fe, Ca, K, Ti, S, Ba, Mn, P, Sr, Zr, Cl, V, Rb, Zn, Cr, Nd, La, Cu, Y, Ni, Pb, Ga, Nb, Th, Co, Sc, As, Cs, U, Sn, Ge, I, Br, Sb, Se, Cd, Hg) via TXRF (Bruker S2 PICOFOX).
- 17 sites sampled; samples prepared as ground powder, suspended in TritonX, and applied to silicon discs for TXRF.
- Limitations discussed in Turf2Surf_WP2_TXRF_Limitations_Glanville.rft.
- Data management and analysis led by Glanville, with laboratory work by Havelange, Chesworth, etc.

## Dataset structure and data fields
- The project provides five data files:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw_data.csv
- Common fields include:
  - Site number (unique site identifier)
  - Habitat and detailed habitat description
  - Site name
  - Ecosystem component (Plant, Soil, Roots)
  - For Plant components, species information; otherwise NA
  - Plot number (1–4) and Replicate number
  - For Soil and Roots, soil depth interval (0–15, 15–30, etc.)
- Missing values are indicated as NA.
- The structure is designed to support GIS-style mapping and integration with the JULES model, enabling spatially explicit visualization of NPP, biomass, leaf traits, soil properties, P fractions, DOC/TDN, available cations, root metrics, and TXRF elemental data.

## Data provenance, processing, and integration
- Data responsibilities assigned to project members (e.g., Simon Smart, Lina Mercado, Helen Glanville, Jo Glanville, MC Blanes).
- Methodologies and data processing routines are described with references to separate linked documents and public code repositories (e.g., Turf2Surf_WP2_NPP_Smart.rft; FitFarquharModel scripts; various lab protocols).
- The dataset is intended to feed into JULES and to support spatial analyses of nutrient cycling, carbon exchange, and ecosystem processes across habitat types within the Conwy catchment.
- Version dates listed: 01/06/2016; 25/08/2016; 04/11/2016.

## How GIS specialists can use this data
- Create habitat- and site-level layers of NPP, biomass, and leaf/plant traits, with depth-resolved soil properties as separate attributes or rasters.
- Map soil property gradients by depth (0–15 cm, 15–30 cm, etc.) across habitats to visualize vertical profiles.
- Visualize P pools and soil nutrients (Olsen P, Root-P, Complex-P, Enzyme-P, Proton-P, DOC/TDN, NO3-, NH4+) alongside plant traits to explore nutrient dynamics spatially.
- Integrate root biomass and in-growth data to assess belowground productivity patterns and soil resource use.
- Overlay TXRF elemental data to evaluate multielement soil chemistry across sites and depths.
- Use the site/habitat structure to summarize data for policy or stakeholder-focused map products and to support model parameterization for JULES-based spatial analyses.
- Access and reuse data through the five CSV files, with documentation on field methods, depth intervals, and replicate structure to ensure reproducibility and correct interpretation in GIS workflows.