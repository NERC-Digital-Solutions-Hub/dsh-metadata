# Turf2Surf WP2 Supporting documentation for data

## Overview
- Describes WP2 activities within the Turf2Surf project: coupled nutrient cycling in terrestrial and freshwater ecosystems and links nitrogen and phosphorus impacts to carbon exchange.
- Data responsibilities focus on connecting plant and soil nutrients to ecosystem processes and integrating parameters into the JULES model.

## Study area and context
- Conwy catchment, North Wales (~500 km²), diverse habitats and climatic gradient; stakeholders include water industries, farmers, foresters, conservation groups and local communities.
- Aims to develop a holistic understanding of pressures on natural resources and associated benefits.
- Extensive baseline data available for reuse by other research projects; data products support wider community engagement and collaboration.

## Data assets and accessibility
- Five data files covering plant biomass, plant structure, plant physiology, soil carbon, and raw soil data.
- Column definitions emphasize Site number, Habitat, detailed habitat description, Site name, ecosystem component (Plant/Soil/Roots), species (for plants), Plot and Replicate numbers, and Soil depth intervals (for Soil/Roots).
- Missing values are indicated as NA.
- Data intended for reuse and integration into broader analyses, including model parameterization (e.g., JULES).

## Sampling design and data collection
- Conwy catchment sampled across 17 habitats with multiple plots per site; soil cores collected to 1 m depth and divided into depth intervals (0–15, 15–30, 30–45, 45–60, 60–75, 75–90, 90+ cm).
- Aboveground Net Primary Productivity (NPP) measured 2013–2015 for dominant species; protection during growth via winter cages in grazed habitats.
- Aboveground standing biomass measured at 10 of 17 sites; distinct methods for grassy/bog habitats versus woodland.
- Root biomass and root growth measured using soil cores and in-growth cores; leaf and shoot traits collected for multiple species.

## Data processing and responsibilities
- Data responsibility and processing led by several researchers (notably Simon Smart, Lina Mercado, Sabine Reinsch, Helen Glanville, and colleagues across CEH Bangor, Bangor University, Exeter University).
- NPP processing linked to JULES modeling; photosynthesis parameters (Vcmax, Jmax, Asat) derived from field and chamber measurements with specific software and calibration (e.g., De Kauwe’s FitFarquharModel scripts; temperature corrections).
- Leaf traits (N, P, LDMC, SLA, LMA, canopy height, bryophyte cover) measured and processed; protocols for sampling, scanning, and chemical analyses outlined.
- Soil analyses include general properties (pH, EC, bulk density, LOI/LOI-C, C/N), phosphorus fractions (Olsen-P, Root-P, Complex-P, Enzyme-P, Proton-P), available C and N (via K2SO4 extraction), NO3 and NH4 determinations, DOC/TDN, available cations (Ca, Na, K), root biomass via imaging, and TXRF elemental analysis.
- QA/QC and methodological references noted (limitations of TXRF documented in Turf2Surf_WP2_TXRF_Limitations_Glanville.rft).

## Datasets and structure
- Data files:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Column A: unique Site number; Column B–C: Habitat, habitat description; Column D: Site name; Column E: ecosystem Component (Plant/Soil/Roots); Column F: plant species (if applicable); Columns G–H: Plot and Replicate numbers; Column I: Soil depth interval for Soil/Roots.
- Missing data marked as NA; data are organized to support cross-site comparisons and model parameterization.

## Variables and methods (highlights)
- Plant: aboveground biomass, NPP, leaf traits (N, P, LDMC, SLA, LMA), canopy height, bryophyte cover; photosynthesis measures (Asat, Vcmax, Jmax).
- Soil: general properties (pH, EC, BD, C, N, LOI, LOI-C), available C and N (0.5 M K2SO4 extraction), P fractions (Olsen-P, Root-P, Complex-P, Enzyme-P, Proton-P), NO3, NH4, DOC, TDN, available Ca/Na/K, TXRF elemental composition.
- Roots: total and fine biomass; in-growth root cores; root traits via WinRhizo.
- Dataset structure is designed to feed into ecosystem models (e.g., JULES) and support cross-cutting analyses.

## Versioning and contacts
- Version dates: 01/06/2016; 25/08/2016; 04/11/2016.
- Principal authors and data responsibilities listed (Sabine Reinsch, Helen Glanville, Simon Smart, Lina Mercado, and others).
- Data responsible contacts provided for various sections (e.g., NPP, photosynthesis, leaf traits, soil analyses).

## Notes for Data Leaders
- Data assets are intended for reuse beyond Turf2Surf WP2 and should be documented with clear metadata and provenance.
- The dataset supports an integrated view of plant and soil processes across a heterogeneous catchment, aligning with holistic data-system thinking and user needs.
- Data quality varies by habitat and depth; recognize NA values and depth-specific limitations when planning analyses.
- TXRF-related data have documented limitations and should be treated accordingly in analyses and reporting.