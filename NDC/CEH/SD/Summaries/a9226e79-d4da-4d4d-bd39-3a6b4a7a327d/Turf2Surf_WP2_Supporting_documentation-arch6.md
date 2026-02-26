# Turf2Surf WP2 Supporting documentation for data

## Overview
- Focus of Turf2Surf: coupled nutrient cycling in terrestrial and freshwater ecosystems; linked to water quality, carbon sequestration, and biodiversity.
- WP2 scope: study nitrogen and phosphorus related impacts on carbon exchange between land and atmosphere.
- Project and authors: Bridget Emmett, Davey Jones, Simon Smart, Lina Mercado, Helen Glanville, Maria C Blanes, Harry Harmens, Sabine Reinsch; correspondence and data responsibility listed for each data area.
- Versions: 01/06/2016; 25/08/2016; 04/11/2016.

## Context and site information
- Study area: Conwy catchment, North Wales (~500 km2) with diverse habitats and climatic gradient; main river and estuary drainage.
- Habitats: blanket bog, moorland, woodlands, grasslands, lakes, floodplains, salt marshes, etc., supporting extensive stakeholder engagement.
- Sampling scope: 17 soil habitats sampled across the catchment (sites 1-10, 14-21); dominant plant species mapped per site; sampling across multiple plots and depths.

## Data components and datasets
- Five data files form the dataset:
  1) Turf2Surf_Plant_biomass_data.csv
  2) Turf2Surf_Plant_structural_data.csv
  3) Turf2Surf_Plant_physiological_data.csv
  4) Turf2Surf_Soil_Carbon_data.csv
  5) Turf2Surf_Soil_raw data.csv
- Column structure (Dataset 4.0 description):
  - Column A: Site number
  - Columns B-C: Habitat and detailed habitat description
  - Column D: Site name
  - Column E: Ecosystem Component (plant, soil, or roots)
  - Column F: Species (for plant components) or NA for soil/roots
  - Columns G-H: Plot number and Replicate number
  - Column I: Soil depth interval (for soil and roots)
  - NA indicates missing data due to depth/restrictive sampling or outliers

## Measurements and data processing (key sections)

### 3.1 Plant measurements
- 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
  - Data responsibility: Simon Smart
  - NPP: measured annually 2013–2015 on dominant species across sites; four plots per site; winter clipping with grazing protection; adjustments for plant life cycles.
  - Standing biomass: measured at 10 of 17 sites; grasses/bogs: harvest in 1 m x 1 m quadrats; woodland: 200 m2 plots with tree cores and leaf litter added to biomass calculations.
  - Purpose: to link plant productivity to soil nutrients and integrate parameters into JULES model.
- 3.1.2 Plant photosynthesis measures
  - Data responsibility: Lina Mercado
  - Parameters: Vcmax, Jmax, Asat for dominant species
  - Methods: field CO2 measurements with CIRAS-I and LICOR 6400; CO2 curves from 50–2000 ppm; temperature corrections to 25°C; analysis via Farquhar-based model; scripts available (GitHub).
  - Relevance: inputs for photosynthesis parameterization in ecosystem models; linked to Turf2Surf WP2 data processing.
- 3.1.3 Leaf traits and plant community traits
  - Data responsibility: Lina Mercado, Simon Smart
  - Traits measured: leaf N, leaf P, leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover
  - Methods: leaf sampling and processing (LMA via leaf area and dry weight; SLA as inverse of LMA); N and P analysis; leaf traits integrated with WP2 to parameterize JULES
  - Role: supports linking plant traits to nutrient cycling and carbon processes

### 3.2 Soil measurements
- 3.2.1 General soil measures
  - Data responsibility: Helen Glanville
  - Sampling: intact cores (17 habitats, depths 0–1 m in intervals); SWC, bulk density (BD), LOI and LOI-C, pH, EC, total C and N
  - Methods: standard core processing, oven drying, soil chemistry analyses; QA/QC with calibration and reference materials
- 3.2.2 Phosphorus (P) fractions
  - Data responsibility: Helen Glanville
  - Fractions: Olsen P, Root-P, Complex-P, Enzyme-P, Proton-P
  - Methods: diverse extraction protocols with colorimetric malachite green assay; detailed steps for each P pool
  - Purpose: characterize plant-available and bioactive P pools to inform soil-plant nutrient dynamics
- 3.2.3 Available carbon (C) and nitrogen (N)
  - Data responsibility: Helen Glanville
  - Methods: 0.5 M K2SO4 extraction for available C and N; subsequent colorimetric or instrument-based analyses; DOC and TDN measured at CEH Bangor
  - Nitrate and ammonium analyses: established colorimetric assays
- 3.2.4 Soil available cations (Ca, Na, K)
  - Data responsibility: Helen Glanville
  - Methods: extraction with 0.5 M acetic acid; measurement by flame photometry
- 3.2.5 Root biomass
  - Data responsibility: Helen Glanville
  - Methods: soil cores; separation of fine vs. large roots; WinRhizo root imaging for length/diameter metrics; dry weight calculations; in-growth core experiments to assess root growth
- 3.2.6 Soil elements – TXRF analysis
  - Data responsibility: Helen Glanville
  - Method: TXRF (Bruker S2 PICOFOX) for multi-element soil composition; sample prep with grinding, suspension, and disc deposition
  - Documentation: TXRF limitations discussed in Turf2Surf_WP2_TXRF_Limitations_Glanville.rft

## Dataset structure and data quality
- File formats: five CSV data files with clearly defined columns (site, habitat, site name, ecosystem component, species, plot, replicate, depth)
- Metadata and responsibility: data producers listed per data type; diverse QA/QC protocols described; some scripts and modeling tools linked (see below)
- Links to data processing and models:
  - NPP data processing detailed in Turf2Surf_WP2_NPP_Smart.rft
  - Photosynthesis modeling scripts: https://github.com/mdekauwe/FitFarquharModel
- TXRF limitations: noted in a dedicated file Turf2Surf_WP2_TXRF_Limitations_Glanville.rft

## Access, use, and integration into models
- Data are designed to support cross-topic data use (plants and soils) and integration into the JULES land-surface model.
- Structure enables cross-site comparisons across habitats, depths, and functional groups (plants, soils, roots).
- Clear attribution of data responsibilities aids data provenance and reuse in policy, conservation, and research contexts.

## Contact and QA references
- Primary contacts for data components are listed with emails (e.g., ssma@ceh.ac.uk; L.Mercado@exeter.ac.uk; h.c.glanville@bangor.ac.uk; MC Blanes; etc.)
- Methodological references and detailed protocols provided within the document and linked supporting files.