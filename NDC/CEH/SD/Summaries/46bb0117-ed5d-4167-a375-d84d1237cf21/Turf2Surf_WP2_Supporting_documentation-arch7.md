# Turf2Surf WP2 Supporting documentation for data

## Overview
- The Turf2Surf project investigates coupled nutrient cycling in terrestrial and freshwater ecosystems, focusing on nitrogen and phosphorus impacts on carbon exchange between land and atmosphere.
- WP2 collects plant- and soil-related data to link nutrient dynamics with ecosystem processes and to inform the JULES land-surface model.

## Study area and sampling framework
- Location: Conwy catchment, North Wales (~500 km2), with a strong climatic gradient and diverse habitats (bogs, moorland, grasses, woodlands, lakes, flood plains, and estuarine interfaces).
- Sampling framework: 17 habitats/sites across the catchment (sites 1–10 and 14–21; some site numbers indicate multiple habitat/age classes within locations). Table 1 lists habitats, number of plots, locations, and dominant species.
- Data are organized to enable cross-site comparisons and integration with ecosystem process models, emphasizing plant–soil nutrient linkages.

## Data contents by domain

- Plant data
  - Biomass and productivity: Aboveground net primary production (NPP) measured annually 2013–2015 for dominant species across four plots per site; winter clipping and grazing exclusion where appropriate; biomass converted to per-m2 values.
  - Structural data: Aboveground biomass for trees/shrubs in woodland habitats; litter and leaf biomass included in soil- and canopy-level calculations.
  - Photosynthesis measures: Vcmax, Jmax, Asat measured for dominant species using CIRAS/Licor systems; CO2 curves and temperature corrections applied; data and scripts linked to Farquhar model.
  - Leaf traits and community traits: Leaf N, leaf P, leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover.

- Soil data
  - General soil measures: Intact cores collected to 1 m depth (17 habitats); depth-resolved sampling (0–15, 15–30, 30–45, 45–60, 60–75, 75–90, 90+ cm) for a total of 300 samples; bulk density, water content, pH, EC, LOI, LOI-C, and total C and N.
  - Phosphorus fractions: Olsen P, Root-P, Complex-P, Enzyme-P, Proton-P; multiple extraction methods and colorimetric assays described.
  - Available C and N: DOC and TDN measured after 0.5 M K2SO4 extraction; detailed extraction and analysis protocol.
  - Available cations: Ca, Na, K measured via 0.5 M acetic acid extraction and flame photometry.
  - Root biomass and growth: 15 cm cores at several sites; root scanning (WinRhizo) for total and fine root biomass; in-growth root tubes to assess root growth over a season.
  - TXRF elemental analysis: Comprehensive soil element suite (Al, Fe, Ca, K, Ti, S, Ba, Mn, P, Sr, Zr, Cl, V, Rb, Zn, Cr, Nd, La, Cu, Y, Ni, Pb, Ga, Nb, Th, Co, Sc, As, Cs, U, Sn, Ge, I, Br, Sb, Se, Cd, Hg) on sites 1–10 and 14–21; detailed sample preparation and instrument setup described; limitations discussed in a separate document.

- Roots
  - Root biomass (above and belowground integration): as above; in-growth cores provide additional data on root proliferation; root measurements aligned with soil data for integrated analyses.

- TXRF
  - Elemental soil composition across depths and habitats; method details and lab work responsibilities noted; limitations documented in dedicated file.

## Dataset structure and files
- Five data files:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Common data schema (Columns A–I):
  - A: Site number (as per Table 1)
  - B: Habitat
  - C: Habitat description
  - D: Site name
  - E: Ecosystem Component (Plant, Soil, Roots)
  - F: Plant species (if Ecosystem Component = Plant; otherwise NA)
  - G: Plot number (1–4)
  - H: Replicate number (used when measurements are not co-located with plots)
  - I: Soil depth interval (for Soil and Roots only)
- Data quality notes:
  - Missing values are indicated as NA
  - Depth-specific data apply to Soil and Roots; other components are not depth-sliced

## Methodology highlights relevant to GIS and mapping
- Spatial design: Site- and habitat-based sampling across a range of ecosystems within the Conwy catchment; data structured to support site-level mapping and depth-resolved soil spatial analysis.
- Data products intended for GIS use: dataset files with consistent site identifiers, habitat descriptors, and replicate information enable join operations with habitat maps, land-use layers, and other spatial datasets.
- Integration with models: Data collected to parameterize JULES and to link plant and soil nutrient pools with above- and below-ground processes; suitable for spatially explicit modelling and scenario analysis.

## Data usage and interpretation notes
- Temporal scope for plant data spans 2013–2015 for NPP and 2013–2014 (plus additional years for some measures) for photosynthesis.
- Phosphorus and carbon analyses include multiple fractions and enzyme pools to capture labile and recalcitrant pools.
- TXRF provides a broad elemental profile; limitations are discussed in Turf2Surf_WP2_TXRF_Limitations_Glanville.rft (reference document).
- Data responsibility and provenance: multiple authors and institutions (CEH, Bangor University, Exeter University) with clearly defined data owners for each measurement type; versioned with initial dates in 2016.

## Key contacts and versioning
- Data responsible for major components is listed per section (e.g., NPP: Simon Smart; Photosynthesis: Lina Mercado; Leaf traits: Lina Mercado, Simon Smart; Soil measures: Helen Glanville and team; TXRF: Helen Glanville and collaborators).
- Version dates: 01/06/2016; 25/08/2016; 04/11/2016.

## Abbreviations (selected)
- Asat, Vcmax, Jmax: photosynthesis measures
- NPP: Aboveground net primary production
- LDMC: Leaf dry matter content
- SLA: Specific leaf area
- LMA: Leaf mass per area
- SWC: Soil water content
- BD: Bulk density
- LOI/LOI-C: Loss on ignition and LOI-derived carbon
- P, Olsen P, Root-P, Complex-P, Enzyme-P, Proton-P: phosphorus fractions
- DOC, TDN: dissolved organic carbon and total dissolved nitrogen
- TXRF: Total X-ray fluorescence analysis