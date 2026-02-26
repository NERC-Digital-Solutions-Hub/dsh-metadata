# Turf2Surf WP2 Supporting documentation for data

## Overview and purpose
- Focus of Turf2Surf: coupled nutrient cycling in terrestrial and freshwater ecosystems, linked to water quality, carbon sequestration, and biodiversity.
- WP2 objective: study nitrogen and phosphorus related impacts on carbon exchange between land and atmosphere, connecting plant and soil nutrients to ecosystem processes to inform modelling (e.g., JULES) and policy-relevant monitoring.

## Study area and sampling design
- Conwy catchment, North Wales (~500 km²): diverse landscapes, climate gradient, and a broad range of habitats (bogs, moors, woodlands, grasslands, lakes, flood plains, salt marshes).
- Sampling design: 17 soil habitats within the catchment (sites 1–10, 14–21; different ages of Llyn Serw bogs regrouped for soil analysis); up to 4 plots per habitat; multiple site-specific plots for aboveground and soil measurements.
- Map and site locations provide a spatial framework for sampling across habitat types and climatic gradients.

## Data collected and key variables

- 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
  - Annual NPP measured for dominant species at all sites (2013–2015); 4 plots per site to capture main species.
  - Winter vegetation clipping with grazing protection (cages) in grazed habitats; biomass dried and weighed; adjustments for plant life strategies.
  - Aboveground biomass measured at 10 of 17 sites (3–9 replicates per habitat); biomass estimation varies by habitat (grasses/bogs vs. woodland).

- 3.1.2 Plant photosynthesis measures
  - Parameters: Vcmax (maximum carboxylation rate), Jmax (electron transport capacity), Asat (photosynthesis at saturating light/CO2).
  - Field measurements (2013–2014) using CIRAS-I with CO2 sensors and LICOR 6400; 50–2000 ppm CO2 curves; data processed to fit Farquhar model; temperature-corrected to 25°C.
  - Modelling linkage to JULES; scripts and code for processing available (GitHub).

- 3.1.3 Leaf traits and plant community traits
  - Traits: leaf N and P (%), leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover.
  - LMA derived from leaves scanned and weighed; N and P analysed via standard lab methods.
  - Trait data contribute to plant–soil nutrient linkages in ecosystem process models.

- 3.2.1 General soil measures
  - Intact soil cores collected to 1 m depth across 17 habitats; cores split into depth intervals (0–15 cm to 90+ cm).
  - Measurements: soil water content (SWC), bulk density (BD), loss-on-ignition (LOI and LOI-C), pH, electrical conductivity (EC), total C and N.
  - QA/QC and data processing performed by a team; data prepared for integration with ecological models.

- 3.2.2 Phosphorus (P)
  - Olsen P (extractable P), Root-P, Complex-P, Enzyme-P, Complex-P, and Proton-P fractions measured to capture various P pools and bioavailability.
  - Extraction methods and colorimetric analyses (Malachite Green) described; approximates P dynamics linked to plant/microbial access.
  - Enzyme-P measured using phosphatase and phytase; detailed extraction and assay procedures provided.

- 3.2.3 Available carbon and nitrogen
  - Soil available C and N measured via 0.5 M K2SO4 extraction; NO3 and NH4 quantified by colorimetric/enzymatic methods.
  - DOC and TDN analysed at CEH Bangor using Thermalox instrument (high-temperature oxidation) with QA/QC batch structure described.

- 3.2.4 Soil available cations (Ca, Na, K)
  - 0.5 M acetic acid extraction; cations measured by flame photometry; data processed for unit conversions.

- 3.2.5 Root biomass
  - Total and fine root biomass measured at six sites; cores collected, roots washed, scanned with WinRhizo, and dried for biomass.
  - Root in-growth cores used to assess root growth over a growing season; methods for core design and collection described.

- 3.2.6 Soil elements – TXRF
  - Total elemental analysis (Al, Fe, Ca, K, Ti, S, etc.) by TXRF (S2 PICOFOX); samples prepared from 0–15 cm to 90+ cm depths.
  - Detailed sample prep, internal standards, and data processing; limitations discussed in a separate file.
  - Data emphasize holistic soil elemental composition for ecosystem nutrient assessments.

## Data structure and files
- Five data files:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Column structure overview:
  - Site number (Table 1 mapping)
  - Habitat and detailed habitat description
  - Site name
  - Ecosystem component (Plant, Soil, Roots)
  - Plant species (when applicable)
  - Plot number and Replicate number
  - Soil depth interval for Soil/Roots
- Missing data indicated as "NA"; dataset designed to support cross-component analyses and integration with ecosystem models.

## Data governance, openness, and accessibility
- Data and associated processing scripts (including modelling code) are accessible for reuse (GitHub repository references and methodological notes).
- Clear documentation of QA/QC procedures and dataset provenance to support transparency and reproducibility.
- TXRF limitations acknowledged in dedicated documentation.

## Relevance for monitoring frameworks
- Provides multi-scale, linked measurements across plants and soils that are essential for evaluating nutrient cycling, carbon fluxes, and ecosystem responses to management policies.
- Data are structured to feed into ecosystem models (e.g., JULES), aiding policy assessment and decision-making.
- Demonstrates comprehensive metadata and standardized procedures, enabling comparability across sites and time.

## Key considerations for monitoring and governance
- The dataset highlights the need for robust metadata, data sharing, and integration across disciplines to avoid data silos.
- Emphasizes methodological transparency and open code to support policy-relevant monitoring frameworks.
- Notes on limitations and QA/QC emphasize ongoing data governance requirements for credible environmental health monitoring.