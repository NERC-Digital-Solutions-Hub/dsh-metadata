# Overview

- Study location and scope
  - Field surveys in Sabah, Malaysian Borneo (July–November 2017)
  - 18 sites total: 14 fragmented forest sites within RSPO-certified oil palm plantations (conservation set-asides) and 4 sites in a large, continuous forest tract for comparison
  - 49 plots across 18 sites; plots are 30 m radius (0.28 ha)
  - Fragmented sites sampled to capture edge effects and fragmentation variation; continuous forest included for baseline comparison
  - Dominant soils: orthic acrisols and dystric cambisols
  - Sites ≥1.5 km apart to minimize spatial autocorrelation; maximum inter-site distance ~192 km

- Study design and sampling framework
  - Nested plot design with three hierarchical levels:
    - Main plot: 30 m radius (trees ≥25 cm dbh and coarse woody debris ≥25 cm)
    - Subplot: 20 m radius (trees 10–25 cm dbh and CWD 10–25 cm)
    - Small subplot: 5 m radius (trees 2–10 cm dbh)
  - Ground vegetation sampled with eight 1×1 m quadrats per plot, located 25 m from plot center along eight cardinal bearings
  - Edge and fragmentation context quantified using UAV-derived landscape metrics within 0.1–2 km buffers

- Data files and contents
  - CWD.csv: coarse woody debris measurements (deadwood ≥10 cm; size, decay class, orientation)
  - lianas.csv: liana dbh and association with host trees (note: lianas not identified to species)
  - seedlings_groundveg.csv: ground vegetation and tree seedlings by morphospecies in eight 1×1 m quadrats
  - sites_habitat.csv: plot- and site-level habitat, topography, fragmentation metrics, and broad landscape context
  - soil.csv: eight soil parameters per plot (pH, phosphorus, nitrogen, carbon, moisture, C:N ratios)
  - trees.csv: living trees and palms with dbh, height (where available), and liana associations
- Data collection period and protocols
  - Fieldwork conducted July–November 2017
  - Standardized protocols for: dbh measurement, height estimation (eye estimates with validation using tangent method), liana measurement, CWD assessment, and seedling/ground-vegetation surveys
  - Species identification notes: live trees identified to genus and species when known; palms not identified; most ground vegetation vouchers collected
- Fragmentation and landscape metrics
  - Landscape context derived from UAV imagery within 0.1–2 km buffers around each plot
  - Metrics include:
    - Total forest area (km²) within buffer
    - Edge index (proportion of forest adjacent to oil palm)
    - Straight-line distance to nearest forest-oil palm edge
    - Years since fragmentation (since first adjacent oil palm establishment)
  - For continuous forest plots, forest area and edge metrics calculated from Google Earth imagery

- Habitat, structure, and topography measurements
  - Leaf litter depth (five measurements per ground quadrat)
  - Forest canopy cover estimated with a spherical crown densiometer (four cardinal directions)
  - Elevation, latitude/longitude (GPS), and slope (in four directions)

- Ground cover, species, and biodiversity notes
  - Ground vegetation identified to genus; some morphospecies unidentified or only identified to family
  - Exotics vs natives recorded for ground vegetation
  - Palms and lianas in lianas.csv should be excluded from biodiversity or community analyses due to identification status

- Data processing, analysis guidance, and quality control
  - Forest canopy cover: canopy_pct = 100 − 1.04 × (Forest_cover readings average)
  - Tree height modeling: predict heights for stems lacking measurements using height–dbh relationship; exclude irregular stems (e.g., multi-stemmed, leaning) from height-model development
  - For eye-based height estimates, when Degrees_to_base is missing but Degrees_to_top is present, height is computed from tangent method plus 1.5 m eye level
  - Quality control: consistent observer for specific measurements; data checked for errors; methodology aligns with published protocols

- Key caveats and usage notes
  - Biodiversity analyses should exclude palms and lianas from lianas.csv due to lack of species identification
  - Ground vegetation identifications vary in taxonomic resolution (some morphospecies unidentified or only to family)
  - Height estimates rely on derived models; exclude irregular stems when constructing predictive height models
  - Some fields reference additional information useful for analysis (e.g., supplementary notes on data interpretation) not included in this summary

- References and context
  - Field and analytical methods are aligned with established tropical forest measurement protocols (e.g., RAINFOR/BIOMASS, harmonized decay classes, standard dbh/height measurement approaches)
  - Contextual literature covers oil palm expansion, fragmentation, and forest conservation under RSPO guidelines and related biodiversity assessments