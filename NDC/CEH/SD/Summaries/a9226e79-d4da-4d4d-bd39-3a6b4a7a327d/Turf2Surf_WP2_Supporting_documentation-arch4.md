# Turf2Surf WP2 Supporting documentation for data

## Overview
- Turf2Surf project examines coupled nutrient cycling in terrestrial and freshwater ecosystems, focusing on nitrogen and phosphorus impacts on carbon exchange between land and atmosphere.
- WP2 studies links between plant and soil nutrients and above/belowground processes to inform ecosystem models (e.g., JULES).
- Data collected across the Conwy catchment (North Wales) between 2013 and 2015 for NPP, plant traits, soil chemistry, and related measurements; linked to ecosystem processes and modeling.

## Study area and collaborators
- Conwy catchment (≈500 km2) in North Wales with diverse habitats and a range of stakeholders (water utilities, agriculture, forestry, conservation, communities).
- Site distribution covers 17 habitats across 1 m depth soil cores and aboveground plots (sampling across varied climatic and soil conditions).
- Project team includes researchers from CEH, Bangor University, Exeter University; corresponding author Sabine Reinsch.

## Data content and focus areas
- 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
  - Annual NPP measured for dominant species at all sites (2013–2015) with multi-plot representation.
  - Aboveground biomass measured at 10 of 17 sites (grasses/bogs via clipping; woodland via tree cores and leaf biomass).
  - NPP adjustments account for plant life strategies and grazing exclusion where applicable.
- 3.1.2 Plant photosynthesis measures
  - Vcmax, Jmax, Asat for dominant species; field measurements using CIRAS-I and LICOR equipment; CO2 response curves (A-Ci) analyzed with Farquhar model and temperature corrections.
  - Data processing scripts reference: mdekauwe/FitFarquharModel (GitHub).
- 3.1.3 Leaf traits and plant community traits
  - Leaf N and P, leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover.
  - LMA derived from leaf scans and drying; N and P analyzed with standard lab methods.
- 3.2.1 General soil measures
  - Intact soil cores (17 habitats) down to 1 m; depth intervals to 90+ cm; analyses include SWC, bulk density, LOI and LOI-C, pH, EC, total C and N.
- 3.2.2 Phosphorus (P) fractions
  - Olsen P, Root-P (soluble/inorganic), Complex-P (10 mM citrate extractable P), Enzyme-P (phosphatase and phytase activity), and Proton-P (1 M HCl extraction).
  - P quantified by Malachite Green colorimetry; detailed extraction and analysis protocols provided.
- 3.2.3 Available carbon and nitrogen
  - Soil available C and N via 0.5 M K2SO4 extraction; NO3 and NH4 via colorimetric assays; DOC and TDN via CEH Bangor protocols (Thermalox/NDIR for DOC; TDN analogous).
- 3.2.4 Soil available cations
  - Ca, Na, K extracted with 0.5 M acetic acid and measured by flame photometry.
- 3.2.5 Root biomass
  - Total and fine root biomass across multiple sites; 15 cm soil cores with root washing, scanning (WinRhizo) for morphology, then drying for biomass; includes in-growth root cores to assess root growth.
- 3.2.6 Soil elements (TXRF)
  - Total elemental analysis (Al, Fe, Ca, K, Ti, S, Ba, Mn, P, Sr, Zr, Cl, V, Rb, Zn, Cr, Nd, La, Cu, Y, Ni, Pb, Ga, Nb, Th, Co, Sc, As, Cs, U, Sn, Ge, I, Br, Sb, Se, Cd, Hg) by TXRF on 17 sites; sample prep includes grinding and TXRF analysis; limitations discussed in dedicated TXRF document.

## Data management and structure
- Five data files are provided:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw_data.csv
- Key metadata in data files:
  - Column A: Site number (as in Table 1)
  - Columns B–C: Habitat and detailed habitat description
  - Column D: Site name
  - Column E: Ecosystem component (Plant, Soil, Roots) with Plant specifying species in Column F
  - Columns G–H: Plot number (1–4) and Replicate number (for co-located vs. representative plots)
  - Column I: Soil depth interval (for Soil and Roots)
- Missing data indicated as NA due to depth limitations, replicate counts, or outliers.
- Table 1 (habitats) provides site-specific plot counts and descriptions (e.g., Nant-y-Brwyn bog, Capel Curig bog/grassland, Ingleborough NNR habitats, etc.).
- Dataset designed to support integration with the JULES model by providing plant and soil parameters linked to aboveground and belowground processes.

## Data processing, provenance, and usage notes
- Data responsibilities credited to specific researchers (e.g., Simon Smart for NPP, Lina Mercado for photosynthesis measures, Helen Glanville for soils and TXRF, etc.).
- NPP, photosynthesis, and leaf trait data include references to analytical methods and, for some, scripts or models used (e.g., Farquhar model, De Kauwe’s FitFarquharModel; GitHub link provided for photosynthesis fitting).
- WP2 aims to translate field measurements into parameters for ecosystem models (e.g., JULES) and to link nutrient pools with process rates.
- TXRF section notes that there are limitations to the TXRF method, with further details in Turf2Surf_WP2_TXRF_Limitations_Glanville.rft.

## Version and authorship
- Version dates: 01/06/2016; 25/08/2016; 04/11/2016.
- Authors and project members include Sabine Reinsch (corresponding author), Helen Glanville, Simon Smart, Bridget Emmett, Lina Mercado, and others from CEH and partner institutions.

## Practical implications for Data Leaders
- Comprehensive, vertically integrated data across plant and soil compartments with explicit linkage to ecosystem modeling (JULES).
- Rich metadata in structured data files enhances discoverability and reuse across projects and networks.
- Clear documentation of sampling design, depth intervals, replicates, and site-level descriptions supports data quality assessment and cross-site comparisons.
- Availability of methodological references and scripts supports reproducibility and potential meta-analyses.
- A dedicated limitations document for TXRF highlights attention to data quality and method constraints, aligning with governance and data quality standards.