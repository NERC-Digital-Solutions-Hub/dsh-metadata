# Turf2Surf WP2 Supporting documentation for data

## Overview
- Describes the Turf2Surf WP2 data collection and processing to study nitrogen and phosphorus impacts on carbon exchange between land and atmosphere in the Conwy catchment.
- Data span aboveground biomass, plant physiology and traits, soil properties, phosphorus fractions, available carbon and nitrogen, cations, root biomass, and elemental soil composition.
- Aims to support data discovery, integration into models (e.g., JULES), and cross-site comparisons; outputs intended to enable data-driven insights and further data products.

## Study Area and Aim
- Location: Conwy catchment, North Wales (~500 km²) with diverse habitats and climates.
- Scope: Holistic understanding of ecological, biogeochemical, and hydrological processes from gene to landscape scale; emphasis on linking plant and soil nutrients to ecosystem processes and carbon exchange.
- Stakeholders: Water industries, agriculture, forestry, fisheries, conservation groups, and local communities.

## Data Collected (key data types)
- Plant data
  - Aboveground net primary productivity (NPP) and standing biomass across sites (2013–2015); field clipping, cages to exclude grazing, and biomass/dry weight measurements.
  - Plant photosynthesis measures (Vcmax, Jmax, Asat) for dominant species; in-field CO2 curves and model-based parameter estimation; temperature corrections to 25°C; data processing scripts available.
  - Leaf traits and plant community traits (N, P, LDMC, SLA, LMA, canopy height, bryophyte cover) measured at most sites (2013–2014). LMA/L SMA calculations from leaf area via ImageJ; chemical analyses for N and P.
- Soil data
  - General soil measures: intact cores to 1 m depth; depth-segmented sampling; soil water content, bulk density, LOI and LOI-C, pH, EC; total C and N analyses.
  - Phosphorus fractions: Olsen P, Root-P, Complex-P, Enzyme-P, Complex-P via multiple extraction protocols; colorimetric phosphate measurements.
  - Available carbon and nitrogen: DOC and TDN via 0.5 M K2SO4 extraction; NO3 and NH4 via standard colorimetric assays.
  - Soil available cations: Ca, Na, K via 0.5 M acetic acid extraction; flame photometry.
  - Root biomass: total and fine roots; WinRhizo root analysis; in-growth root cores to study root growth and biomass.
  - Soil elements: TXRF (Total X-Ray Fluorescence) elemental analysis (Al, Fe, Ca, K, Ti, S, etc.) across sites; detailed lab protocol and QA notes.
- Dataset integration
  - Data collected to support integration into JokULES and other ecosystem models; cross-linking of plant and soil parameters to aboveground and belowground processes.

## Sampling Design and Sites
- Catchment-wide design across diverse habitats (e.g., blanket bog, heath, grasslands, woodlands, lakes, wetlands, arable land).
- Site and plot structure
  - 17 soil habitats sampled within 23 site descriptions; plots per habitat range from 1 to 4.
  - Each habitat site includes detailed location and dominant plant description; depth- and species-specific sampling for different data streams.
- Temporal scope
  - NPP (2013–2015), photosynthesis and leaf-trait measurements (2013–2014), soil sampling (spring 2014); ongoing dataset development for broader temporal coverage.

## Data Processing and Modeling
- NPP and biomass
  - Standardized protocols to measure NPP by species; adjustments for plant life cycles; biomass scaled to per m² values.
- Photosynthesis data
  - A-Ci curves analyzed with Farquhar-based models; temperature corrections to 25°C; Vcmax and Jmax derived; scripts (Levenberg–Marquardt) and model fitting described; R scripts available via GitHub.
- Leaf and plant traits
  - Leaf N, P, LDMC, SLA, LMA calculations; leaf area analysis via ImageJ; standard lab analyses for N and P.
- Soil and nutrients
  - QA/QC procedures noted for C and N measurements; multiple extraction methods for P fractions; DOC/TDN analyzed with specified instrumentation and protocols.
- Root and TXRF data
  - Root biomass and in-growth cores processed with imaging (WinRhizo) and dry weight; TXRF sample preparation and analysis described; limitations acknowledged in dedicated file.

## Dataset Structure and File Descriptions
- Five data files
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Common column schema (highlights)
  - Column A: unique Site number
  - Columns B–D: habitat details and site name
  - Column E: ecosystem component (plant, soil, or roots)
  - Column F: for plants – species; for soil/roots – NA
  - Columns G–H: Plot number (1–4) and Replicate number
  - Column I: Soil depth interval (for Soil and Roots)
- Missing data indicated as NA
- Data provenance and responsibilities (per section)
  - Data responsible contacts listed for each data category (e.g., NPP: Simon Smart; Photosynthesis: Lina Mercado; Leaf traits: Lina Mercado and Simon Smart; Soil measures and fractions: Helen Glanville; Available C/N: Helen Glanville; Cations: Helen Glanville; Root biomass: Helen Glanville; TXRF: Helen Glanville)
- Additional notes
  - A separate document provides detailed NPP methodology; a GitHub repository hosts photosynthesis modeling scripts.
  - TXRF limitations discussed in Turf2Surf_WP2_TXRF_Limitations_Glanville.rft

## Access, Reuse, and Contacts
- Primary data custodians and PIs listed with contact emails in the respective sections.
- Model and analysis scripts referenced (e.g., mdekauwe/FitFarquharModel on GitHub) for reproducing photosynthesis parameter estimations.
- Useful for cross-site comparisons, data integration into ecosystem models (e.g., JULES), and development of data products enabling broader data use.

## Summary of Utility for Data Support
- Provides a comprehensive, multi-domain data package linking plant productivity, physiology, and traits with soil chemistry, nutrient pools, and root dynamics across a heterogeneous catchment.
- Enables self-serve data exploration through clearly structured files and column definitions; enables integration into land-surface models and ecological analyses.
- Includes detailed protocols and QA notes to support data quality assessment and reuse, with explicit responsibilities and data provenance to facilitate collaboration and data governance.