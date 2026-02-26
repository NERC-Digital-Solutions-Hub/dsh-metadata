# Turf2Surf WP2 Supporting documentation for data

## Overview
- Document describes data outputs from Turf2Surf WP2, focusing on coupled nutrient cycling in terrestrial and freshwater ecosystems and its link to water quality, carbon exchange, and biodiversity.
- Temporal scope: data collected between 2013 and 2015; aims to relate plant and soil nutrients to ecosystem processes and to parameterize the JULES land-surface model.
- Project team: authors include Sabine Reinsch, Helen Glanville, Simon Smart, and others across CEH and partner universities.
- Data intended to support policy-relevant monitoring by providing standardized measures of productivity, plant function, soil chemistry, and nutrient pools.

## Study area and sampling design
- Location: Conwy catchment, North Wales (~500 km2), with diverse landscapes and climates (precipitation gradient; Snowdonia mountains; various soils and habitats).
- Habitats/sites: 17 soil/landscape habitats sampled across multiple site names (e.g., Nant-y-Brwyn, Llyn Serw, Capel Curig, Glasfwy, Bery’ls wood, Red Kite Woods, Ingleborough NNR, Conwy arable, etc.).
- Sampling structure: plots per site (commonly 3–4 plots per habitat) with replication; soils sampled to 1 m depth; aboveground and belowground components collected across habitats.
- Output focus: baseline data and site-specific descriptors to enable cross-site comparisons and integration into ecosystem process models.

## Key measures and data types

- 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
  - Annual NPP measured for dominant species (2013–2015) with protected plots in winter to prevent grazing where applicable.
  - Aboveground biomass quantified across habitats; woody vegetation sampled with tree cores; biomass calculations scaled to a per m2 basis.
  - Purpose: link plant productivity to nutrient inputs and to model outputs in JULES.

- 3.1.2 Plant photosynthesis measures
  - Variables: Vcmax (max carboxylation rate at 25°C), Jmax (electron transport capacity at 25°C), Asat (photosynthetic rate at saturating light/CO2).
  - Field and lab measurements using CIRAS-I, LICOR equipment, and development of CO2-response curves; temperature corrections to 25°C using established functions.
  - Data processing via a published R-based workflow; linked to JULES parameterization.

- 3.1.3 Leaf traits and plant community traits
  - Metrics: leaf N and P (%), LDMC, SLA, LMA, canopy height, bryophyte cover.
  - LMA and related traits derived from leaf measurements and ImageJ analysis; N and P analyses conducted with standard lab methods.
  - Purpose: derive plant functional traits to inform community composition and ecosystem processes in models.

- 3.2.1 General soil measures
  - Field collection: intact soil cores to 1 m depth from 17 habitats; samples segmented by depth (0–15, 15–30, …, 90+ cm).
  - Measured: soil water content, bulk density, LOI and LOI-C, pH, EC, total C and N.
  - QA/QC and multi-analytical methods used to ensure data quality and comparability across habitats.

- 3.2.2 Phosphorus
  - Phosphorus fractions assessed via Olsen P, Root-P, Complex-P, and Enzyme-P; additional data on available P using multiple extraction schemes (Malachite Green colorimetry).
  - Methods reflect different P pools: readily available, root-accessible, carbonate-bound, and enzyme-labile pools.
  - Data intended to illuminate P availability and turnover in the rhizosphere and soil biogeochemistry.

- 3.2.3 Available carbon and nitrogen
  - Soil extracts for available C and N using 0.5 M K2SO4; measurement of DOC and TDN with QA/QC protocols.
  - Processes describe extraction, storage, and analysis workflows.

- 3.2.4 Soil available cations
  - Extraction with 0.5 M acetic acid; Ca, Na, K measured with flame photometry.
  - Aimed at understanding base cations associated with soil fertility and their role in nutrient cycling.

- 3.2.5 Root biomass
  - Standing root biomass: coarse (<2 mm) and fine roots separated; roots scanned with WinRhizo for morphological parameters; dry weight determined.
  - In-growth cores: roots grown in situ for ~3–4 months to assess root production and colonization.
  - Data support analyses of belowground carbon storage and root dynamics relevant to nutrient uptake.

- 3.2.6 Soil elements (TXRF)
  - Total X-Ray Fluorescence (TXRF) for broad elemental profiling (Al, Fe, Ca, K, etc.) across all sites and depths.
  - Sample prep includes grinding, dispersion on discs, and internal standards; used to characterize multielement soil chemistry.

- Data integration goal
  - Across measures, data are intended to be incorporated into the JULES model to improve representations of plant-soil nutrient interactions and carbon cycling.

## Methods and data processing highlights

- Data responsibility and provenance
  - Primary data managers and analysts are named for each data type (e.g., Simon Smart for NPP; Lina Mercado for photosynthesis; Helen Glanville for soils and TXRF).
- Modeling linkage
  - WP2 aims to embed measured parameters into JULES via Turf2Surf data processing workflows and scripts (e.g., photosynthesis modeling workflow, Farquhar-based fits, temperature corrections).
- Documentation and reproducibility
  - Specific methodological references provided for photosynthesis modeling and P analyses; scripts and code referenced (e.g., GitHub repository for photosynthesis model fitting).
- Data quality controls
  - QA/QC procedures indicated for C, N, and other analyses; calibration ranges and internal standards described for TXRF and colorimetric assays.

## Dataset structure and data fields

- Five data files
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Common metadata framework
  - Column A: Site number (referenced to Table 1)
  - Column B–C: Habitat and detailed habitat description
  - Column D: Site name
  - Column E: Ecosystem component (Plant, Soil, Roots)
  - Column F: For Plant components, specific species; otherwise NA
  - Column G–H: Plot and Replicate numbers
  - Column I: Soil depth interval (for Soil and Roots components)
- Data considerations
  - Missing values indicated as NA
  - Replicates and plot details allow site-level comparisons and alignment with field sampling constraints

## Governance, sharing, and data notes

- The documentation emphasizes openness and data sharing as part of the project’s data governance, including clear metadata and standardized datasets to support transparency and reuse.
- Methods note potential limitations (e.g., TXRF limitations documented in a separate file) and the need for careful interpretation when integrating across measures.
- Data are designed to be used for policy-relevant monitoring and to support model-based extrapolations of nutrient cycling and carbon dynamics at landscape scales.

## Practical implications for monitoring frameworks

- Provides a comprehensive, multi-component data suite (biomass, productivity, leaf and plant traits, soil chemistry, available nutrients, root dynamics, and TXRF elemental data) suitable for informing environmental health monitoring and policy evaluation.
- The integrated design supports linking field measurements to process-based models (JULES), enabling scenario testing and policy impact assessments on nutrient cycling, water quality, carbon fluxes, and biodiversity.
- Site- and habitat-level granularity, with standardized depth intervals and replication, enhances comparability over time and across landscapes.
- Potential considerations for policymakers
  - Ensure access to metadata and data governance details to facilitate reuse.
  - Leverage model-linked parameters for scenario analyses and monitoring frameworks.
  - Be mindful of methodological limitations and QA/QC requirements when aggregating data across sites or years.