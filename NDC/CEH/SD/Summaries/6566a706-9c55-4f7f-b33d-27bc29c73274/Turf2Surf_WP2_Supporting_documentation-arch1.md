# Turf2Surf WP2 Supporting documentation for data

- Project focus and aim
  - Turf2Surf investigates coupled nutrient cycling in terrestrial and freshwater ecosystems, linking nitrogen and phosphorus impacts to carbon exchange, water quality, and biodiversity.
  - WP2 specifically studies how nitrogen and phosphorus relate to carbon exchange between land and atmosphere, integrating plant–soil nutrient data into the JULES model.

- Study area
  - Conwy catchment, North Wales (~500 km2) with a climate/land-use gradient.
  - Diverse habitats (blanket bog, moorland, conifer woodland, grassland, lakes/reservoirs, flood plains, salt marsh) and a range of stakeholders (water industry, farming, forestry, conservation, communities).

- Habitats and sampling sites
  - 17 soil habitats across multiple sites (1–21), with detailed site descriptions and dominant species where available.
  - Sampling structure includes 3–4 plots per site for NPP, and 3–9 replicates per habitat for aboveground biomass; sampling locations mapped across the catchment.

- Key data types and measurements (WP2 data)

  - 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
    - Annual NPP measured for dominant species at all sites (2013–2015) with seasonal clipping and grazing protection where applicable.
    - Aboveground biomass measured at 10 of 17 sites, using standardized plot, canopy, or tree-core methods depending on vegetation type.
    - Data processed to align with plant life strategies; linked to aboveground processes for incorporation into JULES.

  - 3.1.2 Plant photosynthesis measures
    - Parameters: Asat, Vcmax, Jmax (25°C) derived from A-Ci curves using LICOR equipment and standard modeling (Farquhar framework).
    - Measurements conducted in 2013–2014 and 2014–2016 with field and laboratory protocols; temperature corrections applied to 25°C.
    - Data processing scripts and modeling approach referenced (GitHub: FitFarquharModel).

  - 3.1.3 Leaf traits and plant community traits
    - Leaf N and P, leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover.
    - LMA/LAS/LMA measurement workflow described; elemental analyses conducted on leaf samples.

  - 3.2.1 General soil measures
    - Intensive soil core sampling (to 1 m, spring 2014) across 17 habitats; depth-stratified sampling (0–15, 15–30, …, 90+ cm).
    - Measurements: soil water content (SWC), bulk density (BD), loss-on-ignition (LOI and LOI-C), pH, electrical conductivity (EC), total C and N.
    - QA/QC and multi-analytical coordination across labs.

  - 3.2.2 Phosphorus (P fractionation and availability)
    - Olsen P (extracted with 0.5 M NaHCO3, colorimetric Malachite Green method).
    - Root-P (0.01 M CaCl2 extraction), Complex-P (10 mM citrate), Enzyme-P (phosphatase and phytase enzyme extracts), and Proton-P (1 M HCl extraction) with colorimetric detection.
    - Multiple extraction schemes reflect different P pools and mobilisation mechanisms.

  - 3.2.3 Available carbon and nitrogen
    - Soil available C and N via 0.5 M K2SO4 extraction from 17 habitats; analyses include DOC and TDN (oxidation/TOC-like methods), with QA/QC sequences.

  - 3.2.4 Soil available cations (Ca, Na, K)
    - Extraction with 0.5 M acetic acid; cations measured by flame photometry.
    - Data contribute to understanding base cation status and nutrient availability.

  - 3.2.5 Root biomass
    - Total and fine root biomass across six sites; 15 cm soil cores with depth fractionation (0–5, 5–10, 10–15 cm).
    - Roots scanned with WinRhizo for morphometrics; dry weight determined; in-growth cores used to assess root growth dynamics.

  - 3.2.6 Soil elements – TXRF analysis
    - Total elemental composition (Al, Fe, Ca, K, Ti, S, Zn, Mn, P, etc.) via TXRF (Bruker S2 PICOFOX).
    - Sample prep includes grinding, suspension, and disc deposition; results linked to soil biogeochemistry and nutrient interactions.

- Dataset structure and file overview
  - Five data files:
    - Turf2Surf_Plant_biomass_data.csv
    - Turf2Surf_Plant_structural_data.csv
    - Turf2Surf_Plant_physiological_data.csv
    - Turf2Surf_Soil_Carbon_data.csv
    - Turf2Surf_Soil_raw data.csv
  - Common column schema
    - Column A: Site number (matches Table 1)
    - Column B: Habitat
    - Column C: Habitat description
    - Column D: Site name
    - Column E: Ecosystem Component (Plant, Soil, or Roots)
    - Column F: Plant species (if Ecosystem Component is Plant; otherwise NA)
    - Column G: Plot number
    - Column H: Replicate number (for non-co-located measurements by site)
    - Column I: Soil depth interval (for Soil and Roots)
  - Data notes
    - Missing values marked as NA
    - Replicates reflect site-specific sampling logistics (e.g., dominant species at a site or non-coincident plots)

- Data management and accessibility
  - TheWP2 dataset is designed to support integration with the JULES land-surface model by providing plant and soil nutrient parameters.
  - Detailed methodologies and scripts (e.g., NPP processing, photosynthesis modeling) are documented and, where applicable, available via external references and repositories.
  - Dataset structure emphasizes traceability from site/habitat biology to soil processes and elemental analyses.

- References and methodology notes
  - Photosynthesis models follow Farquhar, Caemmerer, and Berry (1980) and related methodological refinements (De Pury & Farquhar, Medlyn et al., Kattge & Knorr).
  - NPP and leaf-trait workflows are linked to Turf2Surf WP2 documentation and reported in associated documents (e.g., Turf2Surf_WP2_NPP_Smart.rft).
  - TXRF limitations and laboratory details are discussed in Turf2Surf_WP2_TXRF_Limitations_Glanville.rft.