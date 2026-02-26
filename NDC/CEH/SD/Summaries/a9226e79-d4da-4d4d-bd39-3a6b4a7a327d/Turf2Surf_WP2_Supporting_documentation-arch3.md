# Turf2Surf WP2 Supporting documentation for data

- Focus: Coupled nutrient cycling in terrestrial and freshwater ecosystems; nitrogen and phosphorus impacts on carbon exchange; links to water quality, carbon sequestration, and biodiversity.
- Purpose for monitoring frameworks: Provides baseline, multi-habitat data and detailed methodologies to inform monitoring design, data collection, quality control, and data governance for environmental health indicators; supports integration into the JULES model.

## Context and study area

- Location: Conwy catchment, North Wales (~500 km2) with diverse landscapes and climatic gradient.
- Objectives: Develop holistic understanding of pressures on natural resources and benefits; study ecological, biogeochemical, and hydrological processes from gene to landscape scale.
- Stakeholders: Water industries, foresters, farmers, shell fisheries, conservation groups, local communities.

## Habitats and sampling framework

- Sites: 23 habitat locations with varying dominant plant communities; table lists unique site numbers, number of plots, location descriptions, and dominant species.
- Sampling emphasis: Baseline, consistent measurements across habitats to support cross-site comparisons and process understanding.
- Vegetation management: NPP and biomass measurements account for grazing and habitat type; specific arrangements for grassland, bogs, woodlands, and moorland.

## Key measurements and data sources

- 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
  - Data responsibility: Simon Smart
  - Coverage: Annual NPP for dominant species at all sites (2013–2015); 4 plots per site; winter clipping and grazing protection where applicable; biomass measured in both grasses/bogs and woodlands with tree cores and litter biomass included.
  - Purpose: Link plant productivity to soil nutrients and to models (e.g., JULES).

- 3.1.2 Plant photosynthesis measures
  - Data responsibility: Lina Mercado
  - Parameters: Vcmax, Jmax (25°C), Asat (field and chamber-based measurements across dominant species)
  - Techniques: CO2 concentration curves (CO2 up to 2000 ppm), light conditions, and temperature corrections; modeling with Farquhar-based framework; temperature corrections following established literature.
  - Purpose: Characterize photosynthetic capacity to inform carbon and nutrient cycling in models.

- 3.1.3 Leaf traits and plant community traits
  - Data responsibility: Lina Mercado, Simon Smart
  - Traits: Leaf N and P, LDMC, SLA, LMA, canopy height, bryophyte cover
  - Methods: Leaf sampling around measured plots; image-based LMA calculations; standard chemical analyses for N and P.
  - Purpose: Trait-based linkages between plant function and nutrient cycling; input for ecosystem models.

- 3.2.1 General soil measures
  - Data responsibility: Helen Glanville
  - Methods: Intact soil cores (0–1 m) from 17 habitats; depth-stratified sampling; SWC, BD, LOI, LOI-C, pH, EC, total C and N
  - Purpose: Baseline soil physical and chemical properties across habitats; QA/QC procedures described; supports soil nutrient modeling.

- 3.2.2 Phosphorus
  - Data responsibility: Helen Glanville
  - Fractions: Olsen P, Root-P, Complex-P, Enzyme-P, Proton-P
  - Methods: Colorimetric assays (Malachite Green) with multiple extraction schemes (Olsen, CaCl2 for root P, citrate for organic-inorganic pools, enzyme-assisted P), 630 nm reads; standard calibration and QA steps noted.
  - Purpose: Detailed P pool characterization to understand availabilities and plant access.

- 3.2.3 Available carbon and nitrogen
  - Data responsibility: Helen Glanville
  - Fractions: DOC and TDN; extraction with 0.5 M K2SO4; subsequent analysis
  - Methods: Field-collected soils (17 habitats); lab analyses with QA steps; storage considerations described
  - Purpose: Evaluate readily available C and N pools feeding microbial and plant processes.

- 3.2.4 Soil available cations (Ca, Na, K)
  - Data responsibility: Helen Glanville
  - Methods: Extraction with 0.5 M acetic acid; flame photometry for cation concentrations
  - Purpose: Key nutrient drivers for soil-plant interactions and buffering capacity.

- 3.2.5 Root biomass
  - Data responsibility: Helen Glanville
  - Measurements: Total and fine root biomass; WinRhizo root scanning for structural traits; in-growth cores to assess root growth
  - Sites: Capel Curig, Nant-y-Brwyn, Red Kite Woods, Alan Davies farm sites, Migneint bog
  - Purpose: Belowground resources and growth dynamics to complement aboveground measures

- 3.2.6 Soil elements – TXRF
  - Data responsibility: Helen Glanville
  - Method: TXRF (Bruker S2 PicoFOX); samples prepared from dried, ground soils; internal standards and calibration described
  - Scope: Broad element suite (Al, Fe, Ca, K, Ti, S, Ba, Mn, P, Sr, Zr, Cl, V, Rb, Zn, Cr, Nd, La, Cu, Y, Ni, Pb, Ga, Nb, Th, Co, Sc, As, Cs, U, Sn, Ge, I, Br, Sb, Se, Cd, Hg)
  - Purpose: Comprehensive soil elemental fingerprint to support nutrient cycling analyses

## Dataset structure and accessibility

- Dataset contents: Five CSV files
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Common schema: Site number; Habitat and detailed habitat description; Site name; Ecosystem component (Plant, Soil, Roots); Plant species (where applicable); Plot and Replicate numbers; Soil depth interval (for Soil and Roots)
- Missing data: Indicated as NA where data are unavailable due to depth restrictions, limited replicates, or other constraints
- Data sharing and reuse: Described as available to other research projects; emphasis on data processing scripts and modules; references to public code repositories (e.g., FitFarquharModel) and a TXRF limitations file for transparency
- Data governance notes: QA/QC processes outlined in multiple sections; explicit acknowledgment of data owners (data responsible persons) for each measurement domain; integration into modeling workflows (e.g., JULES)

## Data governance, quality, and limitations

- QA/QC: Explicit QA/QC steps for major analyses (e.g., C/N, P fractions, TXRF), standard reference materials, calibration ranges, and data handling procedures
- Metadata and documentation: Comprehensive methodological descriptions; separate methodology document for NPP; dedicated notes on TXRF limitations
- Data integration: Designed to feed parameterization and validation for the JULES model, linking plant, soil, and nutrient processes
- Access considerations: Acknowledges baseline data availability to other research projects; potential barriers to public data sharing are recognized in the broader project context

## Roles and contact points

- Plant biomass and NPP: Simon Smart
- Plant photosynthesis measures and leaf traits: Lina Mercado; collaboration with CEH Bangor (Harry Harmens, Sabine Reinsch)
- Soil general measures, phosphorus fractions, available C/N, cations, root biomass, TXRF: Helen Glanville (and collaborators)
- Data processing and modeling support: Multiple authors, with references to scripts and code repositories
- Overall coordination: Turf2Surf WP2 team and CEH colleagues

## Relevance for monitoring frameworks

- Comprehensive, multi-habitat baseline data enabling cross-site comparisons and trend analyses
- Detailed measurement protocols and standardized depth-resolved soil sampling to support consistent monitoring
- Integration-ready data (plant and soil nutrients, carbon dynamics, and elemental soil composition) for process-based modeling and scenario assessment
- Clear data governance and sharing approach, with explicit QA/QC and metadata practices to facilitate data reuse and replication in policy evaluation and decision-making