# Turf2Surf WP2 Supporting documentation for data

- The Turf2Surf project investigates nutrient cycling in terrestrial and freshwater ecosystems and how nitrogen and phosphorus impacts carbon exchange between land and atmosphere. WP2 covers nitrogen and phosphorus influences on carbon exchange, linking plant and soil nutrients to ecosystem processes and aiming to feed into the JULES model.

## Overview of the study area

- Location: Conwy catchment, North Wales (~500 km²) with diverse landscapes and a climate gradient (precipitation 500–1064 mm, mountains to the west).
- Habitats: Wide range including blanket bogs, montane/moorland, conifer plantations, diverse grasslands, lakes/reservoirs, flood plains, and salt marshes.
- Stakeholders: Water industries, shell fisheries, farmers/foresters, tourism, conservation groups and local communities.
- Data purpose: Establish baseline, process-level understanding of ecological, biogeochemical and hydrological processes from gene to landscape scale, focusing on pressures influencing natural resources and benefits.

## Habitats and sampling sites

- 17 habitats sampled across the Conwy catchment with 23 site descriptors (Table 1), representing diverse vegetation types and ages (e.g., blanket bogs, heaths, conifer woodland, broadleaved woodland, improved and semi-improved grasslands, hay meadows, arable land).
- Plot structure: Typically 3–4 plots per habitat per site; replicates used to represent dominant species where field plots could not be co-located with measurement plots.
- Sampling sites include locations such as Nant-y-Brwyn, Llyn Serw, Capel Curig, Glasgwm, Bery’ls Wood, Coed Dolgarrog NNR, Red Kite Woods, Ingleborough NNR, Hiraethlynn, Nant-y-coed, Alun Davies farms, Migneint, Conwy arable fields, Purple Moor, Montane sites, etc.

## Data streams and measurement methods

- 3.1.1 Aboveground net primary production (NPP) and standing biomass
  - Annual NPP measured for all dominant species at all sites (2013–2015) using 4 plots per habitat; winter clipping and grazing exclusion via wire cages where appropriate.
  - Aboveground biomass measured at 10 of 17 sites (3–9 replicates per habitat); biomass from grasses/bogs by clipping in 1 m x 1 m quadrats, woodland biomass via random 200 m² plots with tree cores and leaf biomass.
  - NPP data linked to plant life strategies and used to inform JULES ecosystem modeling.

- 3.1.2 Plant photosynthesis measures
  - Parameters measured: Asat, Vcmax, Jmax (at 25°C) for dominant species.
  - Instruments: CIRAS-I with leaf cuvettes, and LICOR 6400 for A–Ci curves; CO2 concentrations from 50–2000 ppm, light ~1500 μmol m⁻² s⁻¹, leaf temp ~20°C.
  - Data processing uses a Farquhar-model-based fitting routine; temperature corrections applied to 25°C.
  - Data and processing linked to JULES parameterization; scripts available via GitHub.

- 3.1.3 Leaf traits and plant community traits
  - Traits measured: leaf N and P (%), leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover.
  - LMA/SLA calculated from sampled leaves; leaf N and P analyzed with standard laboratory methods.
  - Data incorporated into JULES parameterizations.

- 3.2.1 General soil measures
  - Intact soil cores collected spring 2014 from 17 habitats (down to 1 m; depth intervals 0–15, 15–30, 30–45, 45–60, 60–75, 75–90, 90+ cm).
  - Measurements: soil water content (SWC), bulk density (BD), loss on ignition (LOI and LOI-C), pH, EC, total C and N.
  - QA/QC and data processing conducted by team members; samples processed for C and N with elemental analyzer.

- 3.2.2 Phosphorus
  - Olsen P (0.5 M NaHCO3, pH 8.5) by colorimetry (Malachite Green method).
  - Root-P measured with 0.01 M CaCl2 extraction and colorimetric assay.
  - Complex-P (10 mM citrate extractable P), Enzyme-P (phosphatase and phytase), and Proton-P (1 M HCl extraction) measured with Malachite Green colorimetry.
  - Procedures mirror detailed literature methods and are designed to reflect P pools accessible to roots and microbial activity.

- 3.2.3 Available carbon and nitrogen
  - Soil available C and N extracted with 0.5 M K2SO4; analyses for DOC and TDN (glucose/creatinine-based standards and QA controls).
  - Methods implemented to capture readily available soil C and N pools.

- 3.2.4 Soil available cations (Ca, Na, K)
  - Extraction with 0.5 M acetic acid; cations measured by flame photometry.
  - Data processed to yield available Ca, Na, and K per soil sample.

- 3.2.5 Root biomass
  - Standing and fine root biomass measured at six sites using 15 cm soil cores (0–5, 5–10, 10–15 cm depths).
  - Roots scanned with WinRhizo for length/diameter metrics; dried and weighed for biomass.
  - In-growth cores used to quantify root production over a season.

- 3.2.6 Soil elements – TXRF
  - Total elemental analysis (Al, Fe, Ca, K, Ti, S, Ba, Mn, P, Sr, Zr, Cl, V, Rb, Zn, Cr, Nd, La, Cu, Y, Ni, Pb, Ga, Nb, Th, Co, Sc, As, Cs, U, Sn, Ge, I, Br, Sb, Se, Cd, Hg) using TXRF on 17 sites.
  - Sample prep included grinding to fine powder, internal standards, and disc deposition for TXRF analysis.
  - Limitations of TXRF discussed in dedicated notes; data linked to broader nutrient analyses and JULES integration.

## Dataset structure and data products

- Data files (five CSVs):
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Common schema:
  - Column A: Site number (as in Table 1)
  - Column B–C: Habitat and detailed habitat description
  - Column D: Site name
  - Column E: Ecosystem component (Plant, Soil, or Roots)
  - Column F: For Plant components, specific plant species; for Soil/Roots, NA
  - Columns G–H: Plot number and Replicate number
  - Column I: Soil depth interval for Soil and Roots
- Data quality notes:
  - Missing values indicated as NA due to restricted depths, limited replicates, or outliers.
  - Data are designed to support cross-study analyses and integration with process models (e.g., JULES).

## Data provenance, quality, and usage context

- Responsible individuals and teams per data stream (e.g., NPP and biomass: Simon Smart; photosynthesis: Lina Mercado; leaf traits: Lina Mercado & Simon Smart; soils and P fractions: Helen Glanville et al.; TXRF: Glanville et al.).
- Data processing emphasizes standardised methods, QA/QC, and alignment with nutrient-cycling and carbon-exchange objectives.
- Links to modeling and processing workflows:
  - Plant photosynthesis modeling uses Farquhar-based fits; temperature corrections to 25°C.
  - NPP and leaf/soil trait data feed into JULES parameterization; relevant scripts are available (e.g., GitHub repository for fit functions).
- Documentation notes:
  - Detailed protocols and methodological references included (standard methods for NPP, P fractions, DOC/TDN, NO3, NH4, cations, TXRF) and links to modeling literature.

## Access, reuse, and practical considerations for analysts

- Dataset intended for consistent monitoring, enabling time-series scrutiny of environmental health and policy performance, with provision for combining with other environmental datasets.
- Data are structured to facilitate portal deposition and sharing, with explicit metadata about sites, habitats, and sampling design.
- Useful for cross-site comparisons, habitat-based nutrient dynamics, and integration with ecosystem models to assess policy scenarios and mitigation strategies.
- Considerations:
  - Some habitat-depth or replicate limits may introduce gaps; NA values indicate missing data that analysts should account for in analyses.
  - TXRF data come with methodological caveats documented in the accompanying notes.

## Authors and version

- Project members: Bridget Emmett, Davey Jones, Simon Smart, Lina Mercado, Helen Glanville, Maria C Blanes, Harry Harmens, Sabine Reinsch
- Authors: Sabine Reinsch (corresponding author), Helen Glanville, Simon Smart
- Version history: 01/06/2016; 25/08/2016; 04/11/2016

- Data credits and contact:
  - Primary data responsibility and contact details provided for each data stream (e.g., NPP: Simon Smart; photosynthesis: Lina Mercado; leaf traits: Lina Mercado & Simon Smart).